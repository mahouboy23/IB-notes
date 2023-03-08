---
tags : mod cs
---
Created: 2023-03-08

## Un protocole : c'est quoi ?
?
Ensemble de règles pour la communication de données sur un réseau.

## Paquet de donnée
?
Un paquet est une unité de base de la communication sur un réseau numérique. Petite unité de données utilisée dans la communication en réseau.

### **Composition d'un paquet de données**
?
La structure d'un paquet dépend du type de paquet et du protocole. Normalement, un paquet comporte un en-tête et une charge utile.
![[image-20230308145655241.png]]
![[image-20230308150001447.png]]

le transfert de données sur internet nécessite la décomposition des données en paquets IP, ce qui est défini dans IP (Internet Protocol), et un paquet IP comprend :
- L'adresse IP source, qui est l'adresse IP de la machine qui envoie les données. 
- L'adresse IP de destination, qui est la machine ou l'appareil auquel les données sont envoyées. 
- Le numéro de séquence des paquets, un numéro qui place les paquets dans un ordre tel qu'ils sont réassemblés de manière à retrouver les données originales telles qu'elles étaient avant la transmission. 
- Le type de service, les drapeaux et d'autres données techniques



