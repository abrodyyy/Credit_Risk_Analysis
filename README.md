# Credit_Risk_Analysis
Module 18: Supervised Machine Learning and Credit Risk

## Overview
We have been tasted with using our skills in data preparation, statistical reasoning, and machine learning to predict credit card risk. Given that the number of good loans outnumber risky loans, we know that credit risk is an unbalanced classification problem. Unbalanced classification problems occur when the distribution of data is known to be biased or skewed. In order to complete our analysis, we'll need to utalize different techniques to train and evaluate models with unbalanced classes. Specifically, we've been asked to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. Finally, we'll compare two machine learning models that reduce bias - BalancedRandomforestClassifier & EasyEnsembleClassifier. Both models will be able to predice credit risk, but we will need to determine which of the two is the most accurate.


## What You're Creating
This new assignment consists of three technical analysis deliverables and a written report:
- Deliverable 1: Use Resampling Models to Predict Credit Risk.
- Deliverable 2: Use the SMOTEENN Algorithm to Predict Credit Risk.
- Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk.
- Deliverable 4: A Written Report on the Credit Risk Analysis (README.md).


## Resources
- Data Source: [LoanStats_201901.csv]
(https://github.com/abrodyyy/Credit_Risk_ Analysis/blob/main/Resources/LoanStats_ 201901.csv)
- Software:
- [Google Colaboratory] (https://colab. research.google.com)
- [Visual Studio Code, 1.70.21 (https: //code.visualstudio.com/updates/v1 70)
- [Jupyter Notebook 6.4.8] (https://jupyter-notebook. readthedocs.io/_/downloads/en/v6.4.8/pdf/)
- [Python 3.9.12] (https://www.python.org/downloads/release/python-3912/)
    - [imbalanced-learn] (https ://imbalanced-learn.org/stable/)
    - [scikit-learn](https://scikit-learn.org/stable/)


## Results

###### Naive Random Oversampling

![Naive Random Oversampling](https://user-images.githubusercontent.com/111623064/217157402-ae3afbc0-1cb9-462f-b45a-b0f4ddf065e8.png)

- Notes 

###### SMOTE Oversampling

![SMOTE Oversampling](https://user-images.githubusercontent.com/111623064/217157354-0f7a4a5a-3642-42d3-a2c2-f4c21b38779f.png)

- Notes 

###### Undersampling using the Cluster Centroids algorithm

![Undersampling](https://user-images.githubusercontent.com/111623064/217157289-10eb3256-7d6b-4417-911a-ac40886dc701.png)

- Notes 

###### Combination (Over and Under) Sampling using SMOTEENN

![Combination (Over and Under) Sampling](https://user-images.githubusercontent.com/111623064/217157499-5d82f072-27a8-40f9-8818-0ee16dce6fe8.png)

- Notes 

###### Balanced Random Forest Classifier

![Balanced Random Forest Classifier](https://user-images.githubusercontent.com/111623064/217157531-2e59c51e-4e96-43be-a1a1-d7ffdb5351e6.png)

- Notes 

###### Easy Ensemble Classifier

![Easy Ensemble Classifier](https://user-images.githubusercontent.com/111623064/217157554-ea4873ed-96a6-4cd2-a405-86be33fcb685.png)

- Notes 

## Summary
