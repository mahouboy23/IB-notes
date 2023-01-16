---
tags : mod Physique
---
Created: 2022-12-12

## La notion de resistance : 
Tout les matériaux ne conduisent pas le courant électrique de la meme manière.
On défini la resistance électrique comme : 
?
$$R=\frac{\delta V}{I}$$ 
R = en Ohm
V = en volte 
I = en ampere 
<!--SR:!2023-01-15,3,250-->

La resistance d'un fil conducteur depend de :
?
- surface de base A
- longueur l
- la nature du matériau p résistivité 
$$R=\frac{\rho l}{A} \hspace{2mm} OU \hspace{2mm} \rho =\frac{RA}{l}$$ R = en ohm 
$\rho$ = en ohm m
A = en $m^2$ 



La droite representant U en fonction de I est linéaire U et I sont proportionnelles  
$U=aI$ 
$U=RI$ 

**Loi d'Ohm**: A temperature constante tension et l'intensite aux bornes d'un conducteurs sont proportionnelles 

**Un conducteur ohmique**: est un conducteur qui obéit a la loi d'Ohm 

## Association de resistors 

- **Association en série** $R_{eq_{s}}=R_{1}+R_{2}+R_{3}...$ 
l'association en série de plusieurs resistors est equivalent a un resistor $R_{eqs}$ dont la resistance est égale a la somme des resistances 

- **Association en parallèle** $\frac{1}{R_{eq//}}=\frac{1}{R_{1}}+\frac{1}{R_{2}}+\frac{1}{R_{3}}$ 
- $$\frac{1}{R}=G$$
- R = en Ohm
- G conductance = Siemens 

### Dissipation d'énergie électrique dans un resistor : Effet joules
Lorsque qu'un conducteur est parcourue par un courant électrique il y a un dégagement de chaleur: c'est l'effet joules
Pour lutter contre l'effet joules on prévoit des dispositif d'aeration ou de ventilation dans certains appareils électrique (tele, ordinateur). L'effet joules est utiliser avantageusement dans certains dispositif comme les plaques chauffantes, chauffe eau..
La puissance dissipe par effet joule est proportionnelle au carre
$$P=RI^2$$
$$U=RI \rightarrow I=\frac{U}{R}$$
$$P=R*\frac{U^2}{R^2}=\frac{U^2}{R}$$ 
### Utilisation des appareils de mesure 
Un appareil de mesure modifie le circuit et a un effet sur la mesure 
- **Utilisation d'un ampèremètre** :
Un ampèremètre ideal a une resistance interne nul
-  **Utilisation d'un voltmètre** :
Un voltmètre ideal a une resistance interne infinie 

### Diviseur de tension et montage potentiométrique
- **Diviseur de tension**
Par exemple si on a un générateur de 12V et que l'on veuille alimenter un appareil de 4V par ex on peut utiliser le montage diviseur de tension.

![[DIVISEUR DE TENSION]]

$$U_{ab}=(R_{ac}+R_{cb})I$$
$$U_{ac}=R_{ac}I$$
$$\frac{U_{ac}}{U_{ab}}=\frac{R_{ac}\cancel{I}}{(R_{ac}+R_{cb})\cancel{I}}$$
$$U_{ac}=\frac{R_{ac}}{R_{ac}+R_{cb}}U_{ab}$$
Si on remplace la resistance de 50$\ohm$ par un de 100$\ohm$ I devient

- **Montage potentiométrique**
?
Un potentiomètre est un conducteur ohmique ayant trois bornes de borne fixe A et B et une borne mobile C appeler curseur. Si l'on branche le potentiomètre par les deux bornes fixes A et B se dernier se comporte comme un resistance fixe. 
![[]]

- **le rheostat**
?
Le rheostat est un potentiomètre branche avec les bornes A et C ou B et C. Le montage rheostat serre a faire varier l'intensite dans un circuit car la resistance varie selon la position du curseur.