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