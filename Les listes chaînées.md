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

## Représentation graphique de listes chaînées

**Listes chaînées linéaires**
?
La liste chaînée de base se compose d'un ensemble de nœuds. Chaque nœud comporte deux éléments : une valeur de données et un pointeur vers le nœud suivant.
- Tête unique, queue unique (premier et dernier élément) 
- Chaque pointeur fonctionne dans une seule direction
![[image-20240111160817534.png]]

**Listes doublement chaînées**
?
Une liste doublement chaînée contient deux pointeurs par nœud, un pour le nœud suivant et un pour le nœud précédent.
- Tête unique, queue unique (premier et dernier élément) 
- Deux pointeurs pour chaque élément (un vers le suivant, un vers le précédent)
![[image-20240111161051443.png]]


**Listes chaînées circulaires**
?
Une liste chaînée circulaire forme une boucle infinie dans sa chaîne en faisant pointer la valeur "next" du dernier nœud sur le premier élément de la liste. 
- Tête unique Un pointeur pour chaque élément (un pour l'élément suivant) 
- Le pointeur du dernier élément pointe vers la tête (créant un cercle)
  ![[image-20240111161153202.png]]

# English 
# Linked Lists (Dynamic Data Structures)

## Static vs Dynamic Data Structures
![[image-20240111154853062.png]]

---

## The Concept of a Node
In programming, a **node** is a basic unit (object) that contains both **data** and a **pointer**.  

### Characteristics
- To traverse a linked list, start from the first node and follow each node’s pointer to the next.  
- A node with a specific value can be found by traversal.  
- Once found, the node’s data can be accessed.  
- A linked list is made of a sequence of nodes.  
- Each node contains data and a pointer.  
- A linked list can be empty.  
- The length of a linked list = number of elements it contains.  
- The last node contains a **null pointer**.  
- The successor of a node = the next node.  
- The predecessor of a node = the previous node.  
- Access to a linked list is via a pointer to the **first node**.  
- This pointer is generally called the **head**.  

---

## Logical Operation of Linked Lists
A **linked list** is a dynamic data structure built from a sequence of nodes.  
Each node contains both data and a reference (pointer) to the next node.  

![[image-20240111155508527.png]]

---

## Insertion in a Linked List
There are three main cases:  
1. Insert a new node at the **beginning**.  
2. Insert a new node at the **end**.  
3. Insert a new node in the **middle** (between two nodes).  

### Insert into an Empty List
- If the list is empty (`head = NULL`), insertion is simple:  
  - The algorithm sets both the **head** and **tail** to point to the new node.  
![[image-20240111160052689.png]]

### Insert at the Beginning
- The new node is placed before the current head.  
- Update the new node’s pointer to point to the current head.  
- Update the head to point to the new node.  
![[image-20240111160136941.png]]

### Insert at the End
- The new node is placed after the current tail.  
- Update the tail’s pointer to point to the new node.  
- Update the tail to the new node.  
![[image-20240111160224689.png]]

### Insert in the Middle
- The new node is inserted between two existing nodes.  
- Update the predecessor’s pointer to point to the new node.  
- Update the new node’s pointer to point to the successor.  
- The head and tail pointers remain unchanged.  
![[image-20240111160403165.png]]

---

## Types of Linked Lists

### Linear Linked List
- Basic form: nodes connected in a single direction.  
- Each node has: data + pointer to the next node.  
- Single **head** and **tail** (first and last elements).  
- Pointers move in one direction only.  
![[image-20240111160817534.png]]

### Doubly Linked List
- Each node has **two pointers**: one to the next node, one to the previous node.  
- Single **head** and **tail**.  
![[image-20240111161051443.png]]

### Circular Linked List
- The last node points back to the **head**, forming a loop.  
- Single **head**, each node has one pointer to the next node.  
- Last node → head (circular structure).  
![[image-20240111161153202.png]]
