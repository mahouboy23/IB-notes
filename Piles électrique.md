---
tags : mod Physique
---
Created: 2022-12-20

Une Piles converti l'énergie chimique en énergie électrique avec dissipation d'énergie sous forme de chaleur. 
Une pile est caractérise par sa [[Fem]] (Force electromotive) e et sa resistance interne r

## Expression de la tension au bornes d'une pile 
Une pile de fem et resistance interne r fournit une tension $U_{pn}$ et une intensité I
*Conversion d'énergie dans une pile:*
![[Pasted image 20221220082900.jpg]]
$$eI = UI+RI^2$$
$$e\cancel{I}=\cancel{I}(U+rI)$$
La tension aux bornes d'une pile est : $U_{pn}=e-rI$ 

-Caractéristique intensité - tension d'une pile


![[forum_189021_1.gif]]

On peut trouver la formule $U_{pn}=e-rI$  en effectuant le montage suivant 
	![[Pasted image 20221220084137.png]]

- U = e quand I = 0 
 e = c'est la tension aux bornes de la pile quand elle ne fournit pas de courant.
- Une pile idéale est une pile qui n'a pas de resistance interne r = 0 et U = e

-Circuit equivalent d'une pile reel  

![[download 1.svg]]

la pile réelle peut être remplacée par un pile idéale e branchée en série avec un resistor r

# Circuit avec des pile

## Circuit simple pile-resistor 
-Circuit simple pile-resistor
![[assets/Piles électrique/download.svg]]
$$U_{pn}=U_R$$$$e-rI=RI$$
$$e=rI+RI$$
$$e=(r+R)I$$

## Circuit simple comportant piles, récepteurs et resistors

- Tension aux bornes d'un récepteur. 
Un récepteur :: (ex un moteur, un électrolyseur) est un appareil qui consomme plus d'énergie que n'a besoin l'effet Joule 
<!--SR:!2023-01-24,1,210-->
Le récepteur est caractérise par un fceme force contre électromotrice r resistance interne. 
$$U_{recept}=é+rI$$![[Pasted image 20230109161706.png]]

- Une pile branchée en opposition se comporte comme un récepteur. 
![[circuit recepteur]] 

## Circuit avec des nœuds comportant un générateur


 ![[image-20230109170126492.png]]

## Association de piles

- en série 
![[association de piles]]

$$U_{pn}=U_{pa}+U_{ab}+U_{bn}$$
$$U_{pn}=e_{1}+e_{2}+e_{3}-(r_{1}+r_{2}+r_{3})I$$
$$e_{s}=\sum\limits e \hspace10mm r_{s}=\sum\limits r_{s}$$
- en parallèle de piles identiques
![[association de pile]]

$$U_{PN}=e-r\frac{I}{n}=e-r\frac{I}{n}=e-r\frac{I}{n}$$
$$e_{//}=e,\;r_{//}=\frac{r}{n}$$
