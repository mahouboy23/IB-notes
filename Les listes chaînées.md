---
tags : mod cs
---
Created: 2024-01-11

## Caractéristiques d'une structure de données dynamique
Structure de données statique vs Structure de données dynamique
?
![[image-20240111154853062.png]]

#### La notion de nœud 
En programmation, un **nœud** :: est une unité de base (objet) qui contient à la fois des données et un pointeur

#### Characteristique
Pour parcourir une liste chaînée, on commence par le premier nœud et on va de nœud en nœud, en suivant le pointeur de chaque nœud pour trouver le nœud suivant. 
Un nœud ayant une valeur spécifique peut être trouvé en parcourant la liste. 
Une fois trouvé, il est possible d'accéder aux données du nœud. 
Une liste chaînée est constituée d'une séquence de nœuds. 
Chaque nœud contient des données et un pointeur 
Une liste chaînée peut être vide. 
La longueur d'une liste chaînée est le nombre d'éléments qu'elle contient. 
Le dernier nœud contient un pointeur nul. 
Le successeur d'un nœud est le nœud suivant. 
Le prédécesseur d'un nœud est le nœud précédent. 
On accède à une liste chaînée en conservant un pointeur sur le premier nœud de la liste. 
Ce pointeur sur le premier nœud d'une liste est généralement appelé :: **head**.

## Fonctionnement logique des listes chaînées
**Une liste chaînée** :: est une structure de données dynamique simple construite à partir d'une série de nœuds. Chaque nœud de la liste est un objet distinct qui contient à la fois des données et une référence (pointeur) au nœud suivant.
![[image-20240111155508527.png]]

