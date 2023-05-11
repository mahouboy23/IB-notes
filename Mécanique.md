---
tags : mod Physique
---
Created: 2023-03-28

## Cinématique

### 1/ **Notion de cinématique**

#### deplacement et distance parcourue 
Souvent la longueur du déplacement est différente de la distance parcourue
![[Pasted image 20230328083239.png]]

**Trajectoire** :: est l'ensemble des position prise par l'objet ou par le mobile au cour du temps

#### VITESSE 
##### A) VITESSE SCALAORE MOYENNE
$$ V = \frac{d}{t}$$
##### B) VECTEUR VITESSE MOYENNE (VELOCITY)
$$\vec{V}=\frac{\vec{D}}{\Delta{\vec{t}}}$$
$M_1$, $M_2$ positions aux date $t_1$ et $t_2$

$$\vec{V}_{1\rightarrow 2}=\frac{\vec{M_{1}M_{2}}}{t_{2}-t_{1}}$$
##### C) VITESSE INSTANTANNEE 
?
C'est le vecteur vitesse moyenne pour 2 positions très proches.
$$\vec{v}=\lim _{\Delta{t} \to 0} \hspace2mm \frac{\vec{M_{1}M_{2}}}{t_{2}-t_{1}} = d\frac{O\vec{M}}{dt} $$ 
![[image-20230328093633362.png]]
pente de la tangente a la trajectoire a la date donnée

#### L'acceleration
?
C'est la variation de la vitesse au cour du temps


- acceleration moyenne a.
$$\vec{a}=\frac{\Delta{\vec{v}}}{\Delta{t}}$$
- acceleration instantanée
$$\vec{a}=\frac{d\vec{v}}{dt}$$
### 2/ **Les equations de la cinématique a une dimension equation SUVAT**

#### uTILISATION DES AIRES
*Diagramme v en fonction de t*

![[image-20230328094704451.png]]



Aire entre la courbe representant r en fonction du temps et l'axe des temps est égale au déplacement  $\Delta{x}$ 
déplacement : $\Delta{X}=A_{1}+A_{2}$
distance parcourue : $d= \lvert A_{1} \rvert + \lvert A_{2} \rvert$ 

*Diagramme a en fonction de t*
![[image-20230328094057566.png]]

$A_{2}$ en $ms^{-2}*s=ms^{-1}$ 
aire entre la courbe de a en fonction de t et l'axe des temps t est $=\Delta{v}$ 

#### Mouvement rectiline uniforme

![[image-20230330154850103.png]]

![[image-20230330170146114.png]]



![[image-20230328092624940.png]]

#### g/ Mouvement d'un projectile

![[nm]]




## Force et Lois de Newton

### **A)** Exemples de forces

#### 1. Force a distance 
- Le poids d'un corps ou/et la force de gravitation 
$$\vec{P} = m\vec{g}$$
-Direction verticale 
-Sens vers le bas
-Point d'application: centre de gravite
-$P=mg$

- **La force électrique**
$\vec{F_{e}} = q\vec{E}$        $E = \frac{K\hspace1mm q_{1}q_{2}}{r^2}$ voir $T_{5}$ 

- **Force magnétique voir**
$F_{m}=qvBsin\theta$ 

#### 2. Force de contact
- **La reaction d'un support**
$\vec{R}$ force qu'exerce le support sur l'objet *Reaction* 
![[Pasted image 20230504094025.png]] 

Quand il y a des frottements la reaction est inclinée

- **La tension d'un fil**
C'est la force que l'on exerce aux 2 extrémités d'un fil
![[Pasted image 20230504095510.png]]


- **La tension d'un ressort**
![[Pasted image 20230509081424.png]]

La tension d'un ressort s'oppose a sa deformation.
$$T = Kx$$
x allongement (compression) du ressort.
K $nm^{-1}$ constante de raideur (d'elasticite) du ressort
$x=l-l_{0}$  $l$, $l_0$  longueur finales et initiales du ressort.
$$ T = kx= k(l-l_{0}) = kl - kl_{0} $$
 - **Poussée d'Archimede**
 Lorsqu'un objet est plonge dans un fluide (gas ou liquide) une force verticale dirigée vers le haut appelée poussée d'archimede (= au poids de fluide déplacé)
 
![[Pasted image 20230509090413.png]]
$$A = P_{fluide} * V_{immerge}*g$$
### **B)** Les lois de Newton

- **Premier lois de Newton** 
Dans un référentiel Galiléens (ou inertie) un système reste au repos ou garde son mouvement rectiligne uniforme si la somme des forces extérieur applique est nul.
Un référentiel Galiléens est un endroit ou on peut applique la premier loi de Newton
$$\sum \vec F_{ext} = \vec 0$$

- **Deuxième loi de Newton**
Dans un référentiel Galiléens la somme des forces extérieur est égale au produit de la masse et du vecteur acceleration.
$$\sum \vec F_{ext} = m\vec a$$
- **Troisième loi de Newton**
Lorsque deux object son interaction la force qu'exerce l'un sur l'autre est oppose a la force que exerce l'autre sur l'un.

### **C)** Application des lois de Newton

- **Méthode de resolution des exercices de dynamique**
1. chois du système (système d'etude)
2. définir le référentiel d'etude
*exemple :* 
-un référentiel du labo, référentiel terrestre pour les mouvement sur Terre
-un référentiel géocentrique pour les satellite, la lune
-un référentiel héliocentrique mouvement des planètes
3. inventaire des forces
4. application d'une loi de Newton
5. définir un repère et faire des projections puis faire des calculs

- **Application de la deuxième loi de Newton**
-Chute Libre
Un object de masse m tombe, on néglige la resistance de l'air. 
système : objet de masse m
Inventaire des forces $\vec p = m \vec g$

-Object glissant sur un plan incline sans frottement
