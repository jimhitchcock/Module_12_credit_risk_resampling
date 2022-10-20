# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
The purpose of this analysis is to use it to build a machine learning model that will effectively predict creditworthy borrowers
* Explain what financial information the data was on, and what you needed to predict.
With loan size, interest rate, income, debt to income ratio, number of accounts, derogatory accounts & total debt values available,
we will create a machine learning model that will predict whether a loan will be paid on time or become delinguent.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
The data set consisted of 75,036 borrowers who are currently in good standing and 2500 borrowers that have defaulted on their loan.
* Describe the stages of the machine learning process you went through as part of this analysis.
First we make sure our data is in the correct format for our machine learning models to recognize, then we assign "loan_status" as our
target variable "y" that we would like to predict.  We then assign all the other columns to the "X" variable.  We are then able to 
instantiate the model, fit the model with the training data, then predict the outcome.  We then evaluate the model's preformance 
by creating a balanced accuracy score, classification report and confusion matrix.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
We first created and ran a basic Logistic Regression model on the data then we resampled the data with the RandomOverSampler function
since the wide disparity between to the two possible outcomes in the data.  Performing loans wildly outnumber the non-performing loans.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
LogisticeRegression was the method used to generate the first model.  It produced a balanced accuracy score of 95.2%, a 100% for performing
loans and 85% for non-performing loans, recall score of 0.99 and 0.91 respectfully.  


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
RandomOverSampler was the method used for teh second model we used.  Since we want to increase the accuracy of our model in predicting
the non-performing loans above all else, we wanted to see how the results improved if we resampled the data to even numbers for both.
The balance accuracy score increased to 99.4%, 0.99 precision scores for both the performing and non-performing loans, and a recall score
of 0.99 for both as well.
## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
Both models did well predicting the creditworthiness of the borrowers however the oversampled data performed slightly better.
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
It is more important that we accurately predict the non-performing borrowers than it is to predict the performing loans.

