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

## Installation

1. Clone the repository:
```bash
git clone https://github.com/RahulShreshtha07/password-strength-prediction-nlp.git
cd password-strength-prediction-nlp
```

2. Create a virtual environment (optional but recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\\Scripts\\activate
```

3. Install required dependencies:
```bash
pip install -r requirements.txt
```

## Usage

### Running the Notebook

1. Start Jupyter Notebook:
```bash
jupyter notebook
```

2. Open `Password_strength_predictor.ipynb` from the notebooks folder

3. Execute all cells to:
   - Load and explore the datasets
   - Build NLP-based features (TF-IDF)
   - Engineer custom features (entropy, repetition)
   - Train the Logistic Regression model
   - Evaluate performance on both datasets

### Dataset Structure

The datasets are located in the `datasets/` folder:

- **primary_data.csv**: Primary dataset (PWLDS) with password strength labels
  - Features: Raw password strings
  - Target: Strength categories
  
- **secondary_data.csv**: Secondary dataset (Kaggle) for cross-validation
  - Features: Raw password strings
  - Target: Strength categories

## Project Structure

```
password-strength-prediction-nlp/
├── README.md                          # Project documentation
├── requirements.txt                    # Project dependencies
├── .gitignore                         # Git ignore file
├── Password_strength_predictor.ipynb  # Main Jupyter notebook
└── datasets/                          # Data folder
    ├── primary_data.csv                 # Primary dataset (PWLDS)
    └── secondary_data.csv               # Secondary dataset (Kaggle)
```

## Results & Insights

- **Primary Dataset Performance**: Macro F1 Score = 0.8876
- **Secondary Dataset Performance**: Macro F1 Score = 0.9994
- **Key Finding**: Strong cross-dataset generalization achieved through effective feature engineering



## Author
Rahul Shreshtha
