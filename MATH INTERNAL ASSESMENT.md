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
	2. **Application des distributions normales/binomiales:**
	    
	    - Analysez si les données globales sur la vitesse de frappe suivent une distribution normale ou binomiale.
	    - Utilisez les données pour calculer la probabilité que ma vitesse de frappe soit supérieure à la moyenne.
	3. **Test du chi-carré:**
	    
	    - Effectuez un test du chi-carré pour comparer vos données à la moyenne globale et déterminer s'il existe une différence significative.
	4. **Utilisation des séries de Maclaurin et de l'intégration:**
	    
	    - Appliquez les séries de Maclaurin pour approximer les fonctions utilisées dans votre analyse.
	    - Utilisez l'intégration pour analyser des modèles de données continues sur la période pendant laquelle vous avez enregistré vos vitesses de frappe.
	
	#### Conclusion
	
	- Résumez les résultats de l'analyse statistique.
	- Déterminez si votre vitesse de frappe est significativement différente de la moyenne mondiale.
	- Discutez des implications de vos résultats et des domaines potentiels de recherche.
	
	### Références et recherches complémentaires
	
	- Manuels statistiques:** Consultez les manuels statistiques standard pour comprendre et appliquer les tests chi-carré, les distributions normales/binomiales et les séries de Maclaurin.
	- Logiciels mathématiques:** Envisagez d'utiliser des logiciels tels que R ou Python pour l'analyse et la visualisation des données.



Data : 
![[image-20240109160339608.png]]

![[image-20240109162205173.png]]


ok also add to the code so that it also gives the data table and make sure that the data follows a normal distribution and up the  test cases to 100

but now give me the python code, just the python code to make the graph AND the table of all the data of the test cases
STDOUT/STDERR

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

no but print it as a pandas data table or something more organised and not text based

