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

# SOMMAIRE A REFAIRE
# Numérotation des pages

I want you to make a 500 words essay that goes into my extended essay explaining the concept of CNN, how it works with somme formulas for explanation and explain the parts of matrices in CNN. Also make it fit into my extended essay and make it so that it can transition on to what i did in my extended essay Hyperparamètres de CNN. Of course everything has to be in french just like my extended essay for the ib program in computer science.

### III. Méthodologie et expérience

#### Procédure expérimentale

Pour évaluer l'efficacité du PSO et des AG pour l'optimisation des hyperparamètres de CNN, la procédure suivante a été suivie :

1. Choix du jeu de données MVTEC contenant des images de produits industriels défectueux et non défectueux issues de 15 catégories.
    
2. Conception d'une architecture CNN pour la détection de défauts.
    
3. Implémentation du PSO et des AG pour chercher la configuration optimale des hyperparamètres à optimiser tels que le taux d'apprentissage et le taux de dropout.
    
4. Entraînement des modèles CNN avec les hyperparamètres optimaux.
    
5. Évaluation et comparaison des performances des modèles optimisés.
    

#### Jeu de données

Le jeu de données MVTEC Anomaly Detection a été choisi car il contient des images réalistes de défauts industriels dans différentes catégories. Les lots d'entraînement, de validation et de test fournis facilitent l'évaluation des performances.

#### Architecture CNN

Un modèle CNN à 5 couches de convolution et 3 couches complètement connectées a été conçu en fonction de la taille des images MVTEC. Les couches utilisent des filtres de taille 3x3, un taux de dropout de 0,5 et la fonction d'activation ReLU. La fonction de coût utilisée est l'entropie binaire croisée.

#### Implémentation de PSO et AG

Le PSO et les AG ont été codés pour chercher les valeurs optimales du taux d'apprentissage, du taux de dropout et de la taille des filtres. Leur précision de détection sur le lot de validation sert de métrique de fitness.

#### Entraînement et évaluation

Les modèles CNN ont été entraînés sur 10 epochs avec les hyperparamètres optimaux, évalués sur le lot de validation à chaque epoch, et les performances du meilleur modèle ont été mesurées sur le lot de test.
Cette méthodologie permettra de comparer de manière équitable les algorithmes PSO et AG pour l'apprentissage des hyperparamètres de CNN de détection de défauts.


ok the big lines are good but try to implement and explain everything in one text but each paragraph relates to on of the titles and go into more details explain more each part and make it longer but still needs to be in french and relate to my extended essay.
