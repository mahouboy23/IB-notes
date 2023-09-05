---
tags:
  - mod
  - EE
---
Created: 2023-09-05

## Introduction

La détection de défauts sur des produits industriels tels que les semi-conducteurs et les pièces de machinerie est cruciale pour le contrôle qualité et l'amélioration des processus. Cependant, la détection manuelle de défauts est fastidieuse, inconstante et peu fiable. Les réseaux de neurones convolutifs (CNN) se sont imposés comme une technique prometteuse pour la détection visuelle automatisée de défauts. Mais les performances des CNN dépendent fortement du réglage approprié des hyperparamètres. Ce memoire vise à comparer deux algorithmes d'optimisation - l'optimisation par essaim de particules (PSO) et les algorithmes génétiques (AG) - pour optimiser les hyperparamètres d'une architecture de CNN pour la détection de défauts sur des images de produits industriels.

Les CNN ont révolutionné la vision d'ordinateur par leur capacité à apprendre automatiquement des hiérarchies spatiales de caractéristiques. Cependant, l'entraînement des CNN nécessite un réglage minutieux des hyperparamètres, souvent effectué par essais-erreurs manuels. Des algorithmes d'optimisation tels que le PSO et les AG peuvent automatiser ce processus en explorant de manière intelligente l'espace des hyperparamètres. Le PSO s'inspire du comportement social d'organismes comme les vols d'oiseaux, tandis que les AG mimtent l'évolution biologique. Cet essai évaluera leur efficacité à trouver des hyperparamètres CNN optimaux permettant de maximiser la précision de détection de défauts.

## Contexte

### Hyperparamètres de CNN

Les CNN comportent divers hyperparamètres à régler, dont le nombre et la taille des filtres, le nombre de couches, le taux d'abandon, la taille de lot, le taux d'apprentissage, etc. La configuration optimale de ces hyperparamètres peut avoir un impact significatif sur la capacité du CNN à apprendre des caractéristiques efficaces et à bien généraliser. Le réglage manuel est inefficient et trouver la meilleurecombinaison d'hyperparamètres est difficile vu l'immensité de l'espace de recherche. Les algorithmes d'optimisation sont donc bien adaptés pour automatiser le processus de réglage des hyperparamètres des CNN.

### Optimisation par essaim de particules

Le PSO s'inspire du mouvement collectif d'organismes tels que les vols d'oiseaux. Il maintient un essaim de solutions candidates appelées particules, qui explorent l'espace des hyperparamètres à la recherche du optimum global. Chaque particule possède une position et une vitesse mises à jour en fonction de sa meilleure position connue et de la meilleure position globale de l'essaim à chaque itération. Les particules sont attirées stochastiquement vers ces meilleures positions. Le PSO équilibre exploration et exploitation de l'espace de recherche à travers peu de paramètres, le rendant facile à mettre en œuvre.

### Algorithmes génétiques

Les AG s'inspirent du processus de sélection naturelle. Une population de solutions candidates appelées chromosomes est maintenue. À chaque génération, l'adaptabilité des chromosomes est évaluée et les plus adaptés sont sélectionnés pour le croisement et la mutation afin de produire une nouvelle progéniture pour la génération suivante. Le croisement combine des parties de deux chromosomes tandis que la mutation introduit des changements aléatoires. Au fil des générations successives, l'adaptabilité moyenne de la population tend à augmenter, convergeant vers des solutions optimales. Mais les AG peuvent être coûteux en calculs en raison des évaluations d'adaptabilité.

## Méthodologie

Le jeu de données MVTec AD contenant plus de 5000 images haute résolution de produits industriels sera utilisé. Les images présentent des annotations au niveau des pixels pour différents types de défauts tels que rayures et bosses.

80% des images serviront à l'entraînement du CNN et à la validation des configurations d'hyperparamètres trouvées par les algorithmes d'optimisation. Les 20% restants constitueront un ensemble de test non vu pour l'évaluation finale.

Une architecture de CNN sera définie avec des couches convolutives, de mise en pool et totalement connectées. L'activation ReLU et l'optimiseur Adam seront utilisés pour un entraînement efficace. Les hyperparamètres à optimiser sont:

Taille des filtres  
Nombre de filtres par couche  
Taux de renoncement  
Taille de lot  
Taux d'apprentissage  
Le PSO et les AG seront mis en œuvre pour rechercher les valeurs optimales d'hyperparamètres maximisant la précision de validation sur 50 générations avec une population de 50 particules/chromosomes. La précision de détection de défauts sur l'ensemble de test sera mesurée avec la meilleure configuration trouvée par chaque algorithme.

Les hyperparamètres, la précision de validation et la vitesse de convergence seront analysés pour évaluer l'efficacité du PSO par rapport aux AG. L'algorithme obtenant la plus haute précision de test en moins de générations sera considéré comme le plus efficace.

Conclusion

Cet essai compare le PSO et les AG pour l'optimisation des hyperparamètres des CNN dans le contexte de la détection automatisée de défauts. La méthodologie analyse leurs performances sur la base de la précision de test, des hyperparamètres optimaux et de la vitesse de convergence. Les résultats fourniront un éclairage sur leur adéquation à l'optimisation automatisée des hyperparamètres dans les CNN pour des tâches de vision par ordinateur.