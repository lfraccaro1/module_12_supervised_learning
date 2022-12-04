# Module 12 Report - Supervised Learning

## Overview
In this project, I have used various techniques to train and evaluate machine learning models with imbalanced classes. 
to determine whether or not a borrower is creditworthy.

I have used a dataset of historical lending activity, which features data including loan size, interest rate, and aspects of the borrower's financial health.

The first step was to create the labels set (y) from the `loan_status` column, and then create the features (X) DataFrame from the remaining columns. After doing this, I checked the balance of the labels variable using the `value_counts` function. I then split the data into training and testing datasets by using the `train_test_split` function. 

Using the imbalanced-learn library, I then used logistic regression models to compare two versions of the dataset, first using the original data, and second using resampled data, achieved by using the `RandomOverSampler` module.

After saving the predictions on the testing data labels for each model, I obtained the balanced accuracy for each, and generated confusuion matrix and classification reports. 

## Results
Here I will display a summary of the results from my analysis.

* Machine Learning Model 1 (Original Data):
  * Balanced Accuracy Score: 95.2%
  * Accuracy: 99%
  * Precision Healthy Loan (0): 100%
  * Precision Risky Loan (1): 85%
  * Recall Healthy Loan (0): 99%
  * Recall Risky Loan (1): 91%

* Machine Learning Model 2 (Resampled Data):
  * Balanced Accuracy Score: 99.4%
  * Accuracy: 99%
  * Precision Healthy Loan (0): 100%
  * Precision Risky Loan (1): 84%
  * Recall Healthy Loan (0): 99%
  * Recall Risky Loan (1): 99%

## Summary
In summary, I would suggest using the second model. It scores better than model 1 in all areas we calculated, with an impressive balanced accuracy score of 99.4%. Model 2 also showed 99% recall for both outcomes, giving me more confidence in this model. I would like to explore ways to further improve its precision however, as it achieved 84% precision at detecting risky loans.

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )