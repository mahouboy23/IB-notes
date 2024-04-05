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

@app.route('/supprimer_tache/<int:id_tache>', methods=['DELETE']) def supprimer_tache(id_tache):     tache = Tache.query.get(id_tache)     if tache:         db.session.delete(tache)         db.session.commit()         return jsonify({'message': 'Tache supprimée avec succès'}), 200     return jsonify({'message': 'Tache non trouvée'}), 404`
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

Ce fichier app.py contient donc la logique principale de l'application, y compris la configuration, la définition du modèle de données, les routes pour les différentes actions (affichage, ajout, mise à jour, suppression de tâches) et la route pour récupérer les événements du calendrier1.