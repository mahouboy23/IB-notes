---
tags : mod Physique
---
Created: 2023-05-13

Make a prompt to create a clear structure (in french) for this Physics Internal Assessment:
### **Sujet:**  Dans quelle mesure la longueur d'un tube de vidange d'un réservoir affecte le débit d'écoulement 

En rapport avec le thème 2.2 - Forces

_Dispositif expérimental_: Un réservoir (ouvert) est percé au fond d'un trou relié à un tube de longueur variable. La hauteur d'eau est mesurée en fonction du temps ainsi que la vitesse à la sortie du tube.

_Variable indépendante_ : Longueur du tube de vidange

_Variables contrôlées_ : Diamètre du tube, viscosité et densité du fluide (eau), température

_Variable dépendante_ : Vitesse d'écoulement du fluide à la sortie du tube

_Méthode :_

1. Mesurer la section du tube de vidange.
    
2. Effectuer des vidanges du réservoir pour différentes longueurs de tube.
    
3. Mesurer la hauteur d'eau en fonction du temps et en déduire la vitesse.
    
4. Comparer les résultats aux modèles d'écoulement parfait et visqueux.

**Hypothèse/déduction** :  Selon la longueur du tube, Le régime d'écoulement Diminuera au fil du temps. L'influence de la viscosité sur la perte de charge sera mit en évidence.
### [[Physics IA draft]] 

|  | 16cm | 14cm | 12cm | 10cm | 7cm | 4cm | 1cm | 0cm |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| temps de h_1 en s | 4.09 | 5.50 | 8.06 | 6.59 | 6.22 | 5.43 | 7.09 | 8.47 |
| temps de h_2en s | 6.15 | 7.88 | 9.73 | 8.15 | 7.81 | 6.78 | 8.62 | 9.81 |


Ok maintenant refait completement la parti théorique et utilise et inspire toi du fichier 1911.13221 (4).pdf. La parti théorique doit sortir un relation entre la longueur du tube et le temps de vidange/debit. et sa doit parler de que d'est truc relevant et utile pour mon exploration : 


tikz code : 
reverse bottle : 
```latex
\documentclass[border=5pt,tikz]{standalone}
\usetikzlibrary{decorations.text,backgrounds}
\definecolor{wine}{RGB}{216,198,62}
\definecolor{bottle}{RGB}{76,163,58}
\tikzset{
    my/.style={
        postaction={decorate},decoration={text along path,
            text={#1},text align=center}
    }
}
\begin{document}
    \begin{tikzpicture}
        \begin{scope}
            \clip (0,-2.5) --+ (0,2.5) arc (0:180:1.5) -- (-3,-2.5) arc (180:235:3) --+ (0,-.25) --+ (.45,-.25) --+ (.45,.015) (0,-2.5) arc (0:-55:3);
            \fill[inner color=bottle!50,outer color=bottle] (0,-2.5) --+ (0,2.5) arc (0:180:1.5) -- (-3,-2.5) arc (180:235:3) --+ (0,-.25) --+ (.45,-.25) --+ (.45,.015) (0,-2.5) arc (0:-55:3);
                \fill[wine!60] (-3,-5.5) rectangle ++(3,3.5);
                \fill[wine!40] (-1.5,-2) circle ({1.5cm-0.4pt} and 0.5cm);
            \foreach \x in {-5,-4.9,...,5}
            \foreach \y in {-5,...,-3}
            {
                \pgfmathsetmacro\opacity{random(1,10)*(1/10)}
                \pgfmathsetmacro\radius{random(1,2)*(.05/2)}
                    \fill[white,opacity=\opacity] (\x+1.3*rnd,\y+1.4*rnd) circle(\radius);
            }
            \draw[very thick] (0,-2.5) --+ (0,2.5) arc (0:180:1.5) -- (-3,-2.5) arc (180:235:3) --+ (0,-.25) --+ (.45,-.25) --+ (.45,.015) (0,-2.5) arc (0:-55:3);
            \path[my={The magic of Ti{\emph{\color{orange}k}}Z}] (-3.5,.5) arc(-180:0:2 and 1);
           \end{scope}
    \end{tikzpicture}
\end{document}
```