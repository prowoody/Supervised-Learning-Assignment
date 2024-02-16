# Module 20 Report - Credit Risk Analysis

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).

The purpose of this analysis is to evaluate the performance of two logistic regression machine learning models in predicting the credit risk associated with loans. The analysis was conducted on financial data of loan sizes, interest rates, borrowers income, debt-to-income ratios, number of accounts, derogatory marks, and total debt. The objective was to predict the loan status, being either a healthy loan of ('0') or high-risk loan of ('1').

* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

The stages of this machine learning process included the following:
1. Split the datasets for training and testing
2. Create and fit a logistic regression model with data
3. Evaluate the model's performance by observing accuracy, precision, recall, and f1 scores
4. Resample the data with Random Over Sampler for class imbalance
5. Create and fit a secondary logistic regression model with resampled data
6. Evaluate the secondary model's performance by observing the same accuracy, precision, recall, and f1 scores

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.

* Accuracy: The accuracy of the model is 0.99, meaning that it correctly classifies 99% of the instances.
* Precision:
  For healthy loans ('0'): The model has a precision of 1.00, meaning that it perfectly identifies true positives with no false positives.
  For high-risk loans ('1'): The model has a precision of 0.87, meaning that it is moderately effective in identifying high-risk loans with some false positives.
* Recall:
  For healthy loans ('0'): The model has a recall of 1.00, meaning that it perfectly identifies all instances of healthy loans with no false negatives.
  For high-risk loans ('1'): The model has a recall of 0.89, meaning that it is moderately effective in identifying high-risk loans with some false negatives.

* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

* Accuracy: The accuracy of the model is 0.99, meaning that it correctly classifies 99% of the instances.
* Precision:
  For healthy loans ('0'): The model has a precision of 0.99, meaning that it is almost perfect at identifying true positives with few false positives.
  For high-risk loans ('1'): The model has a precision of 0.99, meaning that it is almost perfect at identifying high-risk loans with few false positives. 
* Recall:
  For healthy loans ('0'): The model has a recall of 0.99, meaning that it is almost perfect at identifying nearly all instances of healthy loans with few false negatives.
  For high-risk loans ('1'): The model has a recall of 0.99, meaning that it is almost perfect at identifying high-risk loans with few false negatives.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

The secondary logistic regression model trained with resampled data outperformed the first model trained with original data, particularly in forecasting high-risk loans ('1'), I found after looking at the modeling results. For high-risk loans, the model generated better precision, recall, and f1 scores; this is crucial because it will help the lending organization cut down on the number of failed loans and associated losses. 
For this credit risk study, I would obviously suggest model 2, which uses logictic regression trained with resampled data, given the accuracy of the results is better than that of the first model. The findings demonstrate that it can more accurately determine whether there is a larger difference between healthy and high-risk loan applications and can steer clear of loans that would result in more losses for the financial institution in the future. 
