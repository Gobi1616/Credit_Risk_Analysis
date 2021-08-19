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

### Random Over Sampler model

![image](https://user-images.githubusercontent.com/82549869/130086415-7478bee9-85c7-4817-ab54-16fdb5a2b614.png)

![image](https://user-images.githubusercontent.com/82549869/130086537-0016d67c-9ad6-43b6-b89a-54829219a7e7.png)

- A balanced accuracy score of 65% is achieved. 

- The high risk precision is just about 1% with a sensitivity of 62%, resulting in an F1 of only 2%. 

- Because of the large number of low-risk people, it has an accuracy of nearly 100 percent and a sensitivity of 68%.

### SMOTE model

![image](https://user-images.githubusercontent.com/82549869/130086692-5fe99072-380f-456f-b532-00833c8df460.png)

- The results are pretty similar to the previous model.

- The balanced accuracy score is 64%.

- The high_risk precision is about 1% only with 63% sensitivity which makes a F1 of 2% only.

- Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 66%.

### Cluster Centroids model

![image](https://user-images.githubusercontent.com/82549869/130087220-4bc2040b-1673-4cb7-86bb-ee77371d14f4.png)

- The balanced accuracy score is about 62%.

- The high_risk precision is still 1% only with 68% sensitivity which makes a F1 of only 2%.

- Due to the high number of false positives, the low_risk sensitivity is 57%.

### Balanced Random Forest Classifier model

![image](https://user-images.githubusercontent.com/82549869/130087757-28ef871d-92f5-42d5-9974-72829e7d0f17.png)

- The balanced accuracy score improved to about 79%.

- The high_risk precision is still low at 4% only with 67% sensitivity which makes a F1 of only 7%.

- Due to a lower number of false positives, the low_risk sensitivity is now 91% with 100% presicion.

### Easy Ensemble Classifier model

![image](https://user-images.githubusercontent.com/82549869/130088291-4ac48955-cbbe-4a6c-90c7-71d006c9dab4.png)

- At the moment, the balanced accuracy score is at 93%. 

- The high risk precision remains poor, at only 7% with 91% sensitivity, resulting in an F1 of only 14%. 

- The low risk sensitivity is now 94% with 100% presicion, thanks to a decreasing number of false positives.

## Summary

All of the credit risk analysis models have poor precision in assessing whether a credit risk is high.  The Ensemble models improved the sensitivity of high-risk credits significantly. With a recall of 92%, the Easy Ensemble Classifier model can detect almost all high-risk credit. On the other hand, because of the low precision, many low-risk credits are still misclassified as high-risk, putting the bank's credit strategy at risk and causing it to miss out on income prospects. For those reasons I would not recommend the bank to use any of these models to predict credit risk.
