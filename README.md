# Credit_Risk_Analysis

## Overview of the loan prediction risk analysis:

The purpose of this analysis was to use a credit card credit dataset from LendingClub, a lending services company, to oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. A combination approach was also utilized to over- and undersample using the SMOTEENN algorithm. Lastly, two machine learning models, BalancedRandomForestClassifier and EasyEnsembleClassifier, were used to predict credit risk. In totlal, six different machine learning models were imported to evaluate the credit card dataset and determine the best machine learning model to predict credit risk.

## Results:
The balanced accuracy score, precision, and recall scores of all six machine learning models are listed along with a screenshot of the jupyter notebook.

### RandomOverSampler
![RandomOverSampling](https://user-images.githubusercontent.com/69759624/104092929-d2a5b780-524c-11eb-8d80-9d60e8e0707b.PNG)

####
* When the data is oversampled, the accuracy is low at 0.67 which is the total correct divided by the total number of data points. The precision is low (0.01) resulting from a large number of false positives for the high-risk group. The average recall is also low with an average of 0.59. The RandomOverSampler technique does not do a good job of predicting credit risk. 

### SMOTE Oversampling
![SMOTEoversampling](https://user-images.githubusercontent.com/69759624/104092935-d6393e80-524c-11eb-8da7-83557ec0fea1.PNG)

####
* Again, when the data is oversampled, the accuracy is low at 0.66 which is the total correct divided by the total number of data points. The precision is low (0.01) resulting from a large number of false positives for the high-risk group. The average recall is also low with an average of 0.69. The SMOTE oversampling technique does not do a good job of predicting credit risk. 

### Cluster Centroids Undersampling
![ClusterCentroidsUndersampling](https://user-images.githubusercontent.com/69759624/104092937-d89b9880-524c-11eb-83a6-d1de897634e3.PNG)

####
* When the data is undersampled, the accuracy is low at 0.55 which is the total correct divided by the total number of data points. The precision is low (0.01) resulting from a large number of false positives for the high-risk group. The average recall is very low with an average of 0.41. The ClusterCentroids undersampling technique is less reliable than the oversampling techniques (RandomOverSampler and SMOTE) for predicting credit risk. 

### SMOTEENN Over and Undersampling Combo
![SMOTEENNcombo](https://user-images.githubusercontent.com/69759624/104092939-dafdf280-524c-11eb-8eaf-bb9f81e7fc47.PNG)

* When the data is both over and undersampled, the results are similar to the undersampling techniques. The accuracy is low at 0.64 which is the total correct divided by the total number of data points. The precision is low (0.01) resulting from a large number of false positives for the high-risk group. The average recall is low with an average of 0.57. The combination technique is not a reliable model for predicting credit risk. 

### Balanced Random Forest Classifier (Ensemble)
![RandomForestClassifierEnsemble](https://user-images.githubusercontent.com/69759624/104092943-dcc7b600-524c-11eb-8fbf-ae4dfec2743a.PNG)

* The RandomForestClassifier technique has improved accuracy, precision, and sensitivity results compared to the over and undersampling techniques. The accuracy is 0.79, but the precision for the high-risk group is only slightly higher at 0.03 because of the large number of false positives (n=2153). The average recall is high at 0.87. The ensemble technique produced the best results, due to a random forest consisting of a group or ensemble of individual decision trees. A large group of uncorrelated decision trees produced more accurate and stable results than individual decision trees. However, the number of false positives is concerning.

### AdaBoost Classifier (Ensemble)
![AdaBoostClassifierEnsemble](https://user-images.githubusercontent.com/69759624/104092944-dfc2a680-524c-11eb-94dc-dec324a2ce62.PNG)

* AdaBoost is an iterative ensemble method. The AdaBoost classifier builds a strong classifier by combining multiple poorly performing classifiers in order to get a high accuracy classifier. This technique resulted in the best accuracy, precision, and recall numbers compared to the other machine learning techniques. The accuracy was the highest at 0.93. The average precision was 0.99 and the average recall was 0.92. 

* The results look strong, but there is a low number of true positives (n=93) in the dataset compared to the false positives (n=983) resulting in a precision score of 0.09 for the high risk set. 

## Summary:

* The RandomOverSampler and SMOTE oversampling models did not produce reliable results for predicting credit risk. The ClusterCentroids undersampling and the combination sampling (SMOTEENN) techniques also did not result in models that could be recommended for future work with credit risk. 

* The two ensemble machine learning models resulted in the best accuracy, precision, and recall scores with the AdaBoost iterative model showing slightly better precision scores than the BalancedRandomForestClassifier. My recommendation is to use the AdaBoost technique but increase the dataset to obtain a higher number of high risk data points. The current data set is imbalanced with a relatively small number of high risk data points. There are too many false positives compared to true positives resulting in a low precision score for the high risk group.
