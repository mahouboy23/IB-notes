---
tags : mod Math
---
Created: 2024-03-19

je veux trouver un nouveau question de recherche pour mon exploration en Math AA HL qui me permet d'incorporet tout c'est calcul et questions and mon exploration. Je veux que la question de recherche a un aim qui permet de relier tout c'est question pour un but spécifique et permet de relier et donner un context pour tout c'est calcul et question.
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


## Answer

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

