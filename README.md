# 💳 Loan Approval Prediction (Machine Learning)

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-ML-orange)
![Status](https://img.shields.io/badge/status-Completed-brightgreen)
![License](https://img.shields.io/badge/license-MIT-green)

A **machine learning classification project** that predicts whether a loan will default (`loan_status`) using structured customer and loan data.  
The project focuses on **data cleaning, feature engineering, encoding, and model tuning** with Random Forest.

---

## 📌 Project Overview

- Problem type: **Binary Classification**
- Target variable: `loan_status`
- Model: **RandomForestClassifier**
- Optimization: **RandomizedSearchCV**
- Evaluation metric: **ROC-AUC**
- Output: CSV submission file for predictions

---

## 🧠 Workflow

1. **Data Loading**
   - `train.csv`
   - `test.csv`
   - `sample_submission.csv`

2. **Data Cleaning**
   - Removed `id`
   - Capped outliers (`person_age`, `person_emp_length`)
   - Log-transformed income (`person_income_log`)

3. **Feature Engineering**
   - Numerical scaling with `StandardScaler`
   - One-hot encoding for nominal categorical features
   - Ordinal encoding for `loan_grade`

4. **Modeling**
   - Random Forest with class balancing
   - Hyperparameter tuning using `RandomizedSearchCV`

5. **Prediction & Export**
   - Final predictions saved as `sub2.csv`

---

## 🧪 Model & Tuning

```text
Model: RandomForestClassifier
Tuning: RandomizedSearchCV
Scoring: ROC-AUC
CV: 3-fold
