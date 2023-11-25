---
tags : mod Math
---
Created: 2023-10-02

# Nombres complexes
$\sqrt{-1}$=::$i$
<!--SR:!2023-12-28,34,286-->

$$\LARGE{z=a+bi}$$
- Re($z$) =:: $a$
<!--SR:!2023-12-26,35,306-->
- Im($z$) =:: $b$
<!--SR:!2024-01-13,68,250-->

---
$(a+bi)(c+di)$=
?
$$\Large{(ac-bd)+i(ad+bc)}$$
<!--SR:!2023-11-22,2,226-->

$(a+bi)^{2}$=
?
$$\Large{a^{2}-b^{2}+i2ab}$$
<!--SR:!2023-11-26,10,250-->

$(a-bi)^{2}$=
?
$$\Large{a^{2}-b^{2}-i2ab}$$
<!--SR:!2023-12-05,11,230-->

$(a+ib)(a-ib)$=
?
$$\Large{a^{2}+b^{2}}$$
<!--SR:!2023-11-25,11,266-->

---

$z^{*}$=
?
$$\Large{a-ib}$$
<!--SR:!2023-11-25,9,291-->

$z+z^*$=
?
$$\Large{2a}$$
<!--SR:!2023-11-26,8,252-->

$z-z^{*}$=
?
$$\Large{2bi}$$
<!--SR:!2023-11-27,11,266-->

$zz^{*}$=
?
$$\Large{a^{2}+b^{2}}$$
<!--SR:!2023-12-05,15,230-->

---
$|z|$=
?
$$\Large{\sqrt{a^{2}+b^{2}}}$$
<!--SR:!2023-11-23,10,286-->

$|z|^{2}$=
?
$$\Large{zz^{*}}$$
<!--SR:!2023-11-22,8,246-->

Propriétés des sommes, soustractions, multiplication et division de deux conjuguées:
?
![[Pasted image 20231002063707.png]]
<!--SR:!2023-11-27,7,252-->

## Forme polaire
Nombre complexe forme polaire et exponentielle::$$\large{z=r(\cos\theta+i\sin\theta)=re^{i\theta}}$$
<!--SR:!2023-11-24,11,246-->

- $\cos\theta$=::$\frac{a}{|z|}$

- $\sin\theta$=::$\frac{b}{|z|}$

- $|zw|$=::$|z||w|$

- $|\frac{z}{w}|$=::$\frac{|z|}{|w|}$

- $zw$=::$|z||w|[\cos(\theta+\alpha)+i\sin(\theta+\alpha)]$

- $\frac{z}{w}$=::$\frac{|z|}{|w|}[\cos(\theta-\alpha)+i\sin(\theta-\alpha)]$

- $z^{n}$=::$|z|^{n}(\cos n\theta+i\sin n\theta)$

- $\theta$=::$\tan^{-1}(\frac{b}{a})$

- $z_{k}$=::$\sqrt[n]{|z|}\text{cis}\left(\frac{\theta}{n}+\frac{2k\pi}{n}\right)=\sqrt[n]{|z|}\exp\left(\frac{i(\theta +2k\pi)}{n}\right),\,k=0,1,2,...,n-1$

- $(z-w)(z-w^{*})$=::$z^{2}-z\text{Re}(w)+|w|^{2}$

## Formules d'Euler (module=1)
Si $|z|=1$ alors $z^{*}$=::$z^{-1}$

$e^{i\pi}$=::$-1$

- $z^{n}+z^{-n}$=::$2\cos(n\theta)$

- $z^{n}-z^{-n}$=::$2i\sin(n\theta)$

- $e^{in\theta}+e^{-in\theta}$=::$2\cos(n\theta)$

- $e^{in\theta}-e^{-in\theta}$=::$2i\sin(n\theta)$

## Fresnel formule complexe
$a\cos\theta+b\sin\theta$=::$\text{Re}[(a-ib)e^{i\theta}]$
