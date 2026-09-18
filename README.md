# credit_card-fraud-detection
# Credit Card Fraud Detection

## 📌 About the Project

This project focuses on detecting **fraudulent credit card transactions** using Machine Learning.

The dataset is highly imbalanced, with normal transactions being much more common than fraudulent transactions.

To handle this imbalance, **SMOTE** is applied to the training data, and an **XGBoost Classifier** is used for fraud detection.

---

## 🎯 Objective

The main objective is to identify whether a credit card transaction is:

- `0` → Normal Transaction
- `1` → Fraudulent Transaction

Since fraud cases are rare, the project focuses on handling class imbalance and reducing missed fraud cases.

---

## 📊 Dataset

The project uses a credit card transaction dataset containing transaction-related features and a target variable:

`Class`

- `0` → Normal
- `1` → Fraud

The dataset contains a highly imbalanced distribution of the two classes.

---

## 🔧 Technologies Used

- Python
- Pandas
- Matplotlib
- Scikit-learn
- XGBoost
- Imbalanced-learn
- Google Colab

---

## ⚙️ Methodology

The project follows these steps:

1. Load the dataset
2. Clean the dataset by handling missing values
3. Separate input features `X` and target `y`
4. Check the class distribution
5. Split the data into training and testing sets
6. Apply **SMOTE** to balance the training data
7. Create an **XGBoost Classifier**
8. Train the model
9. Generate fraud probabilities
10. Set a decision threshold of `0.30`
11. Generate final predictions
12. Evaluate the model
13. Analyze feature importance

---

## 🤖 Machine Learning Model

### XGBoost Classifier

XGBoost is a gradient boosting algorithm that builds multiple decision trees sequentially.

Each new tree tries to correct the errors made by previous trees.

The model is configured with:

- `n_estimators = 100`
- `max_depth = 5`
- `learning_rate = 0.1`

---

## ⚖️ Handling Class Imbalance

### SMOTE

SMOTE stands for **Synthetic Minority Over-sampling Technique**.

It generates synthetic samples of the minority class instead of simply duplicating existing samples.

In this project, SMOTE is applied **only to the training data** so that the test data remains realistic and unbiased.

---

## 🎚️ Decision Threshold

Instead of using the default threshold of `0.50`, a threshold of:

```text
0.30
