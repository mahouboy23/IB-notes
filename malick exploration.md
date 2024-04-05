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

```python

```