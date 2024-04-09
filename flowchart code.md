---
tags : mod cs
---
Created: 2024-04-02
use plantuml to make the diagrams, give me the complete plantuml code for the flowchart diagrams and use the plantuml Sequence Diagram and syntax to respect the norms of a computer science flowchart, use the plantuml documentation to fully is it's capabilities
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

flowchart TB A[Coordinateur accède à la page de gestion des utilisateurs] --> B{La liste des utilisateurs est-elle vide ?} B -->|Oui| C[Afficher un message indiquant qu'aucun utilisateur n'est disponible] B -->|Non| D[Afficher la liste des utilisateurs] D --> E{Le coordinateur souhaite-t-il ajouter un nouvel utilisateur ?} E -->|Oui| F[Ouvrir le formulaire d'ajout d'utilisateur] F --> G[Saisir les informations de l'utilisateur] G --> H{Les informations sont-elles valides ?} H -->|Non| I[Afficher un message d'erreur] I --> G H -->|Oui| J[Soumettre le formulaire] J --> K[Envoyer une requête POST à l'API pour ajouter l'utilisateur] K --> L{La requête a-t-elle réussi ?} L -->|Oui| M[Rafraîchir la liste des utilisateurs] L -->|Non| N[Afficher un message d'erreur] M --> D N --> D E -->|Non| O{Le coordinateur souhaite-t-il modifier un utilisateur ?} O -->|Oui| P[Sélectionner l'utilisateur à modifier] P --> Q[Ouvrir le formulaire de modification d'utilisateur] Q --> R[Modifier les informations de l'utilisateur] R --> S{Les informations sont-elles valides ?} S -->|Non| T[Afficher un message d'erreur] T --> R S -->|Oui| U[Soumettre le formulaire] U --> V[Envoyer une requête PUT à l'API pour mettre à jour l'utilisateur] V --> W{La requête a-t-elle réussi ?} W -->|Oui| X[Rafraîchir la liste des utilisateurs] W -->|Non| Y[Afficher un message d'erreur] X --> D Y --> D O -->|Non| Z{Le coordinateur souhaite-t-il supprimer un utilisateur ?} Z -->|Oui| AA[Sélectionner l'utilisateur à supprimer] AA --> AB[Confirmer la suppression] AB --> AC[Envoyer une requête DELETE à l'API pour supprimer l'utilisateur] AC --> AD{La requête a-t-elle réussi ?} AD -->|Oui| AE[Rafraîchir la liste des utilisateurs] AD -->|Non| AF[Afficher un message d'erreur] AE --> D AF --> D Z -->|Non| AG[Le coordinateur termine la gestion des utilisateurs]

## Managing Grade Boundaries as a Teacher

plaintext

flowchart TD
    A[Initialiser] --> B[Vérifier l'enseignant]
    B -->|Oui| C[Obtenir limites existantes]
    C --> D[Obtenir classes enseignant]
    D --> E[Afficher modal]
    E --> F[Sélectionner classe et valeurs]
    F --> G[Entrer les plages de notes]
    G --> H[Envoyer]
    H --> I[Traiter l'ajout]
    I --> J[Actualiser les limites]
    J --> K[Fin]

    B -->|Non| K[Fin]

    F -.->|Ajouter des plages| G
    G -->|Toutes les valeurs saisies?| H
    H -->|Oui| I
    I --> J

    style A fill:#F9F,stroke:#333,stroke-width:2px
    style B fill:#F9F,stroke:#333,stroke-width:2px
    style C fill:#F9F,stroke:#333,stroke-width:2px
    style D fill:#F9F,stroke:#333,stroke-width:2px
    style E fill:#FFF,stroke:#333,stroke-width:2px
    style F fill:#FFF,stroke:#333,stroke-width:2px
    style G fill:#FFF,stroke:#333,stroke-width:2px
    style H fill:#FFF,stroke:#333,stroke-width:2px
    style I fill:#F9F,stroke:#333,stroke-width:2px
    style J fill:#F9F,stroke:#333,stroke-width:2px
    style K fill:#F9F,stroke:#333,stroke-width:2px
