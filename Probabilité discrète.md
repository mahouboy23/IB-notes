---
tags : mod Math
---
Created: 2023-10-02

## Experience aléatoire événements  
Une expérience aléatoire est une expérience dont l'issue dépend du:: hasard.
<!--SR:!2023-11-22,12,302-->
L'ensemble des résultats possibles d'une expérience aléatoire est appelé:: univers.
<!--SR:!2024-01-23,78,290-->
On appelle événement :: toute partie de l'univers (sous-ensemble)
<!--SR:!2024-03-02,1,229-->

### Définitions
- Evénement élémentaire :: a une seule issue
<!--SR:!2024-01-22,77,290-->
- Evénement composé :: a plusieurs issues
<!--SR:!2023-12-01,11,307-->
- Evénement A et B (conjonction d'événement):: événement constitué des issues communes aux deux événements
<!--SR:!2024-03-26,25,287-->
- Evénement contraire a A noté A' :: événement dont les issues n'appartiennent pas a A
<!--SR:!2023-12-22,32,302-->
- Evénement A ou B (disjonction d'événement):: événement constitué de toutes les issues des deux événements
<!--SR:!2023-12-11,35,250-->
- Evénement incompatible (mutuellement exclusif):: conjonction des deux événements avec aucune issue
<!--SR:!2023-12-25,34,302-->
- Evénement certain :: toutes les issues
<!--SR:!2023-11-30,10,307-->
- Evénement impossible :: aucune issue
<!--SR:!2023-11-29,11,307-->

## Calcul de probabilité
- La probabilité d'un événement est la somme:: des éléments élémentaires qui le compose.
<!--SR:!2023-11-29,9,287-->
- Lorsque les événements élémentaires ont meme probabilité, on dit qu'il y a :: équiprobabilité ou équi-répartition.
<!--SR:!2024-01-03,42,322-->

### Propriété
- $P(U)$=:: 1 
<!--SR:!2023-12-12,36,270-->
- $P(0)$=:: 0
<!--SR:!2023-11-22,9,303-->
- $P(A)+P(A')$=:: 1
<!--SR:!2023-12-11,21,282-->
- $P(A\cup B)$=:: $P(A)+P(B)-P(A\cap B)$
<!--SR:!2023-12-08,32,270-->
- $P(A/B)$=:: $\frac{P(A\cap B)}{P(B)}=\frac{n(A\cap B)}{n(B)}$
<!--SR:!2023-12-01,11,307-->
- 
- ## Événements dépendants
Deux événements sont dépendants si:: la survenance de l'un d'entre eux affecte la probabilité que l'autre se produise. L'échantillonnage sans remplacement en est un exemple.
<!--SR:!2023-11-25,9,267-->

Pour les événements dépendants A et B, $P(A\cap B)$=::$P(A)\times P(B/A)$
<!--SR:!2023-12-14,24,282-->

## Probabilité conditionnelle
Pour deux événements A et B, $A/B$ représente l'événement "A sachant B", et $P(A/B)$=::$\frac{P(A\cap B)}{P(B)}$
<!--SR:!2024-01-21,76,290-->

Pour des événements indépendants, $P(A)$=::$P(A/B)=P(A/B')$
<!--SR:!2023-12-05,15,282-->

Axiom des probabilités totales, pour événement secondaire : $P(B)$=::$P(A\cap B)+P(A'\cap B)$
<!--SR:!2023-12-02,5,223-->

$P(A\cap B')$=::$P(A)-P(A\cap B)$
<!--SR:!2023-11-29,2,207-->

$A\Delta B$ (difference symetrique)=: $(A \cap B') \cup (A' \cap B)$ 