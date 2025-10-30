Customer Churn Prediction

Project Overview
This project predicts customer churn for a telecom company using machine learning. The goal is to identify customers at risk of leaving the service so the business can take proactive retention actions.

Dataset
Contains customer demographic and service usage information.
Key features include tenure, contract type, monthly and total charges, and service subscriptions.
Target variable: Churn (0 = retained, 1 = churned).

Models Used
Logistic Regression, Random Forest Classifier, XGBoost Classifier

Data Preprocessing
Handled missing values and dropped irrelevant columns (e.g., customerID).
Scaled numeric features (tenure, MonthlyCharges, TotalCharges) using StandardScaler.
Encoded categorical variables via one-hot encoding.
Addressed class imbalance with class weights and threshold tuning.

Model Evaluation
Metrics used: Precision, Recall, F1-Score, ROC-AUC
Threshold tuning was applied to improve detection of churners.

Best performing model: Logistic Regression with threshold 0.35.

Model	Precision	Recall	F1-Score	ROC-AUC
Logistic Regression	0.44	0.90	0.59	0.8384
Random Forest	0.52	0.72	0.60	0.8161
XGBoost	0.47	0.77	0.58	0.8113

Feature Importance
Top features influencing churn:
Contract type (2-year contracts reduce churn)
Tenure (longer-tenured customers less likely to churn)
Internet service type (Fiber optic customers more likely to churn)
TotalCharges, MonthlyCharges
Service subscriptions like Streaming TV/Movies, Online Security, Phone Service

Key Insights
Churn is imbalanced (~25%), so threshold tuning is crucial.
Logistic Regression is interpretable and captures most churners (high recall).
Features like tenure, contract, and services are strong predictors.

