

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

