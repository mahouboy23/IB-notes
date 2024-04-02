---
tags : mod cs
---
Created: 2024-04-02

## Login Functionality

plaintext

`Bienvenue sur l'application de gestion des notes IB; si (l'utilisateur tente de se connecter) {   envoyer les informations de connexion au serveur;   si (la réponse du serveur est OK) {     connecter l'utilisateur;   } sinon {     afficher le message d'erreur;   } }`

## Viewing Classes as a Student

plaintext

`si (l'utilisateur est connecté en tant qu'étudiant) {   récupérer la liste des classes de l'étudiant;   afficher les classes de l'étudiant; }`

## Viewing Grades as a Student

plaintext

`si (l'utilisateur est connecté en tant qu'étudiant) {   récupérer la liste des classes de l'étudiant;   si (une classe est sélectionnée) {     récupérer les notes pour la classe sélectionnée;     afficher les notes de l'étudiant pour la classe sélectionnée;   } }`

## Managing Users as a Coordinator

plaintext

`si (l'utilisateur est connecté en tant que coordinateur) {   récupérer la liste des utilisateurs;   si (l'utilisateur sélectionne 'Ajouter un nouvel utilisateur') {     ouvrir le formulaire d'ajout d'utilisateur;     si (le formulaire est soumis) {       ajouter le nouvel utilisateur;     }   } sinon si (l'utilisateur sélectionne 'Modifier') {     ouvrir le formulaire de modification d'utilisateur;     si (le formulaire est soumis) {       mettre à jour les informations de l'utilisateur;     }   } sinon si (l'utilisateur sélectionne 'Supprimer') {     supprimer l'utilisateur;   } }`

## Managing Classes as a Coordinator

plaintext

`si (l'utilisateur est connecté en tant que coordinateur) {   récupérer la liste des classes;   si (l'utilisateur sélectionne 'Ajouter une nouvelle classe') {     ouvrir le formulaire d'ajout de classe;     si (le formulaire est soumis) {       ajouter la nouvelle classe;     }   } sinon si (l'utilisateur sélectionne 'Modifier') {     ouvrir le formulaire de modification de classe;     si (le formulaire est soumis) {       mettre à jour les informations de la classe;     }   } sinon si (l'utilisateur sélectionne 'Supprimer') {     supprimer la classe;   } sinon si (l'utilisateur sélectionne 'Assigner un étudiant') {     ouvrir le formulaire d'assignation d'étudiant;     si (un étudiant est sélectionné) {       assigner l'étudiant à la classe;     }   } }`

## Managing Grade Boundaries as a Teacher

plaintext

`si (l'utilisateur est connecté en tant qu'enseignant) {   récupérer les limites de notes;   si (l'utilisateur sélectionne 'Ajouter une nouvelle limite') {     ouvrir le formulaire d'ajout de limite de notes;     si (le formulaire est soumis) {       ajouter la nouvelle limite de notes;     }   } sinon si (l'utilisateur sélectionne 'Modifier') {     ouvrir le formulaire de modification de limite de notes;     si (le formulaire est soumis) {       mettre à jour la limite de notes;     }   } sinon si (l'utilisateur sélectionne 'Supprimer') {     supprimer la limite de notes;   } }`