# Module 12 Report Template

## Overview of the Analysis

In this analysis, we developed a machine learning model using logistic regression to predict the creditworthiness of borrowers based on historical lending data from a peer-to-peer lending services company. The purpose of the analysis was to assess the risk associated with each loan application, helping the company identify high-risk loans (classified as 1) and healthy loans (classified as 0).

The dataset provided included financial and demographic information for each loan, with the goal of predicting the loan_status variable, where:
	•	0 represents a healthy loan (low-risk)
	•	1 represents a high-risk loan

To understand the data distribution, we used value_counts on the loan_status variable, revealing an imbalance with significantly more healthy loans than high-risk ones. This imbalance can affect model performance, as the model might become biased toward the majority class.

Machine Learning Process Stages:

	1.	Data Preparation: We separated the data into features (x) and labels (y), where loan_status served as the label.
	2.	Data Splitting: We split the dataset into training and testing subsets using train_test_split, with 80% of the data for training and 20% for testing.
	3.	Model Selection and Training: We chose logistic regression as our primary machine learning algorithm, instantiating the model with a random_state of 1 to ensure reproducibility. We trained the model using the training data.
	4.	Model Evaluation: After training, we evaluated the model’s performance on the test data, generating predictions and comparing them with actual values using a confusion matrix and a classification report. Key metrics such as accuracy, precision, recall, and F1-scores were used to assess the model’s effectiveness.

## Results

Machine Learning Model 1 (Logistic Regression):

	•	Accuracy: 99%
	•	Precision for 0 (healthy loan): 1.00
	•	Recall for 0 (healthy loan): 1.00
	•	F1-Score for 0 (healthy loan): 1.00
	•	Precision for 1 (high-risk loan): 0.86
	•	Recall for 1 (high-risk loan): 0.91
	•	F1-Score for 1 (high-risk loan): 0.88

## Summary

The logistic regression model demonstrated high performance in predicting both healthy and high-risk loans, with an overall accuracy of 99%. The model’s precision and recall scores for healthy loans were perfect, meaning it correctly identified all healthy loans without any false positives. For high-risk loans, the model achieved strong but slightly lower precision and recall scores, indicating a small number of misclassifications.

## Recommendation

Given the results, this logistic regression model is highly effective for predicting healthy loans and reasonably effective for predicting high-risk loans. If the company prioritizes minimizing risk and is particularly concerned about identifying high-risk loans, we may consider further tuning or balancing techniques to improve the model’s performance on the minority class. However, based on the high accuracy and balanced metrics, this logistic regression model is recommended as it performs well in predicting both loan statuses.


