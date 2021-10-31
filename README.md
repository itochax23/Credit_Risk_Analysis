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

There is a bulleted list that describes 
* the balanced accuracy score 
* the precision 
* recall scores of all six machine learning models (15 pt)

## Summary

There is a summary of the results (2 pt)

There is a recommendation on which model to use, or there is no recommendation with a justification (3 pt)
