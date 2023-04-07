---
tags : mod EE
---
Created: 2023-04-07

In this study, we used a database containing medical conditions and their associated symptoms. The database consists of approximately 10,000 records and is stored in a CSV file.

To preprocess the data, we first removed any duplicate records and then converted the categorical data into numerical values using one-hot encoding. Next, we split the data into a training set and a testing set using the train_test_split function from the scikit-learn (sklearn) library in Python. The training set consists of 80% of the data, and the testing set consists of the remaining 20%.

We then used the two machine learning algorithms provided by the sklearn library, such as logistic regression and linear regression to predict the medical conditions based on the symptoms. To evaluate the performance of these algorithms, we used evaluation metrics such as accuracy, precision, recall, and F1 score. We also used k-fold cross-validation to ensure that our models were not overfitting the data.

Overall, our methodology involved preprocessing the data, splitting it into training and testing sets, and using various machine learning algorithms and evaluation metrics to predict medical conditions based on symptoms.