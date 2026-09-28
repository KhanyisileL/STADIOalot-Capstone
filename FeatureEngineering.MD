# Feature Engineering

## Overview
This document describes the feature engineering applied to the 
preprocessed Avazu CTR dataset.

## Notebook
The feature engineering code is located in 
`notebooks/02_feature_engineering.ipynb`.

## Features Created

### Frequency Encoding Features
- **device_id_count** – How frequently each device ID appears in the 
training data. High-frequency devices may indicate heavy users whose click 
behaviour is more predictable.
- **device_ip_count** – How frequently each IP appears. Captures 
shared-connection patterns (e.g., corporate networks, public WiFi).
- **device_model_count** – How frequently each device model appears. 
Popular models may show different click behaviour than niche devices.

## Preprocessing Note
Time-based features (`day_of_week`, `hour_of_day`) were extracted during 
the preprocessing phase and are already included in the 24 base features.

## How to Run
1. Open `notebooks/02_feature_engineering.ipynb` in Jupyter.
2. Ensure the four `.pkl` files from preprocessing are in the `datasets/` 
folder.
3. Run all cells sequentially.
4. Engineered features are saved as `X_train_engineered.pkl` and 
`X_test_engineered.pkl` in the `datasets/` folder.

## Results
- Base features (after preprocessing): 24
- Engineered features: 27 (24 base + 3 frequency-encoded columns)
- Training set: 800,000 rows × 27 columns
- Test set: 200,000 rows × 27 columns

