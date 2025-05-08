# credit-risk-classification


## Overview of the Analysis

The purpose of this analysis was to build a model that indentifies high risk loans from non-high risk loans. The goal was to identify high risk borrowers based on variables such loan amount, interest rates, borrower income, debt to income ratio, number of accounts, total debt and derogatory marks. 

**Data info:**
* 77,536 Total Loan Records
* Target Variable: 'Loan Status'
    * Healthy loan (0):  75,036 total
    * High Risk Loan (1): 2,500 total

Maching Learning Pipeline:
1. Import CSV file
2. Used train_test_split() from sklearn.model_selection to training and testing sets
3. Used LogisticRegression() to create the model
4. Trained the model using model.fit(X_train, y_train)
5. Generated predictions using model.predict(X_test)
6. Generated a confusion matrix and printed the classification report



## Results

**Machine Learning Model 1:**
    * Accuracy: 0.99

**Healthy-loan (0)**

    * Precision: 1.00

    * Recall: 0.99

    * F1-score: 1.00

    * Support: 18,765

**High-risk-loan (1)**

    * Precision: 0.84

    * Recall: 0.94

    * F1-score: 0.89

    * Support: 619


## Summary

- **Best performer:**  
  I tested Logistic Regression and it performed very well.  It had a perfect F1 (1.00) for healthy loans and a strong 0.89 for high-risk loans.

- **Why it performs best:**  
  It flags 94% of real high risk loans while almost never mislabeling healthy ones, giving it a solid balance between catching true risks and keeping false positives low.

- **Dependence on the problem:**  
  Since overlooking a high risk loan is more costly than mistakenly flagging a safe one, I focused on making sure the model catches as many high risk loans as possible (prioritizing sensitivity) rather than aiming for perfect precision.

- **Recommendation:**  
  My recommendation is to use this Logistic Regression model. 

  ## Resources
  I used examples from class to write the code and used Chatgpt for optimizing text and supporting my learning