---
tags : mod Physique
---
Created: 2023-06-12

![[image-20230612164314064.png]]

## Travaille d'une force constante
Le travail d'une force constante $\vec F$ dont le point d'application se déplace de A a B est :: $W_{a \rightarrow b}(\vec f)$ 
![[image-20230615082950257.png]]


?
$$W_{a \rightarrow b}(\vec f) = \vec{F} * \vec{AB} = f * AB * \cos\theta$$
-$W$ en $J$ 
-$F$ en $N$ 
-$AB$ en $M$ 

?
- $W > 0$  travail moteur
- $W < 0$ travail resistant 
- $W = 0$ quand $f = 0$ ou $\cos\theta = 0$ avec $\theta = 90\degree$  
**Consequence** : Le travail de la force centripète est nul
<!--SR:!2023-09-10,2,230-->

### Application  (BOOK)

## Travail du poids d'un corps


$$W_{a \rightarrow b}(\vec P) = f * AB * \cos\theta = \vec P* \vec{AB}$$

![[Pasted image 20230615082356.png]]

![[image-20230615084814820.png]]

Formule du calcule du travail du poids
$$W_{a \rightarrow b}(\vec p) = P(z_{a}-z_{b})= mg(z_{a}-z_{b})$$
$\large{z_{a}}$ , $\large{z_{b}}$ sont les altitudes des points A et B

Le travaille du Poids est indépendant du chemin suivi, il depend des altitudes initiales et finales. De telle forces sont appelées conservatives. 

## Travail des forces électriques

$V_{A}-V_{B} = U_{AB} =$ *DDP entre A et B*

**DDP** = difference de potentielle électrique

$W_{A \rightarrow B}(\vec F_{e})$

Par definition $\vec{E}*\vec{AB}$ :: $V_{a}-V_{b}$
$$qE(x_{b}-x_{a}) = q(V_{a}-V_{b})$$
$$E = \frac{V_{a}-V_{b}}{x_{a}-x_{b}}$$

$$W_{A \rightarrow B}(\vec{F_{e}})=q(V_{a}-V_{b})$$ $$V_{a}-V_{b}=\frac{W_{a \rightarrow b} \hspace 1mm \vec{F_{e}}}{q}$$
**Energie potentielle électrique par unite de charge**

## Puissance d'une force

#### Puissance moyenne

$W_{A \rightarrow B}(\vec F)$  travail de la force $\vec{F}$ lors du déplacement de $A$ a $B$.
$\Delta t$ durée de ce déplacement.

**Puissance** :: travail par unite de temps
<!--SR:!2023-09-09,2,244-->
Formule de la Puissance :
?
<!--SR:!2023-09-08,1,230-->

$$P=\frac{|W_{A \rightarrow B} \hspace 1mm (\vec F) |}{\Delta t}$$
$P$ = Watts
$|W_{A \rightarrow B} \hspace 1mm (\vec F) |$ = Joule
$\Delta t$ = seconde

#### Puissance instantanee
?
$$W_{A \rightarrow B} \hspace 1mm (\vec F) = \vec{F}* \vec{AB} $$
<!--SR:!2023-09-08,1,230-->

## Travail d'une force variable (selon l'axe des x)

#### Graph force-deplacement
![[Drawing 2023-09-08 10.31.38.excalidraw]]

Aire entre la courbe representant la force en fonction de la position et l'axe des position entre $x_a$ et $x_b$ représentent le travail de la force variable $F$ entre  $x_a$ et $x_b$ 

**Formule** :
$$\text{Aire} = \frac{b+B}{Z}*h$$
$$= \frac{F_{A}+F_{B}}{Z}*(x_{B}-x_{A})$$

#### calcule du travail effectuer par un ressort




![[Drawing 2023-09-08 10.53.02.excalidraw]]
##### formule:
$$\Large{W_{A\rightarrow B}(\vec{T})=\frac{k}{2}(x^{2}_{a}-x^{2}_{b})}$$
## Energie cinétique

#### Energie cinetique de translation
L'énergie cinétique c'est l'énergie que possède un objet du au fait de son mouvement 
$$E_c=\frac{1}{2}mv^{2}$$
$E_c$ en $J$ 
$m$ en $kg$
$V^{2}$ en $ms^{-1}$    
#### Theorem de l'energie cinetique 
Dans un révérenciel galiléen la variation d'énergie cinétique d'un solide pendant une durée donnée est égal a la somme des travaux des forces extérieurs applique au solide.
$$\Delta E_{c}=E_{c_{2}} - E_{c_{1}} = \sum\limits W_{1-2} (\vec{F}) $$