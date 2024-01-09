---
tags : mod cs
---
Created: 2024-01-09

## Les files
Une file d'attente stocke un ensemble d'éléments dans un ordre particulier et n'autorise l'accès qu'au premier élément inséré. Les éléments sont récupérés dans l'ordre dans lequel ils ont été insérés.

La file d'attente est une structure de données FIFO (First-In, FirstOut). Les éléments d'une file d'attente peuvent être des nombres, des valeurs booléennes, des caractères, des objets, des tableaux, etc. 
**Les files utilisent trois méthodes** :: enqueue(), dequeue(), isEmpty()![[image-20240109102443014.png]]

### La fonction enqueue() 
Cette fonction permet d'inserer un élément à la fin de la file :: **enfiler**

### La fonction dequeue() 
Retirer un élément du début de la file d'attente : **défiler**

### La fonction isEmpty() 
?
Tester si la file ne contient aucun élément.

### Cas d’utilisation des files 
- Les files sont utilisées pour modéliser les files d'attente physiques, telles que les personnes faisant la queue à la caisse d'un supermarché. 
- La file d'attente d'impression affiche les documents en attente d'impression. Ces documents suivront la politique du premier envoi, première impression. 
- Lors de l'envoi de données sur l'internet, plusieurs paquets de données attendent dans une file d'attente avant d'être envoyés. 
- Un serveur répond généralement à plusieurs demandes. Dans la plupart des cas, ces demandes sont stockées dans une file d'attente. La procédure de demande est la suivante : premier arrivé, premier servi.