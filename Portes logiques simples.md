---
tags : mod cs
---
Created: 2023-01-27

## Les opérateurs booléens
?
En informatique, le type de données booléen est un type de données, ayant deux valeurs (généralement désignées par true et false), destiné à représenter les valeurs de vérité de la logique et de l'algèbre de Boole.

Il doit son nom à George Boole, qui a été le premier à définir un système algébrique de logique au milieu du XIXe siècle. Le type de données booléen est principalement associé aux instructions conditionnelles, qui permettent différentes actions et modifient le flux de contrôle selon qu'une condition booléenne spécifiée par le programmeur est vraie ou fausse. Les opérations logiques des circuits informatiques sont régies par les règles de la logique booléenne.

### Portes logiques
Il existe six opérateurs booléens :: **AND, OR, NOT, NAND, NOR et XOR.**

Pour comprendre comment ils fonctionnent, observez un
circuit électrique simple qui comprend un interrupteur
unique, une lampe, une batterie et quelques câbles de
connexion.

Comme la lumière et l'interrupteur peuvent être allumés ou
éteints, le circuit peut se trouver dans l'un des deux états,
et ressemble ainsi au système binaire utilisé dans les
systèmes informatiques.

![[image-20230127105424342.png]]

- **AND** : 
?
L'opérateur booléen AND est légèrement plus compliqué que le simple circuit électrique de l'interrupteur marche/arrêt. La principale différence est qu'il y a deux interrupteurs en série, au lieu d'un seul.
![[image-20230127105601444.png]]
![[image-20230127105541508.png]]

- **OR** :
?
L'opérateur booléen OR possède deux interrupteurs, comme l'opérateur booléen AND. Mais au lieu de les avoir en série, l'opérateur booléen 0R a les deux interrupteurs en parallèle. 
![[image-20230127105756258.png]]
![[image-20230127105808542.png]]

- **NOT** :
?
Cet opérateur booléen a une seule entrée et une seule sortie. Cet opérateur prend l'entrée et produit l'inverse. Si l'entrée est 1/vrai, la sortie sera O/faux, et si l'entrée est O/faux, la sortie sera 1/vrai.
![[image-20230127105955092.png]]
![[image-20230127105945484.png]]

- **NAND** :
L'opérateur booléen NAND est similaire à l'opérateur booléen AND, mais avec ses sorties inversées. Comme pour l'opérateur booléen AND, l'opérateur booléen NAND peut se trouver dans quatre états. Au lieu d'avoir une sortie à 1 lorsque les deux entrées sont à 1, comme c'est le cas pour l'opérateur booléen AND, l'opérateur booléen NAND a une sortie 1 lorsqu'une ou les deux entrées sont à 0.
![[image-20230127110224972.png]]
![[image-20230127110229951.png]]

- **NOR** :
L'opérateur booléen NOR est similaire à l'opérateur booléen OR mais avec ses sorties inversées. Comme pour l'opérateur booléen OR, l'opérateur booléen NOR peut se trouver dans quatre états. Au lieu d'avoir une sortie de 1/vrai lorsqu'une ou les deux entrées sont 1/vrai, comme c'est le cas pour l'opérateur booléen OR, l'opérateur booléen NOR a une sortie de 1/vrai lorsque les deux entrées sont O/faux.
![[image-20230127110436680.png]]
![[image-20230127110427509.png]]

- **XOR** :
L'opérateur booléen XOR peut être considéré comme l'un ou l'autre, mais pas les deux. Comme pour l'opérateur booléen OR, l'opérateur booléen XOR peut se trouver dans quatre états.
![[image-20230127110609843.png]]
![[image-20230127110630242.png]]

#### Remarque
L'IB utilise ses propres symboles pour les portes logiques, et non ceux de la
norme britannique que vous trouverez sur le Web.
?
![[image-20230127110730585.png]]

![[image-20230127110825955.png]]

## Combinaison d'opérateurs / de portes logiques
- **Q = NOT(A AND B)**
![[image-20230127111307482.png]]

- **Q = NOT A NOR B**
![[image-20230127111349436.png]]

- **Q = C AND (A OR B)** 
![[image-20230127111452517.png]]

### Applications possibles dans le monde réel
*AND* : Alarme incendie : Fumée (1) ET chaleur (1)

*OR* : Lumière de voiture interne : L'une ou l'autre porte ouverte (1)

*NOR* : Climatisation : La climatisation ne se met en marche (1) que si les DEUX fenêtres A et B sont fermées. (0)

*XOR* : 2 interrupteurs d'éclairage dans un couloir

![[image-20230127112738121.png]]

![[image-20230127113027798.png]]

