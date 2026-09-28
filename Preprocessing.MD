# Preprocessing

## Overview
This document describes the preprocessing steps applied to the Avazu CTR 
Prediction dataset. The preprocessing prepares the raw data for feature 
engineering and model training.

## Notebook
The preprocessing code is located in `notebooks/01_preprocessing.ipynb`.

## Steps Applied

### 1. Data Loading
- Loaded a sample of **1,000,000 rows** from the full Avazu dataset (which 
contains 40,428,967 rows).
- The full dataset was not used to keep training times manageable.

### 2. Dropping Irrelevant Columns
- Dropped the `id` column (unique row identifier with no predictive 
value).

### 3. Missing Values
- The dataset had **no missing values** in any column.

### 4. Target Variable
- The target is `click` (binary: 1 = clicked, 0 = not clicked).

### 5. Categorical Encoding
- Applied **Label Encoding** to all categorical (object type) columns.
- Columns encoded: `site_id`, `site_domain`, `site_category`, `app_id`, 
`app_domain`, `app_category`, `device_id`, `device_ip`, `device_model`.

### 6. Feature Scaling
- Applied **MinMaxScaler** to scale all features to the range [0, 1].
- Scaling is required for Logistic Regression (Model 1) to ensure all 
features contribute equally.

### 7. Train/Test Split
- Split the data into **80% training** and **20% testing**.
- Used `stratify=y` to preserve the class distribution in both sets.
- `random_state=42` for reproducibility.

## Output Files
The preprocessing script saves the following files to the `datasets/` 
folder:
- `X_train.pkl` – Scaled training features
- `X_test.pkl` – Scaled testing features
- `y_train.pkl` – Training target
- `y_test.pkl` – Testing target

## How to Run
1. Open `notebooks/01_preprocessing.ipynb` in Jupyter Notebook.
2. Ensure `train.csv` is located in the `datasets/` folder.
3. Run all cells sequentially.
4. The processed data will be saved as pickle files in `datasets/`.

## Results
- **Training set:** 800,000 rows × 22 features
- **Testing set:** 200,000 rows × 22 features

