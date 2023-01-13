---
tags : mod cs
---
Created: 2023-01-11

## L'extraction de l'instruction
?

L'unité centrale est chargée de savoir quelle instruction elle doit prendre dans la
mémoire primaire pour pouvoir fonctionner correctement.

Pour ce faire, il envoie l'adresse appropriée à la mémoire primaire via le bus de
mémoire (MAR).

L'instruction qui réside dans l'adresse spécifique est ensuite copiée dans le bus
de données et envoyée à l'unité de commande(CU) dans sa mémoire
temporaire (registres).

![[image-20230111153226991.png]]

![[image-20230111153247249.png]]

