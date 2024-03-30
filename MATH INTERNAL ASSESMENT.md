---
tags : mod math
---
Created: 2023-05-08

## Internal assessment

#### Objectif/question de recherche

**Comment ma vitesse de frappe se compare-t-elle à la moyenne optimale mondiale et quelle est la probabilité que ma vitesse de frappe soit supérieure à la moyenne ?**.

#### Introduction

- Présentez l'importance de la vitesse de frappe à l'ère numérique.
- Indiquez votre vitesse de frappe personnelle et l'objectif de la comparer à la vitesse mondiale à l'aide de méthodes statistiques.

#### Collecte des données

- Recueillez les données relatives à votre vitesse de frappe sur une période donnée (par exemple, 30 jours), en enregistrant les vitesses quotidiennement dans des conditions normalisées.
- Obtenez un ensemble de données sur les vitesses de frappe mondiales. Les sites web consacrés à la vitesse de frappe ou les études en ligne constituent une source potentielle.
	#### Analyse des données
	
	1. **Statistiques descriptives:**
	    
	    - Calculez la moyenne, la médiane et l'écart-type de vos vitesses de frappe et des données globales.
	2. **Application des distributions normales:**
	    
	    - Analysez si les données globales sur la vitesse de frappe suivent une distribution normale.
	    - Utilisez les données pour calculer la probabilité que ma vitesse de frappe soit supérieure à la moyenne.
	3. **Test du chi-carré:**
	    
	    - Effectuez un test du chi-carré pour comparer vos données à la moyenne globale et déterminer s'il existe une différence significative.
	4. **Utilisation des séries de Maclaurin et de l'intégration:**
	    
	    - Appliquez les séries de Maclaurin pour approximer les fonctions utilisées dans l'analyse.
	    - Utilisez l'intégration pour analyser des modèles de données continues sur la période pendant laquelle j'ai enregistré mes vitesses de frappe.
	
	#### Conclusion
	
	- Résumez les résultats de l'analyse statistique.
	- Déterminez si ma vitesse de frappe est significativement différente de la vitesse mondiale optimale.
	- Discutez des implications de mes résultats et des domaines potentiels de recherche.
	
Données : 
![[image-20240109160339608.png]]

![[image-20240109162205173.png]]

### DONNEES BRUTES

Test Number  Time (minutes)  Words Per Minute
0             1             1.0         48.556209
1             2             1.0         43.100629
2             3             1.0         45.414952
3             4             1.0         50.463573
4             5             1.0         48.970232
..          ...             ...               ...
95           96             1.0         44.326293
96           97             1.0         41.542000
97           98             1.0         48.643482
98           99             1.0         42.007648
99          100             1.0         43.107957

[100 rows x 3 columns]
Mean WPM: 41.74
Standard Deviation: 4.03


---
# [[MATH IA HL]]

SO i want you to recreate a structure and detail how and what we are gonna by focusing one main objectives and mathematics points of the research question.
**question de recherche** :Comment ma vitesse de frappe se compare-t-elle à la vitesse de frappe optimale.

here are the main mathematics points that i want to appear :
- use the math_ex and other to evaluate the normal distribution and find the parameters like variance, mean ect... and create the probability density function while explaining and proving the proprieties we are gonna use and some important aspects (relevant to the IA),
- To find the probability i want to use integration (of the pdf) and the area under the curve to find the probability that i achieve the optimal typing speed, but since the pdf functions is to hard or possibly impossible to integrate to normal means we are gonna use the McLaurin series to find an approximation of the probability
- Use z values and the z formula to find a new mean required for bringing up the probability to a realistic number and to give an idea where i need to get to improve.


# Introduction et objectif
description et info :  Définissez clairement l'objectif de l'experience, qui est de comparer ma vitesse de frappe personnelle à la vitesse de frappe optimale. Expliquez l'importance de cette comparaison dans le contexte de l'ère numérique, l'ecole, le travaille ect...
# Information général

## Distribution normale
description et info : Commencez par définir la vitesse de frappe comme une variable aléatoire $X$ qui suit une distribution normale $X \sim \mathcal{N}(\mu,\,\sigma^{2})$. Cela établit le cadre pour l'analyse statistique
## PDF d'une distribution normale
description et info : Présentez la fonction de densité de probabilité (PDF) $f(x)$ de la distribution normale et expliquez son rôle dans la modélisation de la probabilité de différentes vitesses de frappe. N'oublie pas on suppose que me données suis une distribution normale.
# Propriétés de la Distribution Normale

## Dérivées Première et Seconde
description et info : Introduit d'abord et pourquoi on fait cette section (calcul des derives et maximum/inflexion) Calculez la première et la seconde dérivée de la PDF, $f'(x)$ et $f''(x)$, pour identifier le comportement de la courbe de la distribution normale, y compris les points critiques et les points d'inflexion.
## Maximum Local et Points d'Inflexion
description et info : Démontrez que la PDF a un maximum local en $x=u$  et des points d'inflexion en $x=u+\sigma$ et $u-\sigma$, ce qui est pertinent pour comprendre la forme de la distribution de votre vitesse de frappe
# Collecte et traitement des Données
## Collecte des Données 
description et info : Décris comment j'ai avez collecté les données de vitesse de frappe sur une période donnée.

graphique :
\begin{figure}[h]
    \centering
    \begin{tabular}{|c|c|c|}
        \hline
        \textbf{Nombre de Test} & \textbf{Temps (minutes)} & \textbf{Mots Par Minutes} \\
        \hline
        1 & 1.0 & 48.556209 \\
        2 & 1.0 & 43.100629 \\
        3 & 1.0 & 45.414952 \\
        4 & 1.0 & 50.463573 \\
        5 & 1.0 & 48.970232 \\
        $n$ & 1.0 & $x_n$ \\
        \hline
    \end{tabular}
    \caption{Échantillons du jeu de données de la vitesse de frappe.}
    \label{fig:data-samples}
\end{figure}
## Calcule de la moyenne ($\mu$) et l’écart-type ($\sigma$)

## Visualisation de la Distribution des Données
description et info : Construisez la fonction de densité de probabilité (PDF) pour ma vitesse de frappe. et utilisez les propriétés (dans, Maximum Local et Points d'Inflexion et Dérivées Première et Seconde ect...) pour discuter de la forme et des caractéristiques de la distribution de ma vitesse de frappe et qu'est ce que cela implique dans plusieurs chose (mon entrainement, les données sur ma vitesse de frappe ect...).
#  Calcul de Probabilité 
## Probabilité d'Atteindre la Vitesse Optimale
description et info : expliquer comment on trouve la probabilité avec l'aire en dessous de la courbe et comment on fait pour trouver la probabilité de ma vitesse de frappe et mentionne que la fonction de densité de probabilité est complexe à intégrer directement.
## l'approximation de la série de Maclaurin
description et info : Expliquez comment la série de Maclaurin peut être utilisée pour approximer la PDF et faciliter le calcul de l'aire sous la courbe, ce qui est nécessaire pour trouver la probabilité recherchée.
## Intégration et Aire sous la Courbe
Intégrez la fonction de densité de probabilité approximée pour calculer l'aire sous la courbe, ce qui vous donnera la probabilité de dépasser la vitesse de frappe optimale.

# Analyse et Interprétation des Résultats

## Utilisation des Valeurs Z

## Amélioration et Objectifs

# Conclusion et evaluation

# bibliographie
- \begin{thebibliography}{9}  
\bibitem{normal1}  
de Moivre, A. (1738). \textit{The Doctrine of Chances: or, A Method of Calculating the Probabilities of Events in Play}. London: Pearson.  
\bibitem{normal2}  
Patel, J. K., & Read, C. B. (1996). \textit{Handbook of the normal distribution} (Vol. 150). CRC Press.  
\bibitem{normal3}  
Kwak, S. G., & Kim, J. H. (2017). Central limit theorem: the cornerstone of modern statistics. \textit{Korean journal of anesthesiology}, 70(2), 144.  
\bibitem{normal4}  
Walla, P. (2017). Comparison of speed of reading and information processing in five different font styles. \textit{EC Neurology}, 5, 189-192.  
\end{thebibliography}
- 

# Annexe

example :
This topic is about how derivatives are applied in Zeno's arrow paradox. This
paradox basically states that a moving arrow moves no distance at an instant, which lasts
O seconds, as it occupies a space equal to its size, nor does it move at any instant for the
same reason, concluding that the arrow, therefore, has no motion.

Zeno's arrow paradox looks absurd at first glance, as you can see the arrow moving, but
the longer you think about it the more sense it makes. It is a good example of how
complicated can the mathematisation of change be, even when talking about something
as "simple" as movement. I therefore consider it to be extremely interesting, as the
more you investigate the more you understand how complex it can be. Calculus is the
mathematical study of change. For this reason, it can be useful to approach Zeno's arrow
paradox, because accepting the concept of infinity, and of a number approaching to
infinity and zero is necessary to try to find a mathematical solution to the paradox. For
example, Zeno defines an instant as O seconds, but if time was entirely composed of
instants of O seconds, as Zeno assumes, there would not be time at all, and consequently
no movement. Calculus allows as to think of an instant as an infinitely small unit of time,
therefore allowing, in this case, movement to exist. To try to answer Zeno's paradox, I
will use the derivative of the velocity of the arrow (distance over time), and make time
shrink towards zero, which is what happens at each instant during the movement of the
arrow. Hopefully, this will help me explain that the arrow moves an infinitesimal amount
of distance each infinitesimal amount of time, which could be the reason why the arrow
would seem to have no movement at each instant.

Something as essential as change, that happens everywhere at every time, looks like a
quite complicated topic in mathematics, and only a small portion of society can
understand the mathematisation Of change, so this work's main aim is to use calculus to
"solve" Zeno's paradox, and explain Why I consider Zeno was not entirely correct
assuming certain things. It Will also help to understand derivatives and rates Of change,
using Zeno's paradox as an example Of Why is calculus necessary to approach some areas
or cases where other mathematical approaches wouldn't be possible, or would be
ineffective.

\subsection{Calcul de l'Aire sous la Courbe} 

Pour calculer la probabilité que ma vitesse de frappe soit supérieure à la moyenne, nous utiliserons des séries de Maclaurin pour approximer la fonction de densité de probabilité de la distribution normale et l'intégration pour calculer l'aire sous la courbe.

\subsubsection{Approximation avec des Séries de Maclaurin}

La série de Maclaurin pour la fonction exponentielle $e^x$ est donnée par :

\begin{equation}
e^x = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \ldots
\end{equation}

Nous utiliserons cette série pour approximer la fonction de densité de probabilité de la distribution normale autour de zéro.

\subsection{Calcul de l'Aire sous la Courbe}

Pour calculer l'aire sous la courbe de la distribution normale à partir de la moyenne jusqu'à l'infini, nous intégrons la fonction de densité de probabilité approximée :

\begin{equation}
P(X > \bar{x}) = \int_{\bar{x}}^{\infty} f(x) \, dx
\end{equation}

où $f(x)$ est la fonction de densité de probabilité de la distribution normale.

\subsubsection{Résultats du Calcul de Probabilité}

Après avoir effectué l'intégration, nous obtenons la probabilité que ma vitesse de frappe soit supérieure à la moyenne. Les résultats sont les suivants :

\begin{align*}
P(X > \bar{x}) &= \text{Valeur calculée de la probabilité}
\end{align*}

Cela nous donne la probabilité que ma vitesse de frappe dépasse la moyenne calculée de 47.74 WPM.
