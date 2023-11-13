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

### Les réseaux neuronaux convolutifs (CNN) 
Les réseaux de neurones convolutifs (CNN) tirent leur nom de leur opération fondamentale : la convolution. Celle-ci leur permet d'analyser efficacement des données d'entrée de type matriciel, telles que des images numériques. Une image numérique peut en effet être représentée par une matrice multidimensionnelle, où chaque pixel correspond à une valeur dans la matrice.

Dans un CNN, les données d'entrée passent d'abord par une ou plusieurs couches de convolution. Chaque couche de convolution applique des filtres de convolution, également appelés noyaux, sur l'ensemble de l'image. Un filtre de convolution est simplement une petite matrice, généralement de 3x3 ou 5x5 pixels. Lorsqu'un filtre est appliqué, il "balaie" l'image entière en effectuant le produit matriciel entre le filtre et les patches (portions) correspondantes de l'image. Cela permet d'extraire des caractéristiques visuelles élémentaires telles que les contours, les coins ou les textures.

Plus précisément, lorsqu'un filtre est déplacé sur l'image, les valeurs des pixels à l'intérieur du filtre sont multipliées aux poids du filtre, puis sommées. Le résultat de cette opération est stocké dans une nouvelle matrice appelée carte de caractéristiques, à la même position que le filtre sur l'image originale. Ainsi, l'application d'un filtre sur une image produit une carte de caractéristiques qui code la présence ou l'absence de la caractéristique détectée par ce filtre à chaque emplacement spatial.

Pour une couche de convolution complète, cette opération est répétée pour de nombreux filtres différents, chacun étant conçu pour détecter un type spécifique de caractéristique. Cela produit un ensemble de cartes de caractéristiques codant diverses informations contenues dans l'image d'origine. Les couches suivantes traitent ces cartes de caractéristiques de manière hiérarchique pour produire des représentations de plus haut niveau.

Les couches de convolution successives permettent d'extraire des caractéristiques de plus en plus complexes, comme des motifs, des objets et finalement des concepts de haut niveau. Grâce à cette architecture en couches, les CNN peuvent apprendre de manière autonome à représenter le contenu des images de façon efficace pour la tâche visée, sans avoir recours à des caractéristiques manuellement conçues. C'est ce qui les rend si performants pour des problématiques telles que la détection visuelle de défauts, comme nous le verrons par la suite.

### Hyperparamètres de CNN

Les CNN ont plusieurs hyperparamètres qui doivent être réglés, notamment le nombre et la taille des filtres, le nombre de couches, le taux d'abandon, la taille du lot, le taux d'apprentissage, etc. La configuration optimale de ces hyperparamètres peut avoir un impact significatif sur la capacité du CNN à apprendre des caractéristiques efficaces et à bien se généraliser. Le réglage manuel est inefficace et la recherche de la meilleure combinaison d'hyperparamètres est difficile en raison de l'étendue de l'espace de recherche. Les algorithmes d'optimisation sont donc bien adaptés à l'automatisation du processus de réglage des hyperparamètres du CNN.
### Optimisation par essaim de particules

Le PSO s'inspire du mouvement collectif d'organismes tels que la volée d'oiseaux. Elle maintient un essaim de solutions candidates, appelées particules, qui se déplacent dans l'espace de recherche hyperparamètre pour trouver l'optimum global. Chaque particule a une position et une vitesse qui sont mises à jour à chaque itération en fonction de sa meilleure position connue et de la meilleure position globale de l'essaim. Les particules sont attirées vers ces meilleures positions de manière stochastique. Le PSO équilibre l'exploration et l'exploitation de l'espace de recherche grâce à quelques paramètres seulement, ce qui le rend facile à mettre en œuvre.
### Algorithmes génétiques

Les AG sont basés sur le processus de sélection naturelle. Une population de solutions candidates, appelées chromosomes, est maintenue. À chaque génération, l'aptitude des chromosomes est évaluée et les plus aptes sont sélectionnés pour le croisement et la mutation afin de produire la progéniture de la génération suivante. Le croisement combine des parties de deux chromosomes, tandis que la mutation introduit des changements aléatoires. Au fil des générations successives, l'aptitude moyenne de la population tend à augmenter et à converger vers des solutions optimales. Mais les AG peuvent être coûteux en termes de calcul en raison des évaluations de l'aptitude.

## Méthodologie et expérience

Pour évaluer l'efficacité du PSO et des AG pour l'optimisation des hyperparamètres de CNN, la procédure suivante a été suivie :

1. Choix du jeu de données MVTEC contenant des images de produits industriels défectueux et non défectueux issues de 15 catégories.
    
2. Conception d'une architecture CNN pour la détection de défauts.
    
3. Implémentation du PSO et des AG pour chercher la configuration optimale des hyperparamètres à optimiser tels que le taux d'apprentissage et le taux de dropout.
    
4. Entraînement des modèles CNN avec les hyperparamètres optimaux.
    
5. Évaluation et comparaison des performances des modèles optimisés.
    

Le jeu de données MVTEC Anomaly Detection a été utilisé. Il contient des images de qualité industrielle de 15 catégories de produits présentant divers défauts, avec séparation en ensembles d'entraînement, validation et test. Les images présentent une grande variété de défauts réalistes tels que des rayures, des impacts ou des infiltrations. La résolution des images varie selon les catégories de 64x64 à 1024x1024 pixels.

Un CNN à 5 couches de convolution et 3 couches complètement connectées a été conçu pour traiter ce jeu de données. Des filtres convolutionnels de taille 3x3 ont été appliqués avec un taux de 0,5 dans les couches de dropout pour prévenir le surapprentissage. La fonction d'activation ReLU a été choisie pour sa rapidité de calcul. En sortie, deux unités fully-connected avec l'activation sigmoid prédisent la présence ou l'absence de défaut à chaque pixel. L'entropie binaire croisée mesure l'erreur de détection à minimiser.

Les hyperparamètres à optimiser sont le taux d'apprentissage initial, le taux de dropout et les tailles de filtre. Le PSO et les AG ont été implémentés dans TensorFlow en Python. Le PSO maintient un essaim de 50 particules représentant des configurations d'hyperparamètres, avec des positions et vitesses mises à jour à chaque itération. Les AG codent les hyperparamètres dans des chromosomes, et opèrent sur une population de 100 individus sur 50 générations avec sélection élitiste, croisement à un point et mutation ponctuelle.

Ces algorithmes évaluent la précision du CNN correspondant sur le lot de validation comme métrique de fitness. Le meilleur individu final définit la configuration optimale. Celle-ci entraîne alors le modèle CNN sur 10 epochs, évalué sur la validation à chaque fois. Enfin, les performances sur le lot de test du meilleur modèle sélectionné sont mesurées.

Cette méthodologie permet de comparer de façon approfondie le PSO et les AG pour l'optimisation des CNN de détection de défauts industriels, en s'assurant que la conception, l'implémentation et les procédures d'évaluation soient bien équitables entre les deux algorithmes.