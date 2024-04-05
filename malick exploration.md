---
tags : mod cs
---
Created: 2024-04-05

## Fichier `app.py`

Ce fichier est le cœur de l'application Flask. Il définit la structure de l'application, les modèles de données, et les routes pour gérer les requêtes HTTP.

- **Initialisation de l'application et configuration**: Au début, l'application Flask est initialisée et configurée pour utiliser une base de données SQLite et pour ne pas suivre les modifications des objets retournés par la base de données (pour des raisons de performance).
- **Définition du modèle `Tache`**: Le modèle `Tache` est défini en utilisant SQLAlchemy, un ORM (Object-Relational Mapping) qui permet de manipuler la base de données à l'aide d'objets Python. Ce modèle définit la structure de la table `tache` dans la base de données, avec des champs pour l'ID, le titre, la description, la date d'échéance, la priorité, et le statut de la tâche.
- **Routes de l'application**: Plusieurs routes sont définies pour gérer les différentes fonctionnalités de l'application, telles que l'affichage des tâches (`/`), l'ajout d'une nouvelle tâche (`/ajouter_tache`), la mise à jour d'une tâche existante (`/mettre_a_jour_tache/<int:id_tache>`), la suppression d'une tâche (`/supprimer_tache/<int:id_tache>`), et la récupération des événements pour le calendrier (`/evenements_calendrier`).

## Fichier `index.html`

Ce fichier est un template HTML qui utilise Jinja2, un moteur de template pour Python, pour générer dynamiquement le contenu HTML en fonction des données fournies par le serveur Flask. Il inclut des formulaires pour ajouter et filtrer les tâches, ainsi qu'un tableau pour afficher les tâches existantes. Il utilise Bootstrap pour le style et FullCalendar pour afficher un calendrier des tâches.

## Fichier `calendar.js`

Ce fichier JavaScript est utilisé pour initialiser et configurer le calendrier FullCalendar dans le navigateur de l'utilisateur. Il définit la source des événements du calendrier comme étant la route `/calendar_events` de l'application Flask, permettant ainsi d'afficher les tâches comme des événements dans le calendrier.

## Base de données

La base de données est gérée par SQLite et SQLAlchemy. SQLite est un système de gestion de base de données relationnelle léger qui stocke la base de données dans un fichier sur le disque. SQLAlchemy est utilisé pour définir les modèles de données et interagir avec la base de données à l'aide de Python, sans avoir à écrire de SQL brut. Les interactions avec la base de données incluent l'ajout, la mise à jour, la suppression, et la récupération des tâches.

## Communication entre les composants

1. **Client et Serveur**: Lorsqu'un utilisateur interagit avec l'interface web (par exemple, en ajoutant une nouvelle tâche), une requête HTTP est envoyée au serveur Flask. Flask traite la requête en fonction de la route correspondante et interagit avec la base de données si nécessaire.
2. **Serveur et Base de données**: Flask utilise SQLAlchemy pour interagir avec la base de données. Par exemple, lors de l'ajout d'une nouvelle tâche, un objet `Tache` est créé et ajouté à la base de données.
3. **Serveur et Client (réponse)**: Flask renvoie une réponse au client, qui peut être une page HTML mise à jour (générée à partir du template `index.html`), une redirection vers une autre route, ou des données JSON (dans le cas de requêtes AJAX faites par `calendar.js`).

## explication app.py :
1-5: Importation des modules nécessaires pour l'application.

```python
from flask import Flask, render_template, request, redirect, jsonify from flask_sqlalchemy import SQLAlchemy from datetime import datetime, date from flask_migrate import Migrate
```

7-10: Configuration de l'application Flask.
- `app = Flask(__name__, static_url_path='', static_folder='static')` crée une instance de l'application Flask en spécifiant le chemin et le dossier des fichiers statiques.
- `app.config['SECRET_KEY'] = 'votre_cle_secrete_ici'` définit une clé secrète pour l'application, utilisée pour signer les données sensibles.
- `app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///gestionnaire_taches.db'` configure l'URI de la base de données SQLite.
- `app.config['SQLALCHEMY_TRACK_MODIFICATIONS'] = False` désactive le suivi des modifications de SQLAlchemy pour économiser des ressources.
```python
`app = Flask(__name__, static_url_path='', static_folder='static') app.config['SECRET_KEY'] = 'votre_cle_secrete_ici' app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///gestionnaire_taches.db' app.config['SQLALCHEMY_TRACK_MODIFICATIONS'] = False`
```

12-13: Création d'instances de SQLAlchemy et Flask-Migrate pour gérer la base de données.
- `db = SQLAlchemy(app)` crée une instance de SQLAlchemy liée à l'application Flask.
- `migrate = Migrate(app, db)` crée une instance de Flask-Migrate pour gérer les migrations de la base de données.
```python
`db = SQLAlchemy(app) migrate = Migrate(app, db)`
```


15-22: Définition du modèle de données `Tache` qui représente une tâche dans la base de données.
- Chaque attribut de la classe `Tache` correspond à une colonne dans la table de la base de données.
- Les attributs sont définis à l'aide de `db.Column()` en spécifiant le type de données et les contraintes (par exemple, `primary_key=True`, `nullable=False`).
```python
`class Tache(db.Model):     
id = db.Column(db.Integer, primary_key=True)     
titre = db.Column(db.String(100), nullable=False)     
description = db.Column(db.Text, nullable=True)     
date_echeance = db.Column(db.DateTime, nullable=True)    
priorite = db.Column(db.Integer, nullable=False, default=1)     
statut = db.Column(db.String(10), nullable=False, default='En Attente')`
```

25-37: Définition de la route principale `/` qui gère les requêtes GET et POST.
- `date_selectionnee = request.args.get('date_echeance_tache') or date.today().isoformat()` récupère la date sélectionnée à partir des paramètres de requête ou utilise la date du jour si aucune date n'est spécifiée.
- `filtre_statut = request.args.get('statut', 'tous')` récupère le filtre de statut à partir des paramètres de requête ou utilise 'tous' par défaut.
- `requete = Tache.query.filter(db.func.date(Tache.date_echeance) == date_selectionnee)` crée une requête de base pour filtrer les tâches par date d'échéance.
- `if filtre_statut in ['Terminé', 'En Attente', 'Non Commencé']: requete = requete.filter(Tache.statut == filtre_statut)` filtre davantage la requête en fonction du statut sélectionné, si celui-ci est spécifié.
- `taches_prevues = requete.all()` récupère toutes les tâches correspondant à la requête.
- `return render_template('index.html', taches_prevues=taches_prevues, date_selectionnee=date_selectionnee, filtre_statut=filtre_statut)` renvoie le template HTML 'index.html' en passant les tâches prévues, la date sélectionnée et le filtre de statut en tant que variables.
```python

`@app.route('/', methods=['GET', 'POST']) def index():     
date_selectionnee = request.args.get('date_echeance_tache') or date.today().isoformat()     filtre_statut = request.args.get('statut', 'tous')          
requete = Tache.query.filter(db.func.date(Tache.date_echeance) == date_selectionnee)          if filtre_statut in ['Terminé', 'En Attente', 'Non Commencé']:         
requete = requete.filter(Tache.statut == filtre_statut)          
taches_prevues = requete.all()     
return render_template('index.html', taches_prevues=taches_prevues, date_selectionnee=date_selectionnee, filtre_statut=filtre_statut)`
```


40-52: Définition de la route `/ajouter_tache` qui gère l'ajout d'une nouvelle tâche.
- Les données de la nouvelle tâche sont récupérées à partir du formulaire soumis via `request.form`.
- `nouvelle_tache = Tache(titre=titre, description=description, date_echeance=date_echeance, statut=statut, priorite=priorite)` crée une nouvelle instance de `Tache` avec les données fournies.
- `db.session.add(nouvelle_tache)` ajoute la nouvelle tâche à la session de base de données.
- `db.session.commit()` enregistre les modifications dans la base de données.
- `return redirect('/')` redirige l'utilisateur vers la page principale après l'ajout de la tâche.
```python

`@app.route('/ajouter_tache', methods=['POST']) def ajouter_tache():     
titre = request.form['titre']     
description = request.form['description']     
date_echeance = datetime.strptime(request.form['date_echeance'], '%Y-%m-%d')     
statut = request.form.get('statut', 'Non Commencé')     
priorite = int(request.form.get('priorite', 1))     
nouvelle_tache = Tache(titre=titre, description=description, date_echeance=date_echeance, statut=statut, priorite=priorite)     db.session.add(nouvelle_tache)    
db.session.commit()     
return redirect('/')`
```

55-66: Définition de la route `/mettre_a_jour_tache/<int:id_tache>` qui gère la mise à jour d'une tâche existante.
- `tache = Tache.query.get(id_tache)` récupère la tâche correspondant à l'ID fourni.
- Si la tâche existe, les attributs de la tâche sont mis à jour avec les données du formulaire soumis via `request.form.get()`.
- `db.session.commit()` enregistre les modifications dans la base de données.
- `return jsonify({'message': 'Tache mise à jour avec succès'}), 200` renvoie un message JSON de succès avec un code de statut HTTP 200.
- Si la tâche n'est pas trouvée, `return jsonify({'message': 'Tache non trouvée'}), 404` renvoie un message JSON d'erreur avec un code de statut HTTP 404.
```python
`@app.route('/mettre_a_jour_tache/<int:id_tache>', methods=['POST']) 
def mettre_a_jour_tache(id_tache):     
tache = Tache.query.get(id_tache)     
if tache:         
tache.titre = request.form.get('titre', tache.titre)         
tache.description = request.form.get('description', tache.description)         tache.date_echeance = datetime.strptime(request.form.get('date_echeance'), '%Y-%m-%d') if request.form.get('date_echeance') else tache.date_echeance         
tache.statut = request.form.get('statut', tache.statut)         
tache.priorite = int(request.form.get('priorite', tache.priorite))         db.session.commit()        
return jsonify({'message': 'Tache mise à jour avec succès'}), 200     else:         return jsonify({'message': 'Tache non trouvée'}), 404`
```

69-77: Définition de la route `/supprimer_tache/<int:id_tache>` qui gère la suppression d'une tâche.
- `tache = Tache.query.get(id_tache)` récupère la tâche correspondant à l'ID fourni.
- Si la tâche existe, `db.session.delete(tache)` supprime la tâche de la session de base de données.
- `db.session.commit()` enregistre les modifications dans la base de données.
- `return jsonify({'message': 'Tache supprimée avec succès'}), 200` renvoie un message JSON de succès avec un code de statut HTTP 200.
- Si la tâche n'est pas trouvée, `return jsonify({'message': 'Tache non trouvée'}), 404` renvoie un message JSON d'erreur avec un code de statut HTTP 404.
```python

@app.route('/supprimer_tache/<int:id_tache>', 
methods=['DELETE']) def supprimer_tache(id_tache):     
tache = Tache.query.get(id_tache)     
if tache:         
db.session.delete(tache)         
db.session.commit()         
return jsonify({'message': 'Tache supprimée avec succès'}), 200     
return jsonify({'message': 'Tache non trouvée'}), 404`
```


80-89: Définition de la route `/evenements_calendrier` qui renvoie les tâches sous forme d'événements JSON pour le calendrier.
- `taches = Tache.query.all()` récupère toutes les tâches de la base de données.
- La boucle `for` parcourt chaque tâche et, si la tâche a une date d'échéance, ajoute un dictionnaire représentant l'événement à la liste `evenements`.
- Chaque événement contient le titre de la tâche et la date d'échéance formatée en tant que date de début.
- `return jsonify(evenements)` renvoie la liste des événements sous forme de réponse JSON.
```python
`@app.route('/evenements_calendrier') 
def evenements_calendrier():     
taches = Tache.query.all()     
evenements = []     
for tache in taches:         
if tache.date_echeance:             
evenements.append({                 
				   'titre': tache.titre,                 
				   'debut': tache.date_echeance.strftime('%Y-%m-%d'),             
				   })     
return jsonify(evenements)`
```

92: Démarrage de l'application Flask en mode débogage si le script est exécuté directement.

```python
if __name__ == '__main__':     app.run(debug=True)`
```

Ce fichier app.py contient donc la logique principale de l'application, y compris la configuration, la définition du modèle de données, les routes pour les différentes actions (affichage, ajout, mise à jour, suppression de tâches) et la route pour récupérer les événements du calendrier.

## Explication index.html :

1-13: Configuration de l'en-tête HTML, y compris les métadonnées, le titre et les liens vers les fichiers CSS et JavaScript nécessaires.

```html
<!DOCTYPE html> 
<html lang="fr"> 
<head>     
 <meta charset="UTF-8">     
 <meta name="viewport" content="width=device-width, initial-scale=1.0">              <title>Gestionnaire de Tâches</title>     
 <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">      <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/fullcalendar@3.10.2/dist/fullcalendar.min.css" />     <script src="https://code.jquery.com/jquery-3.5.1.min.js"></script>     <script src="https://cdn.jsdelivr.net/npm/fullcalendar@3.10.2/dist/fullcalendar.min.js"></script>     <script src="/static/calendar.js"></script>  </head>`
```

16-48: Formulaire pour ajouter une nouvelle tâche, avec des champs pour le titre, la description, la date d'échéance, le statut et la priorité.

```html
<div class="mt-4">     
<h3>Ajouter une Nouvelle Tâche</h3>     
<form action="/ajouter_tache" method="POST">         
<div class="form-group">             
<label for="tacheTitre">Titre</label>             
<input type="text" class="form-control" id="tacheTitre" name="titre" required>         </div>         
<div class="form-group">             
<label for="tacheDescription">Description</label>             
<textarea class="form-control" id="tacheDescription" name="description" rows="3"></textarea>         
</div>         
<div class="form-group">             
<label for="tacheDate">Date</label>             
<input type="date" class="form-control" id="tacheDate" name="date_echeance" required>   </div>         
<div class="form-group">             
<label for="tachestatut">Statut</label>             
<select class="form-control" id="tachestatut" name="statut">                 
<option value="non_commence" selected>Non Commencé</option>                 
<option value="En Attente">En Attente</option>                 
<option value="Terminé">Terminé</option>             
</select>         
</div>         
<div class="form-group">             
<label for="tachePriority">Priorité</label>             
<select class="form-control" id="tachePriority" name="priorite">                 <option value="1" selected>Pas Important</option>                 
<option value="2">Important</option>                 
<option value="3">Très Important</option>             
</select>         
</div>         
<button type="submit" class="btn btn-primary">Ajouter Tâche</button>     
</form>         
</div>
```

51: Emplacement où le calendrier sera rendu.

```html
<div id="calendar" class="mt-5"></div>
```

54-98: Tableau des tâches prévues, filtré par date et statut. Il affiche les détails de chaque tâche et permet de les modifier ou de les supprimer.

```html
<div class="mt-5">     
<h2>Tâches Prévues</h2>     
<form method="GET">         
<input type="date" id="date_echeance_tache" name="date_echeance_tache" value="{{ date_selectionnee }}">         
<select name="statut" id="filtreStatut">             
<option value="tous" {{ 'selected' if filtre_statut == 'tous' }}>Tous</option>             <option value="Non Commencé" {{ 'selected' if filtre_statut == 'Non Commencé' }}>Non Commencé</option>             
<option value="En Attente" {{ 'selected' if filtre_statut == 'En Attente' }}>En Attente</option>             
<option value="Terminé" {{ 'selected' if filtre_statut == 'Terminé' }}>Terminé</option>         </select>         
<button type="submit" class="btn btn-primary">Afficher les Tâches</button>     </form>     <table class="table" id="tachesDueTable">         
<thead>             
<tr>                 
<th>Titre</th>                 
<th>Description</th>                 
<th>Date d'Échéance</th>                 
<th>Statut</th>                 
<th>Priorité</th>                 
<th>Actions</th>             
</tr>         
</thead>         
<tbody>             
{% for tache in taches_prevues %}             
<tr class="{{ 'table-success' if tache.statut == 'Terminé' else 'table-secondary' if tache.statut == 'En Attente' else 'table-danger' }}">                 
<td>                     
<input type="text" class="form-control" value="{{ tache.titre }}" onchange="updateTache({{ tache.id }}, 'titre', this.value)">                 
</td>                 
<td>                     
<textarea class="form-control" onchange="updateTache({{ tache.id }}, 'description', this.value)">{{ tache.description }}</textarea>                 
</td>                 
<td>                     
<input type="date" class="form-control" value="{{ tache.date_echeance.strftime('%Y-%m-%d') }}" onchange="updateTache({{ tache.id }}, 'date_echeance', this.value)">         
</td>                 
<td>                     
<select class="form-control" onchange="updateTache({{ tache.id }}, 'statut', this.value)">                         
<option value="Non Commencé" {{ 'selected' if tache.statut == 'Non Commencé' }}>Non Commencé</option>                         
<option value="En Attente" {{ 'selected' if tache.statut == 'En Attente' }}>En Attente</option>                         
<option value="Terminé" {{ 'selected' if tache.statut == 'Terminé' }}>Terminé</option>                     </select>                 
</td>                 
<td>                     
<select class="form-control" onchange="updateTache({{ tache.id }}, 'priorite', this.value)">                         
<option value="1" {{ 'selected' if tache.priorite == 1 }}>Pas Important</option>                         <option value="2" {{ 'selected' if tache.priorite == 2 }}>Important</option>                         
<option value="3" {{ 'selected' if tache.priorite == 3 }}>Très Important</option>                     </select>                 
</td>                 
<td>                     
<button class="btn btn-danger" onclick="supprimer_tache({{ tache.id }})">Supprimer</button>                 
</td>             
</tr>             
{% endfor %}         
</tbody>     
</table> 
</div>
```

100-129: Scripts JavaScript pour gérer la mise à jour et la suppression des tâches via des requêtes fetch vers les routes Flask correspondantes.

html

```html
<script>     
function updateTache(tacheId, field, value) {         
const formData = new FormData();         
formData.append(field, value);              
fetch(`/mettre_a_jour_tache/${tacheId}`, {             
method: 'POST',             
body: formData         
}).then(response => response.json())         
.then(data => {             
if (data.message) {                 
console.log(data.message);                 
location.reload();            
}         
})         
.catch(error => console.error('Erreur lors de la mise à jour de la tâche:', error));     }          
function supprimer_tache(tacheId) {         
fetch(`/supprimer_tache/${tacheId}`, {             
method: 'DELETE'         
}).then(response => response.json())         
.then(data => {             
console.log(data);             
location.reload();         
})         
.catch(error => console.error('Erreur lors de la suppression de la tâche:', error));     }     
</script>
```

Ce fichier index.html contient la structure et le contenu de la page principale de l'application. Il inclut un formulaire pour ajouter de nouvelles tâches, un emplacement pour afficher le calendrier et un tableau pour afficher et gérer les tâches prévues. Les scripts JavaScript gèrent les interactions utilisateur, telles que la mise à jour et la suppression des tâches, en communiquant avec le backend Flask via des requêtes fetch.

## Explication calendar.js :

1-11: Configuration et initialisation du calendrier FullCalendar.
```javascript
document.addEventListener('DOMContentLoaded', function() {     
var calendarEl = document.getElementById('calendar');     
var calendar = new FullCalendar.Calendar(calendarEl, {         
});     
calendar.render(); });
```
``
- L'écouteur d'événement `DOMContentLoaded` s'assure que le code s'exécute une fois que le DOM est complètement chargé.
- `var calendarEl = document.getElementById('calendar');` récupère l'élément HTML avec l'ID 'calendar', qui servira de conteneur pour le calendrier.
- `var calendar = new FullCalendar.Calendar(calendarEl, {...});` crée une nouvelle instance du calendrier FullCalendar en passant l'élément de conteneur et un objet de configuration.
- `calendar.render();` rend le calendrier dans le conteneur spécifié.

3-7: Configuration de la barre d'outils d'en-tête du calendrier.

```javascript
headerToolbar: {     left: 'prev,next today',     center: 'title',     right: 'dayGridMonth,timeGridWeek,timeGridDay' },

- `left: 'prev,next today'` affiche les boutons de navigation "précédent", "suivant" et "aujourd'hui" à gauche de la barre d'outils.
- `center: 'title'` affiche le titre du calendrier au centre de la barre d'outils.
- `right: 'dayGridMonth,timeGridWeek,timeGridDay'` affiche les boutons de sélection de vue "mois", "semaine" et "jour" à droite de la barre d'outils.
```

8: Définition de la vue initiale du calendrier.

```javascript
initialView: 'dayGridMonth',
```

- `initialView: 'dayGridMonth'` définit la vue par défaut du calendrier sur la vue mensuelle.

9: Configuration de la source d'événements pour le calendrier.

```javascript
events: '/evenements_calendrier',
```

- `events: '/evenements_calendrier'` indique au calendrier de récupérer les événements à partir de la route Flask '/evenements_calendrier', qui doit renvoyer des données JSON représentant les tâches.

Ce fichier calendar.js est responsable de la configuration et de l'initialisation du calendrier FullCalendar. Il définit la disposition de la barre d'outils d'en-tête, la vue initiale et la source des événements du calendrier. Le calendrier s'attend à ce que la route Flask '/evenements_calendrier' renvoie des données JSON représentant les tâches, qui seront ensuite affichées en tant qu'événements dans le calendrier.La bibliothèque FullCalendar fournit une interface utilisateur riche et interactive pour afficher et gérer les événements du calendrier. Elle offre des fonctionnalités telles que la navigation entre les vues (mois, semaine, jour), l'affichage des détails des événements et la possibilité de personnaliser l'apparence du calendrier.