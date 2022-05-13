# Project Overview
This project repository is created to classify a car into one of the 4 usability conditions(unacceptable, acceptable, good, very good) based on 7 features. It is a multi class classification problem.

## Key Question
Each car evaluation is described with 7 attributes. 6 of the attributes represent car characteristics, such as buying price, price of the maintenance, number of doors, capacity in terms of persons to carry, the size of luggage boot, and estimated safety of the car. The seventh variable represents the evaluation of the car (unacceptable, acceptable, good, very good). 
The idea is to predict the evaluation of the cars based on their characteristics.


## Dataset
The dataset is from UCI machine learning repository. There are no missing values in the dataset.
Class distribution: ]
unacc: 70%
acc: 22%
Other (134): 8%

Data Source Link: http://archive.ics.uci.edu/ml/datasets/Car+Evaluation


## Approach
- Some initial EDA and anomaly detection checks are performed
- Ordinal mapping has been used instead of categorical variable conversion to retain the orderWeights are assigned to orginal variables based on their levels
- Several classification models are tried with and without grid search and their results are noted. A holistic comparison is done to assess which models performed better
- The following models were tried: KNN, Decision Tree, Logistic Regression, SVC

## Results
The data was then standardized for usage in the KNN and logistic regression models because in KNN distance has to be calculated and Logistic is using regularization

The models were built using both normal hyperparameter tuning and grid search CV to identify best set of parameters and the performance was measured in terms of Accuracy, Precision, recall, AUC score, and confusion matrix. MCC and Cohen's Kappa was checked to evaluate multi-class classification.

Using the above specifications, both overfitting and underfitting were assessed and relevant steps were taken to avoid the issue. The best metrics and their performances have been summarised and suitable models have been recommended based on evidence.

Based on the above results, it can be said that KNN and SVC are the best performing because not only do they have high accuracy but also high MCC and 
Kappa. This leads to the conclusion that these models are able to model the multiple classes effectively
