---
tags : mod cs
---
Created: 2024-04-16
description :
ok maintenant je veux continuer ma partit C. Les reponce que tu dois me donner ne dois pas etre par fichier et ou par page sa doit etre part technique ou concept ou fonctionnaliter (comment j'ai fait pour faire cette fonctionnaliter quel technique utiliser). Tu dois me donner tes reponse sur format overleaf et PRENDRE DES SNIPPET de code, apres je vais prendre les screenshot et les remplacer mais je dois savoir quel code du parle ou reference donc inclut les snippet de code que tu utilise. Si on doit montrer un screenshot de quelque chose qui se passe dans l'application mes [screenshot de (description de ce que je dois mettre la)] puis je vais l'ajouter apres. Les variable, parametre, code, fonction ect doit etre one to one et ne traduit pas ces elements mes le reste et explication DOIT etre en francais. Quand on fait une nouvelle parti donne un titre de quelque mots qui exprime bien la technique ou concept ou fonctionnaliter qui represente cette section. Quand tu remarque une technique ou concept ou fonctionnaliter assez complexe ou autre trouve un reference pour sa mais ne le fait pas pour des truc qui allere originel ou qui sont vraiment simple et intuitif. finalement a la fin donne moi un compte des mots que tu a utiliser a la fin qui compte pas les titre, diagram, tableau. Donc on commence sont par :
modélisation de la base de données et configuration du serveur/backend (ce n'est pas le titre choisi un meilleur titre):
- table des donnees creer avec my sql donc montre le code mysql pour creer la table ("")
  - Parle de la connection a la base de donnee et comment sa ete set up (provide code and functionnality)
- Et parle de la configuration du server et l'utilisation de routes et controllers dans node.js on montrer du code
  RESPECTE LE CRITERE ET CONDITION DONNEES PREALABLEMENT

## Modélisation de la base de données avec MySQL

La modélisation de la base de données est une étape cruciale dans le développement d'une application web. Elle permet de définir la structure des données et les relations entre les différentes entités. Dans notre cas, nous avons utilisé MySQL pour créer la base de données de notre application de gestion des notes du programme IB. Voici un extrait du code SQL pour créer la Table Users :

CODE

Chaque table représente une entité spécifique de notre application, comme les utilisateurs, les classes, les notes, les limites de notes et les associations entre les étudiants et les classes.[screenshot de la création des tables dans MySQL Workbench]

## Connexion à la base de données

Pour établir la connexion entre notre application Node.js et la base de données MySQL, nous avons utilisé le module `mysql2`. Voici un extrait du code pour configurer la connexion :

Code

Nous avons créé un pool de connexions pour optimiser les performances et la gestion des ressources. Les informations de connexion sont stockées dans des variables d'environnement pour des raisons de sécurité.

## Configuration du serveur et utilisation des routes et contrôleurs

Pour structurer notre application Node.js, nous avons suivi une architecture basée sur les routes et les contrôleurs. Cette approche permet de séparer les préoccupations et de rendre le code plus modulaire et maintenable.
## Routes

Les routes définissent les différents endpoints de notre API et associent chaque route à un contrôleur spécifique. Voici un exemple de fichier de routes pour la gestion des notes :
CODE
Dans cet exemple, nous définissons les routes pour les opérations CRUD (Create, Read, Update, Delete) sur les notes. Chaque route est associée à une fonction du contrôleur `gradeController`.

## Contrôleurs

Les contrôleurs contiennent la logique métier de notre application. Ils gèrent les requêtes entrantes, interagissent avec la base de données et renvoient les réponses appropriées. Voici un extrait du contrôleur `gradeController` :
CODE
Dans cet exemple, nous avons deux fonctions du contrôleur : `getStudentGrades` pour récupérer les notes d'un étudiant, et `createGrade` pour ajouter une nouvelle note. Ces fonctions interagissent avec la base de données en utilisant des requêtes SQL et renvoient les réponses appropriées.
 
 ### 344


Authentification : 
- Aspect jwt token, parametre du token
- authContext et comment sa marche / integrer dans l'application
- Logic des routes proteger et re-directement vers les dashboard correct 
  
  
