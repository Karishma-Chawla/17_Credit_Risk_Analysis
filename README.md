
# Overview

The goal of is to predict credit risk using Supervised Machine Learning model. Machine Learning statistical algorithms are utlized to make predictions based on data patterns provided.

<img width="551" alt="Credit Risk" src="https://user-images.githubusercontent.com/98617082/186016565-bd872805-0952-48e8-b908-cd2bebef8921.png">

# Data

CSV file including infomation on applicant and loan.

Size : 435 MB
![image](https://user-images.githubusercontent.com/98617082/186029250-4ad0a41a-8fb1-4a85-ad8a-003479d4623c.png)


Various techniques are used to train and evaluate the data are mentioned below:
* Two oversampling algorithms -naive random oversampling algorithm and the SMOTE algorithm to determine which algorithm results in the best performance. . 
* Undersampling data using the ClusterCentroids algorithm.
* Combination over- and under-sampling algorithm SMOTEENN to resample the data to determine if the algorithm results in the best performance compared to the other sampling algorithms. 
* Compare two machine learning models that reduce bias, BalancedRandomForestClassifier and Easy Ensemble AdaBoost classifier.


## Results
### DELIVERABLE 1-Over sampling using RandomOversampler

![image](https://user-images.githubusercontent.com/98617082/176328272-cc897e40-f6a4-43e8-b0a7-1b19f3cae1f2.png)

*  The "High Risk" precision rate was only 1% with the recall at 60%.
* "Low Risk" had a precision rate of 100% and recall at 65%.
* Accuracy score of 62.5%.

### Over sampling using SMOTE
![image](https://user-images.githubusercontent.com/98617082/176328289-5f01e146-a3c0-4e17-99f9-dfab67e85a6c.png)

 
*  The "High Risk" precision rate was only 1% with the recall at 64%.
* "Low Risk" had a precision rate of 100% and recall at 66%.
* Accuracy score of 65%.
* Results are similar to the last model.

### Undersampling using ClusterCentroids resampler
![image](https://user-images.githubusercontent.com/98617082/176328307-ce166b4a-31e7-4ecb-affc-4dd472f9d3d5.png)

 
* Accuracy score of 65%.
*  The "High Risk" precision rate was only 1% with the recall at 61% resulting in F1 score of 1%.
* "Low Risk" had a precision rate of 100% with a recall of 45% compared to oversampling methods.

### DELIVERABLE 2- Combination Sampling- SMOTEENN
SMOTEENN Model combines aspects of both oversampling and undersampling.
![image](https://user-images.githubusercontent.com/98617082/176328338-500a8fba-3591-422b-8863-a3cf8f56758d.png)

 
* The balanced accuracy score was at 65% when using a combined sampling model.
*The "High Risk" precision rate did not improve was only 1%, however the recall increased to 72% giving this model an F1 score of 2%.
*"Low Risk" still showed a precision rate of 100% with the recall at 57%.

## DELIVERABLE 3- ENSEMBLE CLASSFIERS

### RandomForestClassifier Model

![image](https://user-images.githubusercontent.com/98617082/176328379-77dbf17a-0051-429a-b290-914a14ea4063.png)
 
•	The balanced accuracy score increased to 78.8% for this model.
•	The "High Risk precision rate increased to 4% with the recall at 67% giving this model an F1 score of 7%.
•	"Low Risk" still had a precision rate of 100% with the recall at 91%.
### Easy Ensemble AdaBoost Classifier

![image](https://user-images.githubusercontent.com/98617082/176328413-6ea661c5-7b17-404f-9cf0-7cc069dfe322.png)

•	The balanced accuracy score increased to 93% with this model.
•	The "High Risk precision rate increased to 9% with the recall at 92% giving this model an F1 score of 16%.
•	"Low Risk" still had a precision rate of 100% with the recall now at 94%.

# Summary
Comparing all the models, Easy Ensemble AdaBoost Classifier yielded the best results with an accuracy rate of 93% , 9% precision rate for "High Risk candidates with 92% recall. The sensitivity of predicting ‘low risk’ was highest at 94% recall (against late 50’s to mid 60’s range by other models).

Ranking based on accuracy and high risk results

* EasyEnsembleClassifer: 93.2% accuracy, 9% precision, 92% recall, and 16% F1 Score
* BalancedRandomForestClassifer: 78.8% accuracy, 4% precision, 67% recall and 7% F1 Score
* SMOTE: Accuracy score of 65%,1% precision, 61% recall of 64%. 
* SMOTEENN: 65% accuracy, 1% precision, 72% recall and 2% F1 Score
* ClusterCentroids: 65% accuracy, 1% precision, 61% recall resulting in F1 score of 1%.
* RandomOverSampler: 62.5% accuracy, 1% precision, 60% recall 
