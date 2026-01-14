# Password Strength Prediction using NLP & Machine Learning

## Overview
This project predicts password strength using a hybrid approach that combines
NLP-based TF-IDF character features with advanced statistical feature engineering.

The goal is to assess password robustness while ensuring strong generalization
across datasets.

## Key Highlights
- NLP-based character TF-IDF modeling
- Custom entropy and repetition features
- Logistic Regression with engineered features
- Cross-dataset evaluation
- Near-perfect generalization on unseen data

## Datasets
- Primary dataset (PWLDS)
- Secondary dataset (Kaggle)

## Model Performance

| Dataset | Model | Macro F1 |
|-------|------|---------|
| Primary | Logistic Regression | 0.8876 |
| Secondary | Logistic Regression | 0.9994 |

## Tech Stack
- Python
- Pandas, NumPy
- Scikit-learn
- TF-IDF (NLP)

## Author
Rahul Shreshtha
