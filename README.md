# Summary Report

## Overview of the Analysis

This analysis was done to determine the creditworthiness of borrowers. Utilizing machine learning cuts the need for lenders to determine if a borrower would or would not default on their loan (eg. healthy loan or high-risk loan). 

For this specific program, historical data from a peer-to-peer lending services company was utlizied. The data included: 
- loan size
- interest rate
- borrower income
- debt:income ratio
- number of accounts
- derogatory marks
- total_debt

Looking at the code you will see two sets of X and y value sets
the X_train/X_test y_train/y_test data comes from splitting the dataset into training and test data.
In this case y = loan_status ( 0 = healthy or 1 = high risk) and X encompasses all the columns in the dataset except for loan_status.

After splitting the data into test and train, the logistic regression model was told to make a prediction on the loan_status based off of the X_test dataset. 
This particular test results in a 95% accuracy in discerning between a healthy loan vs. a high risk loan. 

Taking things further, the RandomOverSampler was used to resample the dataset and the same train, fit, predict sequence was done.
With the oversampled data the model was able to discern a healthy loan from a high risk loan 99% of the time.


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

- Machine Learning Model 1 - Orginial Data:
 - Balance accuracy score = 95% This means that the model is able to truely discern a healthy loan 95% of the time.
 - The precison was at 1.00 for healthy loan and 0.85 for hig-risk loans.
 - The recall was at 0.99 for healthy loans and 0.91 for high-risk laons.
 - Accuracy = 99%


 
- Machine Learning Model 2 - Oversampled Data:
 - Balance accuracy score = 99% 
 - The precison was at 1.00 for healthy loan and 0.85 for hig-risk loans.
 - The recall was at 0.99 for healthy loans and 0.91 for high-risk laons.
 - Accuracy = 99%


## Summary

In summary, this model for both tests was accurate for discerning wether a loan would be healthy or high-risk.
Model 2, which utlized oversampled data, was more accurate than model 1 as shown by their balance accuracy scores (99% for model 2 v. 95% for model 1); without a decrease in precision. 
I would recommend the use of model 2 when trying to discern a healthy loan not so much for a high-risk loan (recall for both models was 85%).

Depending on what the institution wants it may be better to modify the model(s) to discern high-risk loans to avoid a possible lost rather than a healthy loan.

