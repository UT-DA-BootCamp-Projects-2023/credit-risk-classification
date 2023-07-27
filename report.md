# Module 12 Report 

## Overview of the Analysis
--
* The main purpose of the analysis is to use the supervised machine learning concept to predict the creditworthiness of the borrowers.
* The historical lending activity dataset which contains information about "loan size", "interest rate", "borrower income”, “debt to income" "num of accounts”, “derogatory marks", "total debt", "loan status" from peer-to-peer lending services company is used to predict the health loan (0) vs high-risk loan (1) status. 
* The variable used in this prediction is loan status which has values of 0 meaning "health loan" status and 1 meaning "high-risk loan" status.
* Below is the list of activities performed which would showcase the usage of supervised machine learning using logistic regression model from sklean.
  * Splitting the data into training and testing datasets by using `train_test_split`
  * Fitting a logistic regression model by using the training data
  * Saving the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model
  * Evaluating the model’s performance by generating the confusion matrix and reviewing the result using print classification report.
  * When some imbalance is found in the result, resampled the data using `RandomOverSampler` module from the imbalanced-learn library
  * And again, went through the process of predicting a Logistic Regression Model with Resampled Training Data and evaluated the model's performance by generating the confusion matrix and reviewing the result using print classification report.

## Results
--
* Machine Learning Model 1 Using `train_test_split`:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
  * Balanced Accuracy Score: 0.94
  * Accuracy Score: 0.99
  * Health loan (0) 
      - precision score: 1.00
      - recall score: 1.00
  * High-risk loan (1) 
      - precision score: 0.87
      - recall score: 0.89

* Machine Learning Model 2 using `RandomOverSampler`:
  * Balanced Accuracy Score: 0.995
  * Accuracy Score: 1.00
  * Health loan (0) 
      - precision score: 1.00
      - recall score: 1.00
  * High-risk loan (1) 
      - precision score: 0.87
      - recall score: 1.00

## Summary
--
Both models performed good for health loan status prediction as the precision and recall score is at 100%. Hence the performance between models will be compared against High-risk loan status prediction.<br>
<br>
It is important to have high Precision and high recall values as "A high precision score indicates less false positives and high recall score indicates less false negative. Based on this consideration, RandomOverSampler model seems to perform better when compared to the 'train_test_split' model. Even though the percentage of false positive (precision score) score is same in both the models, RandomOverSampler model showcases better recall score and thus reducing false negative score. Still with only 87% precision rate false positive could lead to potential loss of customer. <br>
<br>
Based on the above explanation I would recommend the `RandomOverSampler` model when compared to '`train_test_split` model due to its improved recall accuracy.