# Credit_Risk_Analysis

## Analysis Overview

In this project, we use Python to build and evaluate several machine learning models to predict credit risk.
We adopted the following procedure:

- Using the RandomOverSampler and SMOTE algorithms, oversample the data. 
- Using the ClusterCentroids technique, undersample the data. 
- Using the SMOTEENN algorithm, take a combinatorial approach to over- and undersampling. 
- BalancedRandomForestClassifier and EasyEnsembleClassifier are two machine learning models that eliminate bias.

## Resources

- Data Source: LoanStats_2019Q1.csv

- Software: Python 3.7.9, Anaconda Navigator 1.9.12, Conda 4.8.4, Jupyter Notebook 6.0.3

## Results (Balanced Accuracy Scores, Confusion Matrixes and Imbalanced Classification Reports)

### RandomOverSampler model

A balanced accuracy score of 65% is achieved. 

The high risk precision is just about 1% with a sensitivity of 62%, resulting in an F1 of only 2%. 

Because of the large number of low-risk people, it has an accuracy of nearly 100 percent and a sensitivity of 68%.

### SMOTE model

The results are pretty similar to the previous model.

The balanced accuracy score is 64%.

The high_risk precision is about 1% only with 63% sensitivity which makes a F1 of 2% only.

Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 66%.

### ClusterCentroids model

The balanced accuracy score is about 62%.

The high_risk precision is still 1% only with 68% sensitivity which makes a F1 of only 2%.

Due to the high number of false positives, the low_risk sensitivity is 57%.

### BalancedRandomForestClassifier model

The balanced accuracy score improved to about 79%.

The high_risk precision is still low at 4% only with 67% sensitivity which makes a F1 of only 7%.

Due to a lower number of false positives, the low_risk sensitivity is now 91% with 100% presicion.

### EasyEnsembleClassifier model

Now, the balanced accuracy score is high to about 93%.

The high_risk precision is still low at 7% only with 91% sensitivity which makes a F1 of only 14%.

Due to a lower number of false positives, the low_risk sensitivity is now 94% with 100% presicion.

## Summary

All the models used to perform the credit risk analysis show weak precision in determining if a credit risk is high.
The Ensemble models brought a lot more improvment specially on the sensitivity of the high risk credits.
The EasyEnsembleClassifier model shows a recall of 92% so it detects almost all high risk credit. On another hand, with a low precision, a lot of low risk credits are still falsely detected as high risk which would penalize the bank's credit strategy and infer on its revenue by missing those business opportunities.
For those reasons I would not recommend the bank to use any of these models to predict credit risk.
