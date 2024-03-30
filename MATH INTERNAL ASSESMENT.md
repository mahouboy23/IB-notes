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
# ---- ((je connais pas un bon titre court et un titre complet perspicace qui fonctionne ici)

## Dérivées Première et Seconde
description et info : Calculez la première et la seconde dérivée de la PDF, $f'(x)$ et $f''(x)$, pour identifier le comportement de la courbe de la distribution normale, y compris les points critiques et les points d'inflexion.
## Maximum Local et Points d'Inflexion
description et info : Démontrez que la PDF a un maximum local en $x=u$  et des points d'inflexion en $x=u+\sigma$ et $u-\sigma$, ce qui est pertinent pour comprendre la forme de la distribution de votre vitesse de frappe
# Collecte et traitement des Données
## Collecte des Données 
description et info : Décris comment j'ai avez collecté les données de vitesse de frappe sur une période donnée.
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

# Annexe