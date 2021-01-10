# Credit_Risk_Analysis

## Overview of the loan prediction risk analysis:

The purpose of this analysis is to use a credit card credit dataset from LendingClub, a lending services company, to oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. A combination approach was also utilized to over- and undersample using the SMOTEENN algorithm. Lastly, two machine learning models were used that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Six different machine learning models were imported to evaluate the the credit card dataset for credit risk, and determine the best machine learning model to predict credit risk.

## Results:
Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.
### RandomOverSampler
![RandomOverSampling](https://user-images.githubusercontent.com/69759624/104092929-d2a5b780-524c-11eb-8d80-9d60e8e0707b.PNG)

####
When the data is oversampled, the accuracy is low at 0.67 which is the total correct divided by the total number of data points. The precision is low (0.01) resulting from a large number of false positives for the high-risk group. The average recall is also low with an average of 0.59. The RandomOverSampler technique does not do a good job of predicting credit risk. 

### SMOTE Oversampling
![SMOTEoversampling](https://user-images.githubusercontent.com/69759624/104092935-d6393e80-524c-11eb-8da7-83557ec0fea1.PNG)

####
Again, when the data is oversampled, the accuracy is low at 0.66 which is the total correct divided by the total number of data points. The precision is low (0.01) resulting from a large number of false positives for the high-risk group. The average recall is also low with an average of 0.69. The SMOTE oversampling technique does not do a good job of predicting credit risk. 

### Cluster Centroids Undersampling
![ClusterCentroidsUndersampling](https://user-images.githubusercontent.com/69759624/104092937-d89b9880-524c-11eb-83a6-d1de897634e3.PNG)

####
When the data is undersampled, the accuracy is low at 0.55 which is the total correct divided by the total number of data points. The precision is low (0.01) resulting from a large number of false positives for the high-risk group. The average recall is very low with an average of 0.41. The undersampling technique is less reliable than the oversampling techniques (RandomOverSampler and SMOTE) for predicting credit risk. 

### SMOTEENN Over and Undersampling Combo
![SMOTEENNcombo](https://user-images.githubusercontent.com/69759624/104092939-dafdf280-524c-11eb-8eaf-bb9f81e7fc47.PNG)

### Balanced Random Forest Classifier (Ensemble)
![RandomForestClassifierEnsemble](https://user-images.githubusercontent.com/69759624/104092943-dcc7b600-524c-11eb-8fbf-ae4dfec2743a.PNG)

### AdaBoost Classifier (Ensemble)
![AdaBoostClassifierEnsemble](https://user-images.githubusercontent.com/69759624/104092944-dfc2a680-524c-11eb-94dc-dec324a2ce62.PNG)

## Summary:

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. (2 pt)
or there is no recommendation with a justification (3 pt)
