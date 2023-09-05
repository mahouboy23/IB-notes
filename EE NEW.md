---
tags:
  - mod
  - EE
---
Created: 2023-09-05

## Introduction

La détection des défauts dans les produits industriels tels que les semi-conducteurs et les pièces de machines est cruciale pour le contrôle de la qualité et l'amélioration des processus. Cependant, la détection manuelle des défauts est fastidieuse, incohérente et peu fiable. Les réseaux neuronaux convolutifs (CNN) sont apparus comme une technique prometteuse pour la détection visuelle automatisée des défauts. Mais les performances des CNN dépendent fortement du réglage approprié des hyperparamètres. Cet essai vise à comparer deux algorithmes d'optimisation - l'optimisation par essaims de particules (PSO) et les algorithmes génétiques (GA) - pour optimiser les hyperparamètres d'une architecture CNN pour la détection des défauts dans les images de produits industriels.

Les CNN ont révolutionné la vision par ordinateur grâce à leur capacité à apprendre automatiquement des hiérarchies spatiales de caractéristiques. Cependant, l'apprentissage des CNN nécessite un réglage approfondi des hyperparamètres, qui est souvent effectué manuellement par essais et erreurs. Les algorithmes d'optimisation tels que PSO et GA peuvent automatiser ce processus en recherchant intelligemment l'espace des hyperparamètres. Le PSO s'inspire du comportement social d'organismes tels que les volées d'oiseaux, tandis que les GA imitent l'évolution biologique. Cet essai évaluera leur efficacité dans la recherche des hyperparamètres CNN optimaux pour maximiser la précision de la détection des défauts.

## Contexte

### Hyperparamètres de CNN

Les CNN ont plusieurs hyperparamètres qui doivent être réglés, notamment le nombre et la taille des filtres, le nombre de couches, le taux d'abandon, la taille du lot, le taux d'apprentissage, etc. La configuration optimale de ces hyperparamètres peut avoir un impact significatif sur la capacité du CNN à apprendre des caractéristiques efficaces et à bien se généraliser. Le réglage manuel est inefficace et la recherche de la meilleure combinaison d'hyperparamètres est difficile en raison de l'étendue de l'espace de recherche. Les algorithmes d'optimisation sont donc bien adaptés à l'automatisation du processus de réglage des hyperparamètres du CNN.
### Optimisation par essaim de particules

Le PSO s'inspire du mouvement collectif d'organismes tels que la volée d'oiseaux. Elle maintient un essaim de solutions candidates, appelées particules, qui se déplacent dans l'espace de recherche hyperparamétrique pour trouver l'optimum global. Chaque particule a une position et une vitesse qui sont mises à jour à chaque itération en fonction de sa meilleure position connue et de la meilleure position globale de l'essaim. Les particules sont attirées vers ces meilleures positions de manière stochastique. Le PSO équilibre l'exploration et l'exploitation de l'espace de recherche grâce à quelques paramètres seulement, ce qui le rend facile à mettre en œuvre.
### Algorithmes génétiques

Les AG sont basés sur le processus de sélection naturelle. Une population de solutions candidates, appelées chromosomes, est maintenue. À chaque génération, l'aptitude des chromosomes est évaluée et les plus aptes sont sélectionnés pour le croisement et la mutation afin de produire la progéniture de la génération suivante. Le croisement combine des parties de deux chromosomes, tandis que la mutation introduit des changements aléatoires. Au fil des générations successives, l'aptitude moyenne de la population tend à augmenter et à converger vers des solutions optimales. Mais les AG peuvent être coûteux en termes de calcul en raison des évaluations de l'aptitude.
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