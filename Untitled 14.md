\section*{Modélisation des Tables de la Base de Données}

Une base de données MySQL a été utilisée pour persister de manière permanente les données relatives à l'application. L'utilisation d'une base de données a été jugée la plus efficace, car elle permet :
\begin{itemize}
  \item un chargement/recherche plus rapide des notes, utilisateurs et intervalles)
\end{itemize}

Voici un exemple de la modélisation de ces tables :

\begin{minted}[mathescape, linenos]{SQL}
CREATE TABLE Users (
  user_id INT AUTO_INCREMENT PRIMARY KEY,
  username VARCHAR(255) UNIQUE NOT NULL,
  password VARCHAR(255) NOT NULL,
  role ENUM('teacher', 'student', 'coordinator') NOT NULL,
  full_name VARCHAR(255) NOT NULL,
  created_at DATETIME NOT NULL
);

CREATE TABLE Classes (
  class_id INT AUTO_INCREMENT PRIMARY KEY,
  class_name VARCHAR(255) NOT NULL,
  grade_level ENUM('11', '12') NOT NULL,
  subject VARCHAR(255) NOT NULL,
  teacher_id INT NOT NULL,
  FOREIGN KEY (teacher_id) REFERENCES Users(user_id)
);

CREATE TABLE Grades (
  grade_id INT AUTO_INCREMENT PRIMARY KEY,
  student_id INT NOT NULL,
  class_id INT NOT NULL,
  grade_value DECIMAL(5,2) NOT NULL,
  total_value DECIMAL(5,2) NOT NULL,
  trimester ENUM('1', '2', '3') NOT NULL,
  date DATE NOT NULL,
  FOREIGN KEY (student_id) REFERENCES Users(user_id),
  FOREIGN KEY (class_id) REFERENCES Classes(class_id)
);

CREATE TABLE GradeBoundaries (
  boundary_id INT AUTO_INCREMENT PRIMARY KEY,
  class_id INT NOT NULL,
  over_value DECIMAL(5,2) NOT NULL,
  grades TEXT NOT NULL,
  FOREIGN KEY (class_id) REFERENCES Classes(class_id)
);

CREATE TABLE StudentClasses (
  student_id INT,
  class_id INT,
  FOREIGN KEY (student_id) REFERENCES Users(user_id),
  FOREIGN KEY (class_id) REFERENCES Classes(class_id)
);
\end{minted}

 Le système utilise un contexte d'authentification (AuthContext), une gestion des routes protégées (ProtectedRoute), et un formulaire de connexion (Login).

\textbf{AuthContext}

Le AuthContext est au cœur du système d'authentification. Il stocke l'état d'authentification global, y compris les informations de l'utilisateur et les fonctions pour se connecter et se déconnecter.

\begin{minted}[mathescape, linenos]{javascript}
export const AuthContext = createContext();
\end{minted}
Lors de la connexion, le token JWT est stocké dans le localStorage et décodé pour extraire les informations de l'utilisateur. Cela permet de persister l'état d'authentification entre les sessions.
\begin{minted}[mathescape, linenos]{javascript}
const login = (token) => {
  localStorage.setItem('token', token);
  const decoded = jwtDecode(token);
  setUser(decoded);
  navigate('/'); // Navigation vers le tableau de bord après la connexion
};
\end{minted}
\textbf{Login}

Le composant Login gère le formulaire de connexion. Il envoie les informations de connexion à l'API et traite la réponse.
\begin{minted}[mathescape, linenos]{javascript}
const handleSubmit = async (event) => {
  event.preventDefault();
  const response = await fetch('/api/login', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({ username, password })
  });
  if (response.ok) {
    const { token } = await response.json();
    login(token); // Utilisation de la fonction login du AuthContext
  } else {
    const { message } = await response.json();
    setErrorMessage(message || 'Login failed');
  }
};
\end{minted}
\textbf{ProtectedRoute}

ProtectedRoute est un composant qui sert à protéger les routes. Il vérifie si l'utilisateur est authentifié et autorisé à accéder à la route demandée. Si ce n'est pas le cas, l'utilisateur est redirigé vers la page de connexion.
\begin{minted}[mathescape, linenos]{javascript}
const ProtectedRoute = ({ children, allowedRoles }) => {
  const { user } = useContext(AuthContext);

  if (!user || !allowedRoles.includes(user.role)) {
    // Redirection vers la page de connexion si non authentifié ou non autorisé
    return <Navigate to="/login" replace />;
  }

  // Rendu des composants enfants si authentifié et autorisé
  return children;
};
\end{minted}
Sécurité

\begin{itemize}
\item Stockage sécurisé du token : Le token JWT est stocké dans le localStorage, ce qui permet de maintenir l'état de connexion entre les sessions.
\item Validation côté serveur : Les informations d'authentification (token JWT) sont validées côté serveur à chaque requête, ce qui assure que l'utilisateur est bien authentifié et autorisé à accéder aux ressources demandées.
\item Protection des routes : Le composant ProtectedRoute assure que seuls les utilisateurs authentifiés et ayant les bons rôles peuvent accéder à certaines parties de l'application.
\end{itemize}

\textbf{Sécurité des Mots de Passe}

La sécurité des mots de passe est essentielle pour protéger les comptes utilisateurs. Dans mon application, j'utilise la bibliothèque bcryptjs pour hacher les mots de passe avant de les stocker dans la base de données MySQL. Voici comment cela est mis en œuvre :
\begin{minted}[mathescape, linenos]{javascript}
const bcrypt = require('bcryptjs');

exports.addUser = async (req, res) => {
    const { username, password, role, full_name } = req.body;
    try {
        const hashedPassword = await bcrypt.hash(password, 10);
        // ...
        const [result] = await db.execute(`
            INSERT INTO Users (username, password, role, full_name) VALUES (?, ?, ?, ?)
        `, [username, hashedPassword, role, full_name]);
        // ...
    } catch (error) {
        // Gestion des erreurs
    }
};
\end{minted}
Lorsqu'un utilisateur s'inscrit, son mot de passe est haché avec bcrypt.hash, ce qui génère un hachage sécurisé. Ce hachage est ensuite inséré dans la table Users de la base de données.

\textbf{Gestion des Utilisateurs}
La gestion des utilisateurs est réalisée à travers différentes routes qui permettent d'ajouter, de récupérer, de mettre à jour et de supprimer des utilisateurs. Chaque utilisateur a un rôle qui détermine ses permissions dans l'application.
\begin{minted}[mathescape, linenos]{javascript}
javascript
const express = require('express');
const userRoutes = require('./routes/userRoutes');
// ...
app.use('/api', userRoutes);
\end{minted}

Les routes sont définies dans userRoutes et sont accessibles via l'API sous le chemin /api.

L'ajout de notes et de limites de notes est une autre fonctionnalité importante de votre application. Voici un aperçu du code côté frontend et backend.

\textbf{Frontend}

Le composant Boundaries.js permet d'ajouter, modifier et supprimer des limites de notes.
\begin{minted}[mathescape, linenos]{javascript}
// Formulaire d'ajout de limite de note
<div className="modal">
  <div className="modal-content">
    <select name="classId" value={newBoundary.classId} onChange={handleBoundaryChange}>
      <option value="">Select a class</option>
      {classes.map(classItem => (
        <option key={classItem.class_id} value={classItem.class_id}>
          {classItem.class_name}
        </option>
      ))}
    </select>
    <input type="number" name="overValue" value={newBoundary.overValue} onChange={handleBoundaryChange} placeholder="Over Value" />
    {newBoundary.grades.map((grade, index) => (
      <div key={index}>
        {/* Champs pour les notes */}
      </div>
    ))}
    <button onClick={handleSubmit}>Submit</button>
  </div>
</div>
\end{minted}
\textbf{Backend}

Le contrôleur boundariesController.js gère les opérations CRUD sur les limites de notes.
\begin{minted}[mathescape, linenos]{javascript}
exports.addBoundary = async (req, res) => {
    const { classId, overValue, grades } = req.body;
    try {
        const [result] = await db.execute(
            `INSERT INTO GradeBoundaries (class_id, over_value, grades) VALUES (?, ?, ?)`,
            [classId, overValue, JSON.stringify(grades)]
        );
        res.status(201).json({ message: "Grade boundary added successfully", boundaryId: result.insertId });
    } catch (error) {
        res.status(500).json({ message: error.message });
    }
};

exports.updateBoundary = async (req, res) => {
    // Logique de mise à jour de limite de note
};

exports.deleteBoundary = async (req, res) => {
    // Logique de suppression de limite de note
};

exports.getBoundariesByTeacher = async (req, res) => {
    // Logique de récupération des limites de notes par enseignant
};
\end{minted}
Dans cet exemple, la méthode addBoundary insère une nouvelle limite de note dans la table GradeBoundaries. Les notes sont stockées sous forme de chaîne JSON dans la colonne grades. Lors de la récupération des limites de notes, les notes sont parsées à partir de la chaîne JSON pour être utilisées côté frontend.

\section*{Gestion des Utilisateurs}
La gestion des utilisateurs est une fonctionnalité clé de votre application. Elle permet d'ajouter, mettre à jour, supprimer et afficher les utilisateurs. Voici un aperçu du code côté frontend et backend.


\textbf{Frontend}

Le composant Users.js affiche une liste des utilisateurs et permet d'ajouter, modifier ou supprimer des utilisateurs.
\begin{minted}[mathescape, linenos]{javascript}
const TableauUtilisateurs = ({ filteredUsers, handleEdit, handleDelete }) => (
  <table {...getTableProps()}>
    <thead>
      {/* Entêtes du tableau */}
    </thead>
    <tbody {...getTableBodyProps()}>
      {filteredUsers.map(user => (
        <tr key={user.user_id}>
          {/* Autres cellules du tableau */}
          <td>
            <div className="action-buttons">
              <button className="edit-button" onClick={() => handleEdit(user)}>Edit</button>
              <button className="delete-button" onClick={() => handleDelete(user.user_id)}>Delete</button>
            </div>
          </td>
        </tr>
      ))}
    </tbody>
  </table>
);

// Composant FormulaireUtilisateur pour le formulaire d'ajout/modification
const FormulaireUtilisateur = ({ modalIsOpen, closeModal, handleSubmit }) => (
  <Modal isOpen={modalIsOpen} onRequestClose={closeModal}>
    <div className="modal-content">
      <form onSubmit={handleSubmit}>
        {/* Champs du formulaire */}
        <button type="submit">Submit</button>
      </form>
    </div>
  </Modal>
);

// Utilisation des composants dans votre application ou page
const App = () => {
  // Logique pour gérer les utilisateurs, l'état du modal, etc.

  return (
    <div>
      <TableauUtilisateurs
        filteredUsers={filteredUsers}
        handleEdit={handleEdit}
        handleDelete={handleDelete}
      />
      <FormulaireUtilisateur
        modalIsOpen={modalIsOpen}
        closeModal={closeModal}
        handleSubmit={handleSubmit}
      />
    </div>
  );
};\end{minted} \textbf{Backend}
Le contrôleur userController.js gère les opérations CRUD (Create, Read, Update, Delete) sur les utilisateurs.
\begin{minted}[mathescape, linenos]{javascript}
exports.addUser = async (req, res) => {
// Logique d'ajout d'utilisateur
};
exports.getUsers = async (req, res) => {
// Logique de récupération des utilisateurs
};
exports.updateUser = async (req, res) => {
// Logique de mise à jour d'utilisateur
};
exports.deleteUser = async (req, res) => {
// Logique de suppression d'utilisateur
};
\end{minted}
