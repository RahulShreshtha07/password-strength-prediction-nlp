# Datasets

This directory contains the password strength prediction datasets split across three CSV files for the Password Strength Prediction project.

## Dataset Files

### Primary Dataset (Divided into 2 parts)

#### `pwlds_part-1.csv`
- **Description**: First part of the primary password dataset
- **Format**: CSV (Comma-Separated Values)
- **Rows**: [Insert number of rows]
- **Columns**: Password samples with strength labels and engineered features

#### `pwlds_part-2.csv`
- **Description**: Second part of the primary password dataset
- **Format**: CSV (Comma-Separated Values)
- **Rows**: [Insert number of rows]
- **Columns**: Password samples with strength labels and engineered features

### Secondary Dataset

#### `secondary_data.csv`
- **Description**: Secondary validation/testing dataset
- **Format**: CSV (Comma-Separated Values)
- **Rows**: [Insert number of rows]
- **Columns**: Password samples with strength labels
- **Purpose**: Used for validation and testing of model performance

## Overview

The project utilizes password datasets for training and evaluating an NLP-based password strength prediction model. The primary dataset was split into two CSV files to manage file size efficiently within GitHub's limits.

## How to Use

### Step 1: Load the Primary Dataset (Both Parts)

Since the primary dataset is divided into two parts, you need to load and concatenate them:

```python
import pandas as pd

# Load both parts of the primary dataset
part1 = pd.read_csv('datasets/pwlds_part-1.csv')
part2 = pd.read_csv('datasets/pwlds_part-2.csv')

# Concatenate the parts
primary_data = pd.concat([part1, part2], ignore_index=True)

print(f"Primary dataset shape: {primary_data.shape}")
print(f"Columns: {primary_data.columns.tolist()}")
print(primary_data.head())
```

### Step 2: Load the Secondary Dataset

```python
# Load the secondary dataset
secondary_data = pd.read_csv('datasets/secondary_data.csv')

print(f"Secondary dataset shape: {secondary_data.shape}")
print(secondary_data.head())
```

### Step 3: Data Preprocessing

Before using these datasets, ensure the following preprocessing steps:

1. **Check for Missing Values**
   ```python
   print(primary_data.isnull().sum())
   print(secondary_data.isnull().sum())
   ```

2. **Explore Data Distribution**
   ```python
   # Check password strength distribution
   print(primary_data['strength'].value_counts())
   print(secondary_data['strength'].value_counts())
   ```

3. **Feature Engineering** (if needed)
   - Extract linguistic features
   - Analyze character composition
   - Calculate entropy and complexity metrics

4. **Normalize/Scale Features** (if applicable)
   ```python
   from sklearn.preprocessing import StandardScaler
   scaler = StandardScaler()
   ```

5. **Train-Test Split**
   ```python
   from sklearn.model_selection import train_test_split
   X_train, X_test, y_train, y_test = train_test_split(
       X, y, test_size=0.2, random_state=42
   )
   ```

## Dataset Features

Expected columns in the datasets:

- **password**: The password string
- **strength**: Target label (0=Weak, 1=Fair, 2=Good, 3=Strong)
- **length**: Length of the password
- **special_chars**: Count of special characters
- **digits**: Count of numeric digits
- **uppercase**: Count of uppercase letters
- **lowercase**: Count of lowercase letters
- Additional engineered features based on NLP analysis

## Important Notes

⚠️ **Security & Privacy**
- These datasets contain password examples for research purposes only
- Do not use these datasets with real passwords or sensitive information
- Handle with care and follow data privacy regulations
- Do not share these files publicly

📝 **Data Guidelines**
- All passwords in these datasets are synthetic or from public password lists
- Intended for machine learning research and model training
- Not representative of actual user passwords

## File Size Information

| File | Size | Records |
|------|------|----------|
| pwlds_part-1.csv | [Size] | [Records] |
| pwlds_part-2.csv | [Size] | [Records] |
| secondary_data.csv | [Size] | [Records] |
| **Total** | **[Total Size]** | **[Total Records]** |

## Merging the Datasets

For complete dataset analysis:

```python
# Combine all datasets
combined_data = pd.concat([primary_data, secondary_data], ignore_index=True)
print(f"Combined dataset shape: {combined_data.shape}")
```

## References & Citations

If you use these datasets in your research, please cite:
- Source/Original Dataset: [Insert source]
- Dataset Preparation: RahulShreshtha07/password-strength-prediction-nlp

## Data Quality Checks

Recommended checks before model training:

```python
# Check for duplicates
print(f"Duplicate rows: {primary_data.duplicated().sum()}")

# Check data types
print(primary_data.dtypes)

# Statistical summary
print(primary_data.describe())
```

## Support & Issues

If you encounter issues with the datasets:
1. Check file encoding (should be UTF-8)
2. Verify CSV format and delimiters
3. Ensure all columns are present
4. Open an issue on the repository for assistance

---

**Last Updated**: January 15, 2026
**Dataset Version**: 1.0
**Maintained By**: RahulShreshtha07
