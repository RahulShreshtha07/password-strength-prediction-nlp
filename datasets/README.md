# Datasets

This directory contains the compressed dataset files used in the Password Strength Prediction project.

## Overview

The project utilizes two primary datasets for training and evaluation of the NLP-based password strength prediction model:

1. **Password Dataset 1** - Training dataset with labeled password strength categories
2. **Password Dataset 2** - Validation/evaluation dataset with diverse password samples

## Dataset Files

### File: `datasets.zip` (or compressed archive)

This archive contains the two datasets in their processed form, ready for use in the model training pipeline.

**Size:** [Insert actual size]
**Format:** ZIP archive
**Compression Ratio:** [Insert ratio]

## How to Use

### Step 1: Extract the Archive

```bash
# Extract the datasets
unzip datasets.zip

# Or if using tar.gz
tar -xzf datasets.tar.gz
```

### Step 2: Verify Extraction

After extraction, you should see the following structure:

```
datasets/
├── dataset1/
│   ├── train.csv
│   ├── test.csv
│   └── metadata.json
├── dataset2/
│   ├── validation.csv
│   ├── test.csv
│   └── metadata.json
└── README.md (this file)
```

### Step 3: Load in Python

```python
import pandas as pd

# Load dataset 1
dataset1_train = pd.read_csv('datasets/dataset1/train.csv')
dataset1_test = pd.read_csv('datasets/dataset1/test.csv')

# Load dataset 2
dataset2_val = pd.read_csv('datasets/dataset2/validation.csv')
dataset2_test = pd.read_csv('datasets/dataset2/test.csv')
```

## Dataset Details

### Dataset 1: Training Dataset

- **Samples:** [Number of samples]
- **Features:** [Number of features]
- **Password Strength Classes:** Weak, Fair, Good, Strong
- **Source:** [Dataset source]
- **License:** [License information]

### Dataset 2: Validation Dataset

- **Samples:** [Number of samples]
- **Features:** [Number of features]
- **Password Strength Classes:** Weak, Fair, Good, Strong
- **Source:** [Dataset source]
- **License:** [License information]

## Feature Description

Key features in the datasets:

- `password`: The actual password string
- `strength`: Target label (0-3 representing Weak, Fair, Good, Strong)
- `length`: Length of the password
- `special_chars`: Count of special characters
- `digits`: Count of numeric digits
- `uppercase`: Count of uppercase letters
- `lowercase`: Count of lowercase letters

## Data Preprocessing

Before using these datasets, ensure the following preprocessing steps:

1. **Text Normalization:** Convert passwords to standardized format
2. **Feature Engineering:** Extract linguistic and structural features
3. **Handling Missing Values:** Check for and handle any NULL values
4. **Train-Test Split:** Use provided train/test split or create custom splits
5. **Scaling/Normalization:** Normalize numerical features as needed

## Important Notes

- **Sensitive Information:** These datasets contain password examples. Handle with care and do not share publicly.
- **Use Case:** Intended for research and model training purposes only.
- **Data Privacy:** Comply with all data privacy regulations when using these datasets.
- **Attribution:** When using these datasets, please cite the original sources.

## References

If you use these datasets, please reference:

- Dataset 1: [Citation/Link]
- Dataset 2: [Citation/Link]

## Support

For issues or questions regarding the datasets, please open an issue on the repository.

---

**Last Updated:** [Date]
**Maintained By:** RahulShreshtha07
