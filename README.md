# Credit_Risk_Analysis

## Overview 

The purpose of this project was to predict credit card risk, and in order to do this we will need to apply all the skills in data preparation, statistical reasoning, and machine learning to build the model to predict this risk. 

We built the model by using the credit card dataset from LendingClub and adapted the following procedures:
 -	oversample the data using the RandomOverSampler and SMOTE algorithms.
 - 	Undersample the data using the ClusterCentroids algorithm.
 - 	Use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm.
 -	Compare two machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier.

After we adapted the procedures, we then will evaluate the performance of these models and make a recommendation on whether they should be used to predict credit risk.

## Results: Balanced Accuracy Scores, Confusion Matrixes and Imbalanced Classification Reports

### RandomOverSampler model

![RandomOverSampler model](https://github.com/backwater-graphics/Credit_Risk_Analysis/blob/main/Images/RandomOverSampler%20model.jpg)
---

-	The balanced accuracy score is 65%.
-	The high_risk precision is about 1% only with 62% sensitivity which makes a F1 of 2% only.
-	Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 68%.

### SMOTE model

![SMOTE model](https://github.com/backwater-graphics/Credit_Risk_Analysis/blob/main/Images/SMOTE%20model.jpg)
![SMOTE model2](https://github.com/backwater-graphics/Credit_Risk_Analysis/blob/main/Images/SMOTE%20model1.jpg)
---

The results are pretty similar to the previous model.
- The balanced accuracy score is 64%.
-	The high_risk precision is about 1% only with 64% sensitivity which makes a F1 of 2% only.
-	Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 63%.

### ClusterCentroids model

![ClusterCentroids model](https://github.com/backwater-graphics/Credit_Risk_Analysis/blob/main/Images/ClusterCentroids%20model.jpg)
---

-	Here the balanced accuracy score is down to about 51%.
-	The high_risk precision is still 1% only with 59% sensitivity which makes a F1 of 1%.
-	Due to the high number of false positives, the low_risk sensitivity is only 44%.

### SMOTEENN model

![SMOTEENN model](https://github.com/backwater-graphics/Credit_Risk_Analysis/blob/main/Images/SMOTEENN%20model.jpg)

-	The balanced accuracy score is about 64%.
-	The high_risk precision is still 1% only with 70% sensitivity which makes a F1 of only 2%.
-	Due to the high number of false positives, the low_risk sensitivity is 57%.

### BalancedRandomForestClassifier model

![BalancedRandomForestClassifier model](https://github.com/backwater-graphics/Credit_Risk_Analysis/blob/main/Images/BalancedRandomForestClassifier%20model.jpg)
![BalancedRandomForestClassifier model](https://github.com/backwater-graphics/Credit_Risk_Analysis/blob/main/Images/BalancedRandomForestClassifier%20model1.jpg)
---

-	The balanced accuracy score improved to about 79%.
-	The high_risk precision is still low at 4% only with 67% sensitivity which makes a F1 of only 7%.
-	Due to a lower number of false positives, the low_risk sensitivity is now 91% with 100% presicion.

### EasyEnsembleClassifier model

![EasyEnsembleClassifier model](https://github.com/backwater-graphics/Credit_Risk_Analysis/blob/main/Images/EasyEnsembleClassifier%20model.jpg)
![EasyEnsembleClassifier model](https://github.com/backwater-graphics/Credit_Risk_Analysis/blob/main/Images/EasyEnsembleClassifier%20model1.jpg)
---

- Now, the balanced accuracy score is high to about 93%.
- The high_risk precision is still low at 7% only with 91% sensitivity which makes a F1 of only 14%.
- Due to a lower number of false positives, the low_risk sensitivity is now 94% with 100% precision.

## Summary

To summarize our evaluation of the performance of these models, we can see the accuracy ranges from the 50% range to the 90% for the first four models which we did some undersampling, oversampling and a combination of both to try and determine which model was best at predicting which loans are considers highest risk. Then we evaluated the next two models to see if the accuracy score was better and we found that the ranges of the last two models had better ranging which was between 78% and 93% for accuracy.

But after looking at all models and the accuracy ranges, we did find that the EasyEnsembleClassifier model was the most effective model and that it provided the highest Score for all risk loans. 

## Recommendation

I would recommend the Easy Ensemble Classifier because it gives the most balances results in accuracy, precision, and recall scores. However, I would suggest to fine tune the model since the precision for high risk loans is quite low, meaning there are a lot of false positives or low risk loans that were classified as high risk.

