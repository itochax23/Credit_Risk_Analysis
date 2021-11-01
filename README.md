# Credit_Risk_Analysis

## Overview
The purpose of this project is to apply machine learning to solve a real-world challenge: credit card risk.

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, we use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we've: 
1. Oversampled the data using the RandomOverSampler and SMOTE algorithms, 
2. Undersampled the data using the ClusterCentroids algorithm. 
3. Used a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. 
4. Compared two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. 

## Results

### Naive Random Oversampling
* Balanced accuracy score is 63.7%
* Precision for high risk is very low at 1%
* Recall for high risk is 65%
<img src="https://github.com/itochax23/Credit_Risk_Analysis/blob/5e9337e0a6eb669cdb87234d1c53fb7c244d4f5a/Resources/NaiveRandomOversampling.png" width="70%">

### SMOTE Oversampling
* Balanced accuracy score is around 64%
* Precision for high risk is also very low at 1%
* Recall for high risk is 69%
<img src="https://github.com/itochax23/Credit_Risk_Analysis/blob/5e9337e0a6eb669cdb87234d1c53fb7c244d4f5a/Resources/SMOTEOversampling.png" width="70%">

### Undersampling
* Balanced accuracy score is 66.3%
* Precision for high risk is very low at 1%
* Recall has an average/total of 40%
<img src="https://github.com/itochax23/Credit_Risk_Analysis/blob/5e9337e0a6eb669cdb87234d1c53fb7c244d4f5a/Resources/Undersampling.png" width="70%">

### Combination Sampling
* Balanced accuracy score is 54.3%
* Precision for high risk is very low at 1%
* Recall average/total is 57%
<img src="https://github.com/itochax23/Credit_Risk_Analysis/blob/5e9337e0a6eb669cdb87234d1c53fb7c244d4f5a/Resources/CombinationSampling.png" width="70%">

## Ensemble Learners
In comparing two models using the training data, we used ensemble algorithms to determine best performance. The following steps were taken in each case:
1. Trained the model using the training data.
1. Calculated the balanced accuracy score from sklearn.metrics.
1. Printed the confusion matrix from sklearn.metrics.
1. Generated a classication report using the imbalanced_classification_report from imbalanced-learn.
1. For the Balanced Random Forest Classifier onely, printed the feature importance sorted in descending order (most important feature to least important) along with the feature score
Note: we used a random state of 1 for each algorithm to ensure consistency between tests

### Balanced Random Forest Classifier
* Balanced accuracy score is around 77.2%
* Precision for high risk is very low at 0.03
* Recall average/total is nearly 90%
<img src="https://github.com/itochax23/Credit_Risk_Analysis/blob/5e9337e0a6eb669cdb87234d1c53fb7c244d4f5a/Resources/BalancedRandomForestClassifier.png" width="70%">

### Easy Ensemble AdaBoost Classifier
* Balanced accuracy score is 91.7%
* Precision is 0.09
* Recall is 94%
<img src="https://github.com/itochax23/Credit_Risk_Analysis/blob/bace984fc5c083f4c2b01c19325ce272c803bec0/Resources/EasyEnsembleAdaBoostClassifier.png" width="70%">

## Summary

* The first four resampling models included undersampling, oversampling, and a combination of both to try to find out which was best at predicting loans with high risk. The next models used ensemble classifiers to predict which loans were high or low risk. 
* The first four models performed less accurately than the ensemble classifiers.  
* The ensemble learners had the best balance of all tthe models with high accuracy and good balance of precision and recall, and the Easy Ensemble AdaBoost Classifier is recommended over the others.
