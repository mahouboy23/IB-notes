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

On peut donc utiliser le modelè visqueux pour la théorie 