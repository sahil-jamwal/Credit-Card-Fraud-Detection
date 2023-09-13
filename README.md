# Credit Card Fraud Detection

## Overview
This repository contains code and resources for building a credit card fraud detection model using machine learning techniques. The goal of this project is to develop a model that can effectively identify fraudulent credit card transactions in a highly imbalanced dataset.

### Dataset
The dataset used for this project contains credit card transactions made by European cardholders in September 2013. It includes a mix of legitimate and fraudulent transactions. Here are some key details about the dataset:

- Number of transactions: 284,807
- Number of fraud cases: 492
- Class imbalance: Positive class (frauds) accounts for only 0.172% of all transactions
- Features: Numerical features obtained through PCA transformation, 'Time,' and 'Amount'
- Target variable: 'Class' (1 for fraud, 0 for legitimate)

### Data Preprocessing
- Checked for missing values (no null values in the dataset).
- Explored the distribution of transaction amounts for both legitimate and fraudulent transactions.
- Balanced the dataset by performing random undersampling of the majority class (Class 0) to match the number of samples in the minority class (Class 1).
- Split the data into training and testing sets (80/20 split) while maintaining class distribution using stratified splitting.

### Model Building
- Trained a logistic regression model on the preprocessed data.
- Trained a Random Forest model on the preprocessed data.
- Evaluated both models using the Area Under the Precision-Recall Curve (AUPRC) as the primary metric, considering the class imbalance.

### Results
Here are the performance metrics for the models on the test dataset:

**Logistic Regression Metrics:**
- Precision: 0.9570
- Recall: 0.9082
- F1-Score: 0.9319
- AUPRC (Area Under the Precision-Recall Curve): 0.9148
- Confusion Matrix:
  [[95  4]
  [13 85]]
- ROC-AUC: 0.9339

 **Random Forest Metrics:**
- Precision: 0.9551
- Recall: 0.8673
- F1-Score: 0.9091
- AUPRC (Area Under the Precision-Recall Curve): 0.8944
- Confusion Matrix: 
  [[95 4]
  [13 85]]
- ROC-AUC: 0.9135


## Tech Stack
- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib/Seaborn

## Usage
You can use this project as a reference for credit card fraud detection using machine learning techniques.
