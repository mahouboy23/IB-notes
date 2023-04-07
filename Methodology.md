---
tags : mod EE
---
Created: 2023-04-07

ENGLISH
In this study, we used a database containing medical conditions and their associated symptoms. The database consists of approximately 10,000 records and is stored in a CSV file.

To preprocess the data, we first removed any duplicate records and then converted the categorical data into numerical values using one-hot encoding. Next, we split the data into a training set and a testing set using the train_test_split function from the scikit-learn (sklearn) library in Python. The training set consists of 80% of the data, and the testing set consists of the remaining 20%.

We then used the two machine learning algorithms provided by the sklearn library, such as logistic regression and linear regression to predict the medical conditions based on the symptoms. To evaluate the performance of these algorithms, we used evaluation metrics such as accuracy, precision, recall, and F1 score. We also used k-fold cross-validation to ensure that our models were not overfitting the data.

Overall, our methodology involved preprocessing the data, splitting it into training and testing sets, and using various machine learning algorithms and evaluation metrics to predict medical conditions based on symptoms.

FRENCH
Dans cette étude, nous avons utilisé une base de données contenant des conditions médicales et leurs symptômes associés. La base de données comprend environ 10 000 enregistrements et est stockée dans un fichier CSV.

Pour prétraiter les données, nous avons d'abord supprimé tous les enregistrements en double, puis converti les données catégorielles en valeurs numériques à l'aide d'un codage à une touche. Ensuite, nous avons divisé les données en un ensemble de formation et un ensemble de test à l'aide de la fonction train_test_split de la bibliothèque scikit-learn (sklearn) en Python. L'ensemble de formation est constitué de 80 % des données et l'ensemble de test des 20 % restants.

Nous avons ensuite utilisé les deux algorithmes d'apprentissage automatique fournis par la bibliothèque sklearn, tels que la régression logistique et la régression linéaire, pour prédire les pathologies sur la base des symptômes. Pour évaluer les performances de ces algorithmes, nous avons utilisé des mesures d'évaluation telles que l'exactitude, la précision, le rappel et le score F1. Nous avons également utilisé la validation croisée k-fold pour nous assurer que nos modèles n'étaient pas surajoutés aux données.

Dans l'ensemble, notre méthodologie a consisté à prétraiter les données, à les diviser en ensembles de formation et de test, et à utiliser divers algorithmes d'apprentissage automatique et mesures d'évaluation pour prédire les conditions médicales sur la base des symptômes.

