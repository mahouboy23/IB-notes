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

### Insertion dans une liste chaînée 
Nous avons trois possibilités : 
?
1. Insertion d'un nouveau nœud au tout début de la liste 
2. Insertion d'un nouveau nœud à la toute fin de la liste 
3. Insertion d'un nouveau nœud au milieu de la liste, qui a donc un prédécesseur et un successeur dans la liste.

#### Insertion dans une liste vide 
Lorsque la liste est vide, ce qui est indiqué par la condition (head =NULL), l'insertion est très simple. L'algorithme fait pointer la tête et la queue sur le nouveau nœud.
![[image-20240111160052689.png]]

#### Insérer au DÉBUT 
Dans ce cas, le nouveau nœud est inséré juste avant le nœud principal actuel. Mettre à jour le pointeur suivant d'un nouveau nœud, afin qu'il pointe vers le nœud principal actuel. Mettre à jour le lien d'en-tête pour qu'il pointe vers le nouveau nœud.
![[image-20240111160136941.png]]

#### Insérer à la FIN 
Dans ce cas, le nouveau nœud est inséré juste après le nœud de queue actuel. Mettre à jour le pointeur suivant du nœud de queue actuel pour qu'il pointe vers le nouveau nœud. Mettre à jour le pointeur de queue pour qu'il pointe vers le nouveau nœud.
![[image-20240111160224689.png]]

#### Insérer au MILIEU 
En général, un nouveau nœud est toujours inséré entre deux nœuds existants. Les pointeurs de tête et de queue ne sont pas mis à jour dans ce cas. Mise à jour du pointeur du nœud "précédent" pour pointer vers le nouveau nœud Mise à jour du pointeur du nouveau nœud, pour pointer vers le nœud "suivant".
![[image-20240111160403165.png]]

