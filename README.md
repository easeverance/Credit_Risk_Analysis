# Credit_Risk_Analysis
## Overview
The purpose of this module is to apply machine learning to solve a real world challenge: credit card risk.  Since good loans outnumber risky loas there is an inherent unbalanced classification problem.  This module employs us to use different techniques to train and evaluate a set of data with unbalanced classed.  Resampling is performed using ***imbalanced-learn*** and ***scikit-learn*** libraries.  The data is evaluated using the ***RandomOverSample*** and ***Smote*** algorithms to oversample the data, ***ClusterCentroids*** algorithm is used to undersample the data, and ***SMOTEENN*** algorithm is used to do a combinatorial approach of over/undersampling. Finally ***BalancedRandomForestClassifer*** and ***EasyEnsembleClassifer*** are used to reduce bias and predict credit risk.  At the end all of the models are evaluated on performace and whether they should be used to predict credit risk. 

## Results

For all of the models the data was split into two: train and test datasets.  The models use the training dataset to learn from and the testing dataset to actually asses the performance.  The first model was the Naive Random Oversampling utilizing the RandomOverSample to resample the data,  second model is the SMOTE Oversampling model, third is the Undersampling model, fourth is the combination of over/under sampling using SMOTEENN, fifth is the Balanced Random Forest Classifier, finally followed by the sixth model Easy Ensemble AdaBoost Classifier.  Below are the results of the the balancec accuracy score, the precision score and the recall score.  

### ***Balanced Accuracy Score***

The balanced accuracy score is the percentage that the model accurately predicts both outcomes.

#### *Naive Random Oversampling*

From the image below you can see that the calcuated balance accuracy score using the RandomOverSample shows a pretty good accuracy of 91%

![Naive Model balanced accuracy score](https://user-images.githubusercontent.com/90973718/149645919-d1339634-56f4-4dbc-9834-b7b00c5d1454.png)

#### *SMOTE Oversampling*

With this model the accuracy improves only slightly at 91.5%

![SMOTE balanced accuracy score](https://user-images.githubusercontent.com/90973718/149645966-5f3650e8-0a78-4a02-8758-272e68234721.png)

#### *Undersampling*

With the undersampling model the prediction accruacy at 91.2% is better than the Random Oversampling but slightly less accurate the the SMOTE Oversampling. 

![Undersampling balanced accuracy score](https://user-images.githubusercontent.com/90973718/149645990-ef61aba9-62b8-400b-b3d8-6550d8bf3f59.png)

#### *Combination Over/Undersampling*

This model produces the most accurate prediction between the oversampling modules and the undersampling one at 92%

![combination balanced accuracy score](https://user-images.githubusercontent.com/90973718/149646065-413db90f-dd42-4fcc-b1f7-7ec3aa356640.png)

#### *Balanced Random Forest Classifer*

Out of all of the models the Balanced Random Forest  was the least accruate at 80%.

![random forest balanced accuracy](https://user-images.githubusercontent.com/90973718/149646112-7bf68787-09dd-4fcd-9f21-723853ecb6d2.png)


#### *Easy Ensemble Classifier*

This model was the most accurate at predicting good loans and risky loans at 92.5%.

![easy ensemble balanced accuracy score](https://user-images.githubusercontent.com/90973718/149646148-2637586b-2840-4f57-9342-6743f8a6c593.png)

### *Precision and Recall Scores*











