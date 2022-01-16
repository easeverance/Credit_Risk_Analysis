# Credit_Risk_Analysis
## Overview
The purpose of this module is to apply machine learning to solve a real world challenge: credit card risk.  Since good loans outnumber risky loas there is an inherent unbalanced classification problem.  This module employs us to use different techniques to train and evaluate a set of data with unbalanced classed.  Resampling is performed using ***imbalanced-learn*** and ***scikit-learn*** libraries.  The data is evaluated using the ***RandomOverSample*** and ***Smote*** algorithms to oversample the data, ***ClusterCentroids*** algorithm is used to undersample the data, and ***SMOTEENN*** algorithm is used to do a combinatorial approach of over/undersampling. Finally ***BalancedRandomForestClassifer*** and ***EasyEnsembleClassifer*** are used to reduce bias and predict credit risk.  At the end all of the models are evaluated on performace and whether they should be used to predict credit risk. 

## Results

For all of the models the data was split into two: train and test datasets.  The models use the training dataset to learn from and the testing dataset to actually asses the performance.  The first model was the Naive Random Oversampling utilizing the RandomOverSample to resample the data,  second model is the SMOTE Oversampling model, third is the Undersampling model, fourth is the combination of over/under sampling using SMOTEENN, fifth is the Balanced Random Forest Classifier, finally followed by the sixth model Easy Ensemble AdaBoost Classifier.  Below are the results of the the balancec accuracy score, the precision score and the recall score.  

### ***Balanced Accuracy Score***

The balanced accuracy score is the percentage that the model accurately predicts both outcomes.

#### *Naive Random Oversampling*

From the image below you can see that the calcuated balance accuracy score using the RandomOverSample shows an accuracy of 65.1%%

![Naive Model balanced accuracy score](https://user-images.githubusercontent.com/90973718/149677987-24a18c57-756d-4c84-bfb2-61309b1cff84.png)


#### *SMOTE Oversampling*

With this model the accuracy declines slightly to 62.7%

![SMOTE balanced accuracy score](https://user-images.githubusercontent.com/90973718/149678057-dc6819c0-eb28-45b6-abf7-0711a6009337.png)


#### *Undersampling*

With the undersampling model the prediction accruacy stayed as the same as the SMOTE Oversampling model at 62.7%.

![Undersampling balanced accuracy score](https://user-images.githubusercontent.com/90973718/149678116-22dc1c1b-69eb-4a74-b0e4-fd5b6e7d0c3a.png)


#### *Combination Over/Undersampling*

This model seems to be the worst thus far at prediction accruacy at 52.9%

![combination balanced accuracy score](https://user-images.githubusercontent.com/90973718/149678241-ad565b5c-76a8-489f-820c-7661f806a13c.png)


#### *Balanced Random Forest Classifer*

The balanced random forest classifier performs better than the oversampling, undersampling and combination over/undersampling modes at 80.0%

![random forest balanced accuracy](https://user-images.githubusercontent.com/90973718/149646112-7bf68787-09dd-4fcd-9f21-723853ecb6d2.png)


#### *Easy Ensemble Classifier*

The easy ensemble classifer hands down out performs the other models when it comes to prediction accuracy at 92.5%.

![easy ensemble balanced accuracy score](https://user-images.githubusercontent.com/90973718/149646148-2637586b-2840-4f57-9342-6743f8a6c593.png)


### *Precision and Recall Scores*

The Accuracy Score is simply the percentage of correct predictions.  However, the accruacy score is not always the most meaninguful metric.  Precision is used to measure how reliable a positive classification can be.  Recall is used to measure test sensitivity. The fundamental difference between precision and recall is that high recall tests are aggressive and are great at detecting the intended targets.  Where as, high precision tests are more conservative, where the predicted positives are true posititives but there is a high liklihood that other true postivies are not predicited.  

#### *Naive Random Oversampling*

The precisin score shows that the model is excellent at predicting low risk loan applications (100%) but is terrible at predicting the high risk loan applications (1%) of the time.  The sentivity percentange is relatively the same between high risk loans and low risk loans. 

![Naive classification report](https://user-images.githubusercontent.com/90973718/149678461-cb45b196-d224-456c-8c7b-d48f00983ec4.png)

#### *SMOTE Oversampling*

You do not see much improvement in prediction between the Naive Random Oversampling and the SMOTE Oversampling. 

![SMOTE classification report](https://user-images.githubusercontent.com/90973718/149678623-60fa0f09-04e2-4df5-bec1-89eb397d99f1.png)


#### *Undersampling*

With this model you don't see any change in precision but you see a significant drop in recall or True Positive Rate decreased.

![undersampling classification report](https://user-images.githubusercontent.com/90973718/149679885-8d98c2ad-4cf1-4595-a5b5-e3af844dbffe.png)


#### *Combination Over/Undersampling*

With the combination over/undersampling the precision remains constant however the recall percentage has increased.  The sensitivity has significantly improved with the high risk loan applications. 

![combination classification report](https://user-images.githubusercontent.com/90973718/149680081-09fda350-761d-4e39-8c2c-fc3e5d07dc9d.png)

#### *Balanced Random Forest Classifer*

The balnced random forest classifier model continues to improve upon the percentages.  Here percision remains the same as the previous models but the recall significantly improves.  

![random forest classification report](https://user-images.githubusercontent.com/90973718/149680180-bb793e28-d91b-4f7d-b396-2fe8303d7e1c.png)


#### *Easy Ensemble Classifier*

Again the easy ensemble classifier model provides the best results out of all of the models.  

![easy ensemble classification report](https://user-images.githubusercontent.com/90973718/149680245-203e4d98-11e3-422b-864c-1b76cb141694.png)



### Summary

Out of all of the models the easy ensemble classifer provided the best accuracy.  Ensemble learning is combining multiple models to help improve the accuracy and decrease the variance resulting in better performance of the model.  
















