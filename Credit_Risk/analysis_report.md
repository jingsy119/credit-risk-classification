# Module 12 Report

## Overview of the Analysis

In this section, the analysis for the machine learning models used in this challenge was summarized.

* The purpose of this analysis was to use logistic regression to train and evaluate model and identify the creditworthiness of loan borrowers.
* The financial information provided include size of the loan, interest rate, income of the borrower, debt to income, number of accounts, derogatory marks, total debt, and loan status. 
* The model is to predict the loan status: whether it is a healthy loan (Class 0) or a high-risk loan (Class 1).
* Parameters such as `value_counts` was used to identify the number of Class 0 and Class 1 loan status to evaluate whether the data is balanced.
* The data was initially split into training and testing sets by using `train_test_split`. It was followed by fitting with a `LogisticRegression` model. The model's performance was evaluated by balanced accuracy score, a confusion matrix, and a classification report. The data was later resampled using the `RandomOverSampler` module from the imbalanced-learn library for it to have rebalanced class distribution and then be the data was predicted also using the logistic regression model. The results were evaluated using the same analyses and compared with the fit without the data resampling.

## Results

The balanced accuracy scores and the precision and recall scores were evaluated for both machine learning models.

* Machine Learning Model 1 (Logistic Regression without resampling):
  * The balanced accuracy score was 0.952, suggesting a decent fit.
  * The confusion matrix unveils that there were 102 predications that were false positive, and 56 were false negative.
  * The classification report suggests that Class 0 has a nearly perfect fit with 1.0 for both precision and f1-score, and 0.99 for the recall score. On the other hand, Class 1 had a considerably weaker fit with precision and recall scores, and f1-score being 0.85, 0.91, and 0.88, respectively. This is attributed to the imbalanced sampling of Class 0 (value count of 75036) and Class 1 (value count of 2500).

* Machine Learning Model 2 (Logistic Regression with random resampling):
  * With the resampling, the balanced accuracy score becomes 0.995.
  * The confusion matrix suggests that the 422 results were false positive, and 403 results were false negative.
  * The classification report suggest that the precision and recall scores, and f1-score all increased to 0.99 for both Class 0 and Class 1.

## Summary

The results of the machine learning models were summarized, and a recommendation on the model to use was included in this section.
* The logistic regression model with random resampling had a better performance than the one without resampling. This is reflected by its higher accuracy score as well high precision, recall, and f1-scores of 0.99 for both Classes 0 and 1. Without resampling, the precision, recall, and f1-scores were high for Class 0 (healthy loan), however, being the minority group, Class 1 (high-risk loan) suffered in these scores. 
* In this usecase, it is more important to predict Class 1, or the high-risk loans. Therefore, oversampling the minority group, Class 1, to train the model is a plausible approach. The feasibility of this approach was justified by high accuracy, precision, and recall scores in the end.
