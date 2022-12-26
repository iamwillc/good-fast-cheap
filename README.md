# **Good Fast Cheap Constraints - Group Project**
---
## Problem Statement
---
The goal is to create the best-performing model on a hold-out sample of data with constrained optimization. The idea is that for any project you can have any two of these. You can have good work done cheaply, but it will take a long time. You can have good work done fast, but it won't be cheap. Or you can have work done fast and on the cheap, but it won't be good. Our team was given the constraint of having a maximum of 20 features fit into the model. The task is to predict if a person's income is more than \\$50,000 given certain profile information and to generate the labels for income above $50,000.
![](https://berkonomics.com/wp-content/uploads/2015/11/goodfastcheap1-1.png)

## Analysis Summary
---
#### *Data Wrangling & Cleaning*
The dataset had columns we decided were multicollinear such as the capital-gain and capital-loss columns which were combined into a net-capital column as the capital-loss subtracted from the capital-gain column equates to the net capital. The native-us column was mapped to give the data better precision as there aren't many non-US native-country values. The column to be predicted was the wage column but the values were in a string format so it was mapped to 0 and 1 so it will fit into the models. 
#### *Modeling & Accuracy of Models*
---
The baseline for the model is an accuracy of 75.9% as predicting 0s will return 75.9% of the dataset as correct. The models fit were KNeighborsClassifier, RandomForestClassifier, and GradientBoosting, with all of them grid-searched to seek the best parameters.
## Conclusions and Recommendations
---
The grid-searched KNearestNeighbors model returned an f1 score of 68.6% for the training set, and 63.7% for the testing set. As for the RandomForest model, the f1 score was worse at 60.8% for training and 61.7% for testing. With the GradientBoosting model, the training set had a 70.9% f1 score and the testing has a 69.2% score, returning this model as the best model among the three. 