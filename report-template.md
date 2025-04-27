# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* The purpose of the analysis was to build (train and test) a model to determine the creditworthiness of borrowers based on a dataset containing historical lending activity. The historical dataset included the following data points:

* loan_size
* interest_rate
* borrower_income
* debt_to_income
* num_of_accounts
* derogatory_marks
* total_debt
* loan_status

The dependent variable (or the labels) was the loan status and the X (or the features) were all the other columns that are indicators of the loan status and creditworthiness of the customer.

In order to build the model, I took the following steps:
* Isolated the labels and features into y and X variables
* Split the dataset between training and testing data
* Fit the training data to the logistic regression model
* And used the trained model against the X testing variables to predict the y (labels)
* Generated the confusion matrix and the classification report to determine how well the model was built

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

- **Precision**
  - **Meaning**: When the model predicts a person has good/bad credit, how often is it correct?
    - **Good Credit (0)**: 100%
    - **Bad Credit (1)**: 86%
  - **Interpretation**: Model is extremely confident when predicting good credit; slightly less confident when predicting bad credit.

- **Recall**
  - **Meaning**: Out of all *actual* good/bad credit people, how many did the model catch?
    - **Good Credit (0)**: 99%
    - **Bad Credit (1)**: 94%
  - **Interpretation**: Model captures almost all good credit cases and most bad credit cases.

- **F1-Score**
  - **Meaning**: Balance between Precision and Recall (especially important when classes are imbalanced).
    - **Good Credit (0)**: 100%
    - **Bad Credit (1)**: 90%
  - **Interpretation**: Model does an excellent job balancing precision and recall, especially for bad credit predictions.

- **Accuracy**
  - **Meaning**: Out of all predictions made, how many were correct overall?
    - **Overall**: 99%
  - **Interpretation**: Model is correct 99% of the time across all predictions. Very strong overall performance.

## Summary

The machine learning model demonstrates very strong performance metrics. It achieves an overall accuracy of 99%, with extremely high precision and recall for good credit cases and strong performance for bad credit cases as well. The model correctly identifies 99% of good credit customers and 94% of bad credit customers. While there is a slight drop in precision for bad credit (86%), the recall is high, meaning the model successfully identifies the majority of risky customers.

Given the high accuracy, balanced F1 scores, and strong ability to detect both good and bad credit risks — despite a slightly imbalanced dataset — I recommend deploying this model for business use.

It would allow the company to confidently approve good credit applications while also minimizing risk from bad credit approvals. However, continued monitoring and periodic retraining are recommended to maintain performance over time, especially if customer profiles evolve.
