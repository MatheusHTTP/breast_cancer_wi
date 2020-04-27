# breast_cancer_wi
Jupyter notebook for a model to predict malignancy for breast cancer based on the wisconsin breast cancer dataset

In this project we build a model to predict whether or not tumours are benign or malignant. We use the Wisconsin Breast Cancer Dataset located here: http://archive.ics.uci.edu/ml/datasets/breast+cancer+wisconsin+(diagnostic)

We first do some prelimary exploration of the data. This is followed by a number of feature engineering steps that involve transformations of the data. Once we have prepared the data we split the data into a training set and a test set.

We then experiment with a number of different models and hyperparameter combinations. We train the combinations using hold out validation with the GridSearchCV class using only the training set. For each best combination we then run predictions on the test set to get a score. We use recall as the primary error metric under the assumption that we don't want to incorrectly classify a malignant tumour as benign. We encoded the diagnostic label column to have values 1 - malignant, 0 - benign.

We use precision and roc_auc as secondary error metrics.

Once we have identified a number of best estimators among the classifier type/ hyperparameter combinations we then use them to create an ensemble voting classifier to produce a final result using the test data set.

We organize the code into a series of classes and functions that can be used to perform the various data transformation and model testing tasks required.
