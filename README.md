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
- Data Source: [LoanStats_201901.csv](https://github.com/abrodyyy/Credit_Risk_ Analysis/blob/main/Resources/LoanStats_ 201901.csv)
- Software:
- [Google Colaboratory](https://colab. research.google.com)
- [Visual Studio Code, 1.70.21](https: //code.visualstudio.com/updates/v1 70)
- [Jupyter Notebook 6.4.8](https://jupyter-notebook. readthedocs.io/_/downloads/en/v6.4.8/pdf/)
- [Python 3.9.12](https://www.python.org/downloads/release/python-3912/)
    - [imbalanced-learn](https ://imbalanced-learn.org/stable/)
    - [scikit-learn](https://scikit-learn.org/stable/)


## Results

###### Naive Random Oversampling

![Naive Random Oversampling](https://user-images.githubusercontent.com/111623064/217157402-ae3afbc0-1cb9-462f-b45a-b0f4ddf065e8.png)

- Balanced Accuracy Score is 66.45% 
- Precision and Recal Scores: 
    - High Risk: Precision rate is only 1%, and the sensitivity/ recall score is only 72%
    - Low Risk:  Precision rate is 100%, but the sensitivity/ recall score is only 61%
    - Average: Precision rate is 99%, but the sensitivity/ recall score is only 61%

Based on the information above, we can determine this is a poor fit for our model. 

###### SMOTE Oversampling

![SMOTE Oversampling](https://user-images.githubusercontent.com/111623064/217157354-0f7a4a5a-3642-42d3-a2c2-f4c21b38779f.png)

- Balanced Accuracy Score is 66.29% 
- Precision and Recal Scores: 
    - High Risk: Precision rate is only 1%, and the sensitivity/ recall score is only 63%
    - Low Risk:  Precision rate is 100%, but the sensitivity/ recall score is only 69%
    - Average: Precision rate is 99%, but the sensitivity/ recall score is only 69%

Based on the information above, we can determine this algorithm is a poor fit for our prediction model. 

###### Undersampling using the Cluster Centroids algorithm

![Undersampling](https://user-images.githubusercontent.com/111623064/217157289-10eb3256-7d6b-4417-911a-ac40886dc701.png)

- Balanced Accuracy Score is 54.43% 
- Precision and Recal Scores: 
    - High Risk: Precision rate is only 1%, and the sensitivity/ recall score is only 69%
    - Low Risk:  Precision rate is 100%, but the sensitivity/ recall score is only 40%
    - Average: Precision rate is 99%, but the sensitivity/ recall score is only 40%

Based on the information above, we can determine this algorithm is a poor fit for our prediction model. 

###### Combination (Over and Under) Sampling using SMOTEENN

![Combination (Over and Under) Sampling](https://user-images.githubusercontent.com/111623064/217157499-5d82f072-27a8-40f9-8818-0ee16dce6fe8.png)

- Balanced Accuracy Score is 68.25%
- Precision and Recal Scores: 
    - High Risk: Precision rate is only 1%, and the sensitivity/ recall score is only 78%
    - Low Risk:  Precision rate is 100%, but the sensitivity/ recall score is only 58%
    - Average: Precision rate is 99%, but the sensitivity/ recall score is only 58%

While this algorithm outperforms the other two resampling algorithms, it is still a poor fit for our prediction model. 

###### Balanced Random Forest Classifier

![Balanced Random Forest Classifier](https://user-images.githubusercontent.com/111623064/217157531-2e59c51e-4e96-43be-a1a1-d7ffdb5351e6.png)

- Balanced Accuracy Score is 78.88% 
- Precision and Recal Scores: 
    - High Risk: Precision rate is only 3%, and the sensitivity/ recall score is only 70%
    - Low Risk:  Precision rate is 100%, but the sensitivity/ recall score is 87%
    - Average: Precision rate is 99%, but the sensitivity/ recall score is 87%

This algorithm is not the best fit for our prediction model, however it does outperform all 3 of the resampling algorithms. 

###### Easy Ensemble Classifier

![Easy Ensemble Classifier](https://user-images.githubusercontent.com/111623064/217157554-ea4873ed-96a6-4cd2-a405-86be33fcb685.png)

- Balanced Accuracy Score is 93.17% 
- Precision and Recal Scores: 
    - High Risk: Precision rate is only 9%, and the sensitivity/ recall score is 92%
    - Low Risk:  Precision rate is 100%, and the sensitivity/ recall score is 94%
    - Average: Precision rate is 99%, and the sensitivity/ recall score is 94%

This algorithm shows the most precision and accuracy compared to the others we've tested thusfar.

## Summary
Out of the algorithms we've tested, the Easy Ensemble Classifier has balanced accurasy score as well as the highest precision rate and recall for both high and low risk credit risk. With that being said, the precision rate for high risk is still only 9%, so we are likely to see a high number of false positives. In other words, this algorithm has a good potential to detect high risk applicants, but we are likely to have low risk applicants incorectly flagged as high risk. The precision rate and recall score for low risk are both high, meaning we will see very minimal false negatives. In other words, this algorithm has the potential to detect low risk applicants, while also minimizing the amount of high risk applicants incorectly flagged as low risk. 

In order for this model to be used in a meaninful way, there would need to be some form of stop gap that would allow for those incorectly flagged applicantions to be reviewed. For example, sending a letter or email to all denied applicants with an explanation as to why they are being denied, and an option to appeal if they feel an error has been made. If that can be done, I would reccomend the company use this algorithm. 

I would also reccomend doing further research into credit risk analysis and supervised machine learning. It would be useful to see what other companies are doing, and determine how our algorithm compares. This research may also prove insightful as to how we might improve upon the algorithm currently selected. 
