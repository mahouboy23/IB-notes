---
tags : mod Math
---
Created: 2023-10-02

## Experience aléatoire événements  
Une expérience aléatoire est une expérience dont l'issue dépend du:: hasard.
<!--SR:!2023-11-10,3,282-->
L'ensemble des résultats possibles d'une expérience aléatoire est appelé:: univers.
<!--SR:!2024-01-23,78,290-->
On appelle événement :: toute partie de l'univers (sous-ensemble)

### Définitions
- Evénement élémentaire :: a une seule issue
<!--SR:!2024-01-22,77,290-->
- Evénement composé :: a plusieurs issues
- Evénement A et B (conjonction d'événement):: événement constitué des issues communes aux deux événements
- Evénement contraire a A noté A' :: événement dont les issues n'appartiennent pas a A
<!--SR:!2023-11-10,3,262-->
- Evénement A ou B (disjonction d'événement):: événement constitué de toutes les issues des deux événements
<!--SR:!2023-12-11,35,250-->
- Evénement incompatible (mutuellement exclusif):: conjonction des deux événements avec aucune issue
<!--SR:!2023-11-21,11,282-->
- Evénement certain :: toutes les issues
- Evénement impossible :: aucune issue

## Calcul de probabilité
- La probabilité d'un événement est la somme:: des éléments élémentaires qui le compose.
- Lorsque les événements élémentaires ont meme probabilité, on dit qu'il y a :: équiprobabilité ou équi-répartition.
<!--SR:!2023-11-22,12,302-->

### Propriété
- $P(U)$=:: 1 
<!--SR:!2023-12-12,36,270-->
- $P(0)$=:: 0
<!--SR:!2023-11-11,3,283-->
- $P(A)+P(A')$=:: 1
<!--SR:!2023-11-17,7,262-->
- $P(A\cup B)$=:: $P(A)+P(B)-P(A\cap B)$
<!--SR:!2023-12-08,32,270-->
- $P(A/B)$=:: $\frac{P(A\cap B)}{P(B)}=\frac{n(A\cap B)}{n(B)}$
- 
- ## Événements dépendants
Deux événements sont dépendants si:: la survenance de l'un d'entre eux affecte la probabilité que l'autre se produise. L'échantillonnage sans remplacement en est un exemple.

Pour les événements dépendants A et B, $P(A\cap B)$=::$P(A)\times P(B/A)$
<!--SR:!2023-11-19,9,282-->

## Probabilité conditionnelle
Pour deux événements A et B, $A/B$ représente l'événement "A sachant B", et $P(A/B)$=::$\frac{P(A\cap B)}{P(B)}$
<!--SR:!2024-01-21,76,290-->

Pour des événements indépendants, $P(A)$=::$P(A/B)=P(A/B')$
<!--SR:!2023-11-11,3,262-->

Axiom des probabilités totales, pour événement secondaire : $P(B)$=::$P(A\cap B)+P(A'\cap B)$
<!--SR:!2023-11-12,2,243-->

$P(A\cap B')$=::$P(A)-P(A\cap B)$>)

$A\Delta B$ (difference symetrique)=: $(A \cap B') \cup (A' \cap B)$ 