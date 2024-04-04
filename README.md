# Finding Default transactions-Prediction of CreditCard transaction fraud
![image](https://github.com/Abhik911/Find-Defaulters-Prediction-of-Credit-Card-fraud-/assets/67280652/97e54abb-c117-403b-9b2c-c8878449bb97)

Classification model to predict whether a transaction is fraudulent or not
FindDefault (Prediction of Credit Card fraud)
Problem Statement:
A credit card is one of the most used financial products to make online purchases and payments. Though the Credit cards can be a convenient way to manage your finances, they can also be risky. Credit card fraud is the unauthorized use of someone else's credit card or credit card information to make purchases or withdraw cash.
It is important that credit card companies are able to recognize fraudulent credit card transactions so that customers are not charged for items that they did not purchase. 
The dataset contains transactions made by credit cards in September 2013 by European cardholders. This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.
We have to build a classification model to predict whether a transaction is fraudulent or not.

The following are the steps that have been employed towards attempting to solve this problem statement: 

	Exploratory Data Analysis: Analyze and understand the data to identify patterns, relationships, and trends in the data by using Descriptive Statistics and Visualizations. 

Data Source Information

Time: Represents the number of seconds elapsed between the current transaction and the first transaction recorded in the dataset.

Amount: Denotes the transaction amount associated with each transaction.

Class: Serves as a label indicating the nature of the transaction. It takes a value of 1 for fraudulent transactions and 0 for legitimate ones.

V1-V28: May be result of a PCA Dimensionality reduction to protect user identities and sensitive features

	Data Cleaning: This might include standardization, handling the missing values and outliers in the data. 
No null values are noticed in the raw dataset.

	Dealing with Imbalanced data: This data set is highly imbalanced. The data should be balanced using the appropriate methods before moving onto model building.
While performing the EDA, it could be seen that only 492 (or 0.172%) of transaction are fraudulent. That means the data is highly unbalanced with respect with target variable Class.This imbalance problem may affect the performance of a model trained on this dataset. It may be necessary to use techniques such as oversampling, undersampling, or class weighting to handle the class imbalance problem when building a model for fraud detection.

Visualisation:
From the heatmap, it can be observed that there are no strong positive or negative correlations between any pairs of variables in the dataset. The strongest correlations are found: Time and V3, with a correlation coefficient of -0.42 Amount and V2, with a correlation coefficient of -0.53 Amount and V4, with a correlation coefficient of 0.4. Although these correlations are relatively high, the risk of multicollinearity is not expected to be significant. Overall, the heatmap suggests that there are no highly correlated variables that need to be removed before building a machine learning model.

Each scatter plot represents the relationship between the 'Time' and 'Amount' features for both legitimate (Class 0) and fraudulent (Class 1) transactions.
The plots and graphs clearly indicate that the dataset is highly imbalanced, with a vast majority of transactions being non-fraudulent (class 0) and a relatively small number of transactions being fraudulent (class 1). To address this imbalance, we need to differentiate between the legitimate and fraudulent data and use techniques such as SMOTE (Synthetic Minority Over-sampling Technique) to balance the data. Instead of undersampling, SMOTE oversamples the minority class by generating synthetic samples to achieve a more balanced distribution of classes.

We also checked the fraudulent transactions occur more often during certain time frame.

	Feature Engineering: 
When we received the dataset, dimensionality reduction was already performed in order to protect user identities and sensitive features.

	Model Selection: Choose the most appropriate model that can be used for this project. 
Various models were implemented to perform the classifications as the following mentioned below:
Logistic Regression
HistGradientBoostingClassifier
Decision Tree
XGBoost

Logistic model seems to perform very well, with high precision, recall, accuracy, and ROC AUC score for both classes. This suggests that the model is effective in identifying fraudulent transactions while minimizing false positives.
HGBC model demonstrates perfect performance on the test set, achieving 100% accuracy with perfect precision, recall, and F1-score for both classes. This suggests that the model is highly effective in distinguishing between legitimate and fraudulent transactions in this dataset.
Decision Tree model performs exceptionally well in distinguishing between legitimate and fraudulent transactions, as shown by its high accuracy, precision, recall, F1-score, and ROC AUC score.
XGBoost model demonstrates exceptional performance in distinguishing between legitimate and fraudulent transactions, achieving perfect classification results across all evaluation metrics. This indicates that the model is highly effective and reliable for fraud detection in this dataset.

 
	Model Validation: Evaluate the performance of the model on data that was not used during the training process. The goal is to estimate the model's ability to generalize to new, unseen data and to identify any issues with the model, such as overfitting. 

Overall, the models, including Logistic Regression, HistGradientBoostingClassifier, Decision Tree, and XGBoost, perform well in detecting fraudulent transactions. However, based on the comparison, the HistGradientBoostingClassifier stands out as the best-performing model across multiple metrics. 

![image](https://github.com/Abhik911/Find-Defaulters-Prediction-of-Credit-Card-fraud-/assets/67280652/c0a7b280-df6e-45fe-81d4-9091e2aaa2e2)


 



