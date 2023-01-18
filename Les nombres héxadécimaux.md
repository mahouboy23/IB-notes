---
tags : mod cs
---
Created: 2023-01-18

## Système numérique décimal
L'hexadécimal est un système de numération comportant 16 symboles :
?
0123456789*ABCDEF*

C'est pourquoi on l'appelle souvent la numérotation **BASE-16**. Le hexadécimal, comme on l'appelle souvent, est utilisé pour représenter rapidement de très grands nombres, comme ceux utilisés dans la représentation des couleurs.

## Ecriture des premiers nombres entiers en hexadécimal
Un nombre écrit en hexadécimal se décompose à l’aide des puissances de 16.
$$B2_{16} = B*16^1 + 2*16^0 = *178_{10}$$

## Conversion entre base hexadécimale et base décimale
**Hexadécimale => Décimale** 
?
Les nombres écrits en hexadécimal suivent le même principe que ceux écrits en décimal mais avec les puissances de 16.
3F4(2) = 3x162 + Fx161 + 4x160 = 3x162 + 15x161 + 4x160 = 1012(10)
![[image-20230118170554710.png]]

**Binaire => Hexadécimale** 
?
Il suffit de faire correspondre un mot de quatre bits (quartet) à chaque chiffre hexadécimal.