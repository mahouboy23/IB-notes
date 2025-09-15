---
tags : mod cs
---
Created: 2024-01-18

**Nœuds enfants** :: Les nœuds situés sous un nœud donné sont ses nœuds enfants. 
**Clé** :: Il s'agit d'un champ de données d'un nœud, qui peut être utilisé pour rechercher le nœud ou effectuer d'autres opérations sur celui-ci. 
**Feuille** :: Un nœud qui n'a pas d'enfant est appelé feuille. 
**Niveau** :: Le niveau d'un nœud particulier correspond au nombre de générations du nœud à partir de la racine. Si nous supposons que la racine est de niveau 1, ses enfants seront de niveau 2, ses petits-enfants de niveau 3, etc.

**Hauteur** :: Nombre d'arêtes entre le nœud supérieur et la feuille la plus profonde (c'est-à-dire la plus éloignée). 
**Parent** :: Tous les nœuds, à l'exception de la racine, qui n'a pas de nœud parent, ont exactement une arête ascendante vers leur nœud parent. 
**Chemin** :: Supposons que l'on veuille se déplacer, de nœud en nœud, le long des arêtes qui les relient. La séquence de nœuds parcourus est appelée chemin. 
**Racine** :: Le nœud situé au sommet de l'arbre est appelé la racine.

Parcourir un arbre signifie visiter chaque nœud dans un ordre précis. Il existe trois façons d'implémenter le parcours d'un arbre :: infixe, préfixe et suffixe.

**Préfixe** : Traiter le nœud, visiter le nœud gauche, visiter le nœud droit. 
Infixe : Visite du nœud gauche, traitement du nœud, visite du nœud droit. 
**Suffixe** : Visite du nœud gauche, visite du nœud droit, traitement du nœud.

# English 
# Tree Terminology and Traversal

## Key Terms
- **Child Nodes** :: The nodes located below a given node are its child nodes.  
- **Key** :: A data field of a node that can be used to search for the node or perform other operations on it.  
- **Leaf** :: A node that has no children is called a leaf.  
- **Level** :: The level of a node corresponds to the number of generations from the root.  
  - If the root is at level 1, its children are at level 2, grandchildren at level 3, and so on.  
- **Height** :: The number of edges between the top node and the deepest (farthest) leaf.  
- **Parent** :: Every node (except the root) has exactly one upward edge pointing to its parent node. 
- **Path** :: The sequence of nodes visited when moving from node to node along connecting edges.  
- **Root** :: The node at the top of the tree is called the root.  

## Tree Traversal
Traversing a tree means visiting each node in a specific order.  
There are three common ways to implement tree traversal: **in-order**, **pre-order**, and **post-order**.  

- **Pre-order (Prefix)**: Process the node → visit left child → visit right child.  
- **In-order (Infix)**: Visit left child → process the node → visit right child.  
- **Post-order (Suffix)**: Visit left child → visit right child → process the node.  
