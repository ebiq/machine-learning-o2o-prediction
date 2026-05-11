# O2O Coupon Usage Prediction Based on Machine Learning

## Project Introduction

This project focuses on predicting whether users will redeem O2O coupons within 15 days after receiving them.

Based on historical user transaction behavior data, this project applies machine learning classification algorithms to analyze user consumption patterns and coupon usage behavior. The project includes data preprocessing, exploratory data analysis (EDA), feature engineering, model training, and performance evaluation.

The implemented models include:

- Decision Tree
- Gradient Boosting Decision Tree (GBDT)
- XGBoost

---

# Project Objectives

- Analyze user coupon consumption behavior
- Explore merchant coupon release strategies
- Construct machine learning features from user behavior data
- Build classification models for coupon redemption prediction
- Compare the performance of multiple machine learning algorithms

---

# Dataset Description

The dataset contains O2O platform user behavior information.

Main features include:

| Feature | Description |
|---|---|
| user_id | User ID |
| merchant_id | Merchant ID |
| coupon_id | Coupon ID |
| discount_rate | Coupon discount rate |
| distance | Distance between user and merchant |
| date_received | Coupon received date |
| date | Consumption date |

Prediction target:

- Predict whether a user will redeem a coupon within 15 days after receiving it.

---

# Exploratory Data Analysis (EDA)

The project performs exploratory data analysis on:

- User consumption frequency
- Coupon distribution patterns
- Merchant coupon release behavior
- Distance distribution
- Coupon redemption trends
- User coupon usage behavior

Visualization methods include:

- Pie charts
- Line charts
- Bar charts
- ROC curves

---

# Data Preprocessing

The preprocessing stage includes:

- Missing value handling
- Date format conversion
- Coupon discount normalization
- Feature cleaning
- Label construction

Coupon discount formats such as:

```python
300:30 -> 0.90
0.8 -> 0.80
```

were unified into normalized discount rates.

---

# Feature Engineering

Feature engineering is implemented in:

```python
feature_name.py
```

Constructed features include:

## User Features

- User coupon usage count
- User consumption frequency
- Coupon usage rate
- Average coupon redemption interval
- Number of unused coupons

## Merchant Features

- Merchant coupon release count
- Merchant coupon usage rate
- Merchant coupon redemption interval

## Coupon Features

- Coupon popularity
- Coupon usage rate

## User-Merchant Interaction Features

- User consumption count for a merchant
- User coupon usage count for a merchant
- User coupon receiving behavior

---

# Machine Learning Models

The following classification models were implemented:

## 1. Decision Tree

- CART-based classification model
- Used as baseline model

## 2. Gradient Boosting Decision Tree (GBDT)

- Ensemble learning method
- Improved prediction performance

## 3. XGBoost

- Gradient boosting framework
- Achieved the best overall performance

---

# Model Evaluation

Evaluation metrics include:

- Accuracy
- Precision
- ROC Curve
- AUC Score

## Model Performance

| Model | AUC | Accuracy | Precision |
|---|---|---|---|
| Decision Tree | 0.9982 | 98.63% | 94.20% |
| GBDT | 0.9985 | 98.69% | 92.20% |
| XGBoost | 0.9985 | 98.68% | 92.18% |

---

# Project Structure

```text
o2o-coupon-prediction/
│
├── notebooks/
│   └── o2o_coupon_prediction.ipynb
│
├── src/
│   └── feature_name.py
│
├── results/
│   ├── roc_curve.png
│   └── evaluation_results.png
│
├── README.md
└── requirements.txt
```

---

# Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- XGBoost

---

# Key Findings

- Most coupons are not redeemed after being received.
- Distance between users and merchants significantly affects coupon usage.
- User historical behavior is highly correlated with coupon redemption probability.
- Ensemble learning models outperform single decision tree models.

---

# Future Improvements

Possible future optimizations include:

- Hyperparameter tuning using GridSearchCV
- Cross-validation
- SMOTE for imbalanced data handling
- Feature importance analysis
- Deep learning based prediction models

---

# Author

Machine Learning Project for O2O Coupon Usage Prediction
