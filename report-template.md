# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

## Overview of the Analysis

The purpose of this analysis is to build a model that can successfully identify the creditworthiness of borrowers and use that to predict loans that may be higher risk.

The data that was used consisted of historical lending activity from a peer-to-peer lending services company. The data included several factors such as: loan size, interest rate, borrower income, debt to income, number of accounts, derogatory marks, total debt, and loan status. 

First, I split the data into training and testing datasets and used loan status as our target variable (healthly loans were labeled 0 and high risk loans were labeled 1).

We then created a logistic regression model using the training data and saved the predictions for the testing data labels. We evaluated the models performance using a generated confusion matrix and then printed out the classificiation report. 

Next, I used RandomOverSampler to resample the data. Then I created another logistic regression model to evaluate the resampled data. I then compared the results to determine which resulted in higher performance. 

## Results

Logistic Regression Model 1 - Original Data


-Accuracy Score: .95

-Healthy Loans:
Precision: 1.00
Recall Scores: .99

-High Risk Loans:
Precision: .85
Recall Scores: .91

Logistic Regression Model 2: Resampled Data

-Accuracy Score:.99

-Healthy Loans:
Precision: 1.00
Recall Scores: .99

-High Risk Loans:
Precision: .84
Recall Scores: .99


## Summary

The logistic regression model using the resampled data performed better with a higher accuracy rate than that of the logistic regression model using the original data. Something to consider is that the precision of the high risk loans within the second model is lower than that of the first (orginial data). This means that Model 1's predictions of high risk loans are more precise. If the intent is to more successful identify high risk loans (1) with higher precision, then the first model using the originial data may be more successful. 

Overall, due to high accuracy, precision, and recall scores, I would reccomend using Logistic Model 2 utilizing the resampled data. 

