---
tags : mod cs
---
Created: 2023-01-11

## Le décodage est appelé
?
Une fois que l'instruction a été extraite, l'unité centrale doit comprendre
l'instruction pour l'exécuter.

L'instruction qui a été reçue par l'UC est alors décodée.
Le décodage d'une instruction permet à l'UC de prendre connaissance de
toutes les données supplémentaires nécessaires à l'exécution de l'instruction.
Toutes les données requises qui doivent être chargées à partir de la mémoire
primaire pour que l'instruction soit exécutable sont alors récupérées.

Les adresses de ces données sont placées sur le bus (d'adresses MAR) de la
mémoire et les données de ces adresses sont reçues par l'unité centrale par le
biais du bus de données (MDR).