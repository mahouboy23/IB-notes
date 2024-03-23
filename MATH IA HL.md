---
tags : mod Math
---
Created: 2024-03-19
## Évaluation de calculus et la probabilités dans la distribution normale

$$X \sim \mathcal{N}(\mu,\,\sigma^{2})$$
$$f(x) = \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x - \mu)^2}{2\sigma^2}}$$
a) Calculer $f'(x)$ et $f''(x)$ *Use chaine rule and other* 
b) Prouver que $f(x)$ admet un maximum local en $x=u$  
c) Montrer que $C_f$  admet un point d'inflection en $x=u+\sigma$ et $u-\sigma$ 
d) $$E(X)=\int_{-\infty}^{+\infty} xf(x) \, dx$$$$\text{Si} \hspace4mm F(x)=\int f(x)\,dx$$
$$\text{Montrer} \hspace4mm \int (x-u)^2f(x)\,dx \,-\sigma^{2}=0$$
Pour $u=50$ et $\sigma=4$ 
e) Construire la fonction $f(x)$
f) Calculer $P(a<X<b)$ que dur $P(X=a)$ et $P(X=b)$ 
g) Representer $f$ 
h) Déduire la concavité de $f(x)$
I) Trouver l'aire $P(40<X<60)$
    i/ Méthode probabilité
    ii/ Méthode integral
j) Montrer que $\sum P(X=X)=1$ 
K) $f(x)$ approche la loi normale trouver $E(X)$ et $Q_2$  on utilisant les intégrales définis
l) Prouver X est une loi normale avec $\text{Moyenne = Mediane = Mode}$ 
m) $P(X>b)=0,30825$ avec l'aide des intégrales $k$ 


## SOLUTION

a)$$
\begin{aligned}
& f(x)=\frac{1}{\sigma \sqrt{2 \pi}} e^{-\frac{(x-y)^2}{2 \sigma^2}} \\
& f^{\prime}(x)=\frac{1}{\sigma \sqrt{2 \pi}}\left(c^{-\frac{(x-\omega)^2}{x \sigma^2}}\right)^{\prime}
\end{aligned}
$$
En applicant chain rule sur $\left[e^{-\frac{(x-u)^2}{2 \sigma^2}}\right] \frac{d}{d x}$ 
$$
\begin{aligned}
& \frac{d y}{d x}=\frac{d y}{du} \times \frac{d u}{d x} \\
& \frac{d y}{d x}=e^{\frac{-(x-u)^2}{2 \sigma^2}} \times\left(-\frac{(x-u)^2}{2 \sigma^2}\right)^{\prime} \\
& \frac{d y}{d x}=e^{-\frac{ (x-u)^2}{2 \sigma^2} \times-\frac{1}{2 \sigma^2} 2(x-u)} \\
& \frac{d y}{d x}=e^{\frac{-(x-u)^2}{2 \sigma^2} \times-\frac{x-v}{\sigma^2}}
\end{aligned}
$$
$$
\begin{aligned}
& f^{\prime}(x)=\frac{1}{\sigma \sqrt{2 \pi^2}} \times e^{-\frac{(x-u)^2}{2 e^2}} \times-\frac{x-u}{\sigma^2} \\
& f^{\prime}(x)=-\frac{e^{-\frac{(x-u)^2}{2 \sigma^2}(x-u)}}{\sigma^3 \sqrt{2 \pi}}=-\frac{(x-u)}{\sigma^2} f(x)
\end{aligned}
$$
$$
\begin{aligned}
& f^{\prime \prime}(x)=\left(-\frac{(x-u)}{\sigma^2}\right)^{\prime} f(x)-\frac{(x-y)}{\sigma^2} f^{\prime}(a) \\
& f^{\prime \prime}(x)=-\frac{1(x)}{\sigma^2}+\frac{(x-y)^{\prime}}{\sigma^2} f^{\prime}(x) \\
& \left.f^{\prime \prime}(x)=-\frac{1(x)}{\sigma^2}-\frac{(x-0)}{\sigma^2} \times-\frac{(x-0)}{\sigma^2} \right\rvert\,(x) \\
&  f^{\prime \prime}(x)= -\frac{f(x)}{\sigma^2}+\frac{(x-0)^2}{\sigma^4} f(x) \\

\end{aligned}
$$
b) Pour prouver que $f(x)$ admet un maximum local en $x=u$ posons $x=4$  $f^{\prime}(x)$ or $f^{\prime \prime}(x)$
$$
\begin{aligned}
& f^{\prime}(u)=-\frac{u-u}{\sigma^2} f(u)=0 \\
& f^{\prime \prime}(u)=\frac{-f(u)}{\sigma^2}+\frac{(u-u)^2 f(u)}{\sigma^4}=\frac{-f(u)}{\sigma^2}
\end{aligned}
$$
Cela indique que la pente de la tangente a la courbe $f(x)$ en $x=u$ est nulle et $f^{\prime \prime}(x)$ est négative
donc $f(x)$ en $x=u$

c) On peut montrer que la courbe de f(x) admet un point d'inflection en $x=u+\sigma$ et $x=u-\sigma$ en posons $f^{\prime\prime}(x)=0$ 
$$
\begin{aligned}
& \frac{-f(x)}{\sigma^2}+\frac{(x-u)^2 f(x)}{\sigma^4}=0 \\
& \frac{\frac{-f(x)}{\sigma^2}+\frac{(x-u)^2 f(x)}{\sigma 4}}{f(x)}=\frac{0}{f(x)} \\
& \sigma^4\left(\frac{-1}{\sigma^2}+\frac{(x-u)^2}{\sigma^4}\right)=0 \times \sigma^4 \\
& -\sigma^2+(x-u)^2=0 \\
& (x-u)^2=\sigma^2 \\
& x-4= \pm \sigma \\
& x=u \pm \sigma
\end{aligned}
$$
d)


e) La fonction de densité de probabilité $f(x)$ pour une variable aléatoire $X$ suivant une distribution normale avec une moyenne $\mu$ et un écart-type $\sigma$ est donnée par la formule :
$$
f(x)=\frac{1}{\sigma \sqrt{2 \pi}} e^{-\frac{(x-\mu)^2}{2 \sigma^2}}
$$

En substituant $\mu=50$ et $\sigma=4$, nous obtenons :
$$f(x)=\frac{1}{4 \sqrt{2 \pi}} e^{-\frac{(x-50)^2}{2 \cdot 4^2}}$$
f)


g) Representation de $f$ 

![[image-20240323104626808.png]]

h) ![[image-20240323105307196.png]]
La courbe bleue montre la distribution normale centrée autour de la moyenne $\mu=50$ avec un écart-type $\sigma=4$. Les points rouges indiquent les points d'inflexion, situés à $\mu \pm \sigma$, soit 46 et 54 dans ce cas. La concavité de la courbe change en ces points : elle est concave vers le bas (comme un "∩") entre eux et concave vers le haut (comme un "U") en dehors de cette plage. La courbe verte représente la seconde dérivée de la fonction de densité, qui traverse zéro aux points d'inflexion, confirmant le changement de concavité.

I)