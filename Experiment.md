---
tags : mod EE
---
Created: 2023-07-14

1. Download and understand the MVTEC Anomaly Detection dataset. This includes:

- Images of defect-free and defective industrial products from 15 categories
- Knowing the train, test and validation splits provided
- Understanding the different types of defects in each category

2. Design your CNN architecture for defect detection. This will depend on:

- Number of categories and image sizes
- Types of layers needed - convolutional, pooling, dropout, etc.
- Number of filters and filter sizes in convolutional layers
- Number of units in fully connected layers
- Activation functions
- Loss function - could use binary cross entropy

3. Implement PSO and genetic algorithm to optimize CNN hyperparameters:

- Determine which hyperparameters to optimize - learning rate, dropout rate, filter sizes, etc.
- Implement the PSO and genetic algorithm optimization routines in code
- Determine population sizes and other algorithm parameters
- Track the best fitness (accuracy, AUC, etc.) at each iteration

4. Train and evaluate the CNN models with optimized hyperparameters:

- Compile your CNN model with optimized hyperparameters from the algorithms
- Split the dataset into train, validation and test sets
- Train the CNN model on the train set for a fixed number of epochs
- Evaluate accuracy, loss and AUC on the validation set at end of each epoch
- Select the model with best validation performance

5. Compare the performance of optimized CNN models:

- Compare accuracy, loss and AUC of models from PSO vs genetic algorithm
- Analyze how optimized hyperparameters differ between algorithms
- Discuss advantages and limitations of each optimization algorithm

6. Perform additional runs of the experiments to verify results and reduce variance.
7. Perform statistical analysis to test for significance of results.
8. Analyze defects detected and errors made by the optimized CNN models.
9. Discuss challenges faced and recommendations for future improvements.