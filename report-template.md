## Overview of the Analysis

I used attributes about previous loans and their borrowers to predict a binary risk classification of future loans using loan and borrower data. 

The dataset used previous loan data and was based on the size and interest rate of the loan, as well as different financial attributes about the borrower such as income, debt, number of accounts, and previous derogatory marks. These were paired with a binary classification of 'Healthy' and 'Risky' for each loan.

I split the data between a training and testing dataset, and fit a logistic regression model to the training dataset, using the remaining testing dataset for predictions to evaluate the model. 

I evaluated the model with a confusion matrix to idenitfy the ammount and type of correct and incorrect classifications.



## Results

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.

    - Accuracy: Total Correct Classificaiton %
        - 0.99

    - Precision: Predicted Label Correct Classificaiton %
        - Healthy: 1.00
        - Risky: 0.85
        - Macro Avg: 0.92
        - Weighted Avg: 0.99

    - Recall: % of Total Label Correctly Predicted
        - Healthy: 0.99
        - Risky: 0.95
        - Macro Avg: 0.97
        - Weighted Avg: 0.99

## Summary

This model is proficient in predicting healthy loans. It is unlikely to flag healthy loans as risky. It is also adequete at identifying most risky loans, correctly flagging 95% of all risky loans.

The model struggles with false positives, with 15% of all risky flags being healthy loans. While 99% of the time, the model send a correct classification, this is mostly due to the low ammount of risky loans compared to healthy loans.

The model has it's uses as a first pass, due to it's simplicity and adequate false negative rate, but I would not reccomend it's use to take action due to it's high false positive rate. Since this is also a model predicting financial information, something with high importance, I cannot reccomend this model for this field. Incorrect classifications have a much higher risk in this field compared to others, so a better model is absolutely required. 