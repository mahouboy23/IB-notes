---
tags : mod Physique
---
Created: 2024-04-05

## Note partie théorique
Pour voir si le vidange du liquide suit un modèle visqueux ou parfait on peut utiliser le nombre de Reynolds qui mesure le rapport entre les forces d’inertie et les forces de viscosité. Pour une conduite cylindrique, comme le tuyau de sortie, l’écoulement est considéré comme parfait si le nombre de Reynolds est supérieur à Re=1000 et visqueux dans le cas contraire. 
$$\operatorname{Re}=\frac{\rho v \mathrm{R}}{\eta} \rightarrow\left\{\begin{array}{l}>1000 \text { écoulement parfait } \\ <1000 \text { écoulement visqueux }\end{array}\right.$$
Mais cela n'est pas suffisant car il ne tient pas compte de l'effet du rayon et longueur du tuyau. Donc on peut utiliser le rapport entre l'énergie cinétique du fluide et l'énergie dissipée par frottement dans le tube sortie : 
$$\operatorname{\frac{E_{c}}{E_{\eta}}} \approx \frac{\frac{1}{2} v^{2} \rho}{\eta \Delta v L} \approx \operatorname{Re} \frac{R}{L} \rightarrow\left\{\begin{array}{l}>1 \text { écoulement parfait } \\ <1 \text { écoulement visqueux }\end{array}\right.$$
### Tableau des valeurs
| Les longueurs du Tube | rapport | écoulement |
| ---- | ---- | ---- |
| 16 | $\frac{0.25}{16}=0.0156$ | écoulement visqueux |
| 14 | $\frac{0.25}{14}=0.0178$ | écoulement visqueux |
| 12 | $\frac{0.25}{12}=0.0208$ | écoulement visqueux |
| 10 | $\frac{0.25}{10}=0.025$ | écoulement visqueux |
| 7 | $\frac{0.25}{7}=0.0357$ | écoulement visqueux |
| 4 | $\frac{0.25}{4}=0.0625$ | écoulement visqueux |
| 1 | $\frac{0.25}{1}=0.25$ | écoulement visqueux |
| 0 | NA | écoulement parfait  |
On peut donc utiliser le modèle visqueux pour la théorie :
on peut déduire deux grandeurs on utilisant la loi de poiseuille qui relie le profil de la vitesse dans le tube à sa section et longueur :
$$v(r, t)=\frac{m g h(t)}{4 \eta L}\left[\mathrm{R}^2-r^2\right]$$$$\left\{\begin{array}{l}\Phi(t)=\int_0^R v(r, t) 2 \pi r d r=\frac{\pi \mathrm{R}^4}{8 L \eta} \rho g h(t) \\ v(t)=\frac{\Phi(t)}{s}\end{array}\right.$$ avec : 
- $v(r,t)$ = la vitesse dans le tube
- $\Phi(t)$ = le debit massique
- $v(t)$ = la vitesse moyenne du fluide à la sortie du tube

donc le temps de vidange peut être donnée par :
$$Q_v=\frac{V}{T}$$
$$Q_v=\frac{\phi}{\rho}=\frac{V}{T}$$
$$T=\frac{V \rho}{\phi}$$  
## Note partie experience et analyse
Apres avoirs collecter les données je peux commencer par representer les données sur les temps de vidange pour chaque longueur du tube. Après je vais utiliser le temps de vidange entre deux hauteurs très proches et la formule du débit massique $Q_m = \frac{\rho V}{t}$, et développer un graphe entre le débit moyen et la longueur du tube.

2. Calcul du débit massique:
- Pour chaque longueur de tube, on calcule le débit massique am en utilisant la formule $\mathrm{Q_m}=\frac{\rho v} {\mathrm{t}}$, où :
- $\quad$ est la masse volumique de l'eau $\left(1000 \mathrm{~kg} / \mathrm{m}^{\wedge} 3\right)$
- $V$ est le volume d'eau écoulé entre les deux hauteurs proches, $V=\pi r^2(h 1-h 2)$
- $r$ est le rayon de la bouteille $(8,7 \mathrm{~cm}=0,087 \mathrm{~m})$
- $h1-h2$ est la différence de hauteur $(0,5 \mathrm{~cm}=0,005 \mathrm{~m})$
- $t$ est le temps mis par le niveau pour passer de h1 à h2 (valeurs du Tableau 3)
- Par exemple, pour $L=16 \mathrm{~cm}$ :
$\mathrm{Q_m}=1000 \times \pi \times(0,087)^2 \times 0,005 / 2,38=0,0119 \mathrm{~kg} / \mathrm{s}$
3. Calcul des incertitudes sur le débit massique:
- L'incertitude relative sur $Q_m$ est donnée par :
$(\frac{\Delta \mathrm{Q_m}}{\mathrm{Q_m}})^2=(\frac{\Delta \mathrm{p}} {\mathrm{p}})^2+(\frac{\Delta \mathrm{r}} {\mathrm{r}})^2+(\frac{\Delta \mathrm{h}} {\mathrm{h}})^2+(\frac{\Delta \mathrm{t}} {\mathrm{t}})^2$
- $\frac{\Delta \mathrm{p}} {\mathrm{p}}$ est négligeable car la masse volumique de l'eau est considérée constante
- $\frac{\Delta \mathrm{r}} {\mathrm{r}}=0,1 / 8,7=0,0115$ (incertitude de la règle)
- $\frac{\Delta \mathrm{h}} {\mathrm{h}}=0,1 / 0,5=0,2$ (incertitude de la règle)
- $\frac{\Delta \mathrm{p}} {\mathrm{p}}$ provient du Tableau 3 (plus grande valeur relative : $\frac{0,01}{1,34} =0,0007$
- Donc $\Delta \mathrm{Q_m} / \mathrm{Q_m}=\sqrt{\left(0^{2}+2 \times 0,0115^{2}+0,2^2+0,302^2\right)}=0,364$
- Pour L $=16 \mathrm{~cm}: \Delta \mathrm{Q_m}=0,364 \times 0,0119=0,00433 \mathrm{~kg} / \mathrm{s}$
![[image-20240408104527245.png]]

