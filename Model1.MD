# Model 1: Logistic Regression

## Overview
This document describes Model 1 (Logistic Regression) applied to the Avazu 
CTR dataset.

## Notebook
The Model 1 code is located in 
`notebooks/03_model1_logistic_regression.ipynb`.

## Technique
Logistic Regression – a linear model for binary classification (click vs. 
no-click).

## Data Preprocessing
- Used the preprocessed and feature-engineered data from 
`X_train_engineered.pkl` and `X_test_engineered.pkl`.
- 27 features total: 24 scaled base features + 3 frequency-encoded 
features.

## Feature Engineering
- Day of week and hour of day (extracted during preprocessing).
- Frequency encoding for device_id, device_ip, device_model.

## Hyperparameters
| Parameter | Value |
| :--- | :--- |
| C | 1.0 |
| penalty | l2 |
| solver | lbfgs |
| max_iter | 1000 |
| class_weight | balanced |
| random_state | 42 |

## Handling Class Imbalance
The Avazu dataset is highly imbalanced (only ~16% of impressions result in 
a click). To address this:
- Used `class_weight='balanced'` so the model weights the minority class 
more heavily.
- Applied a prediction threshold of 0.5 on predicted probabilities.

## Evaluation Metrics
- Accuracy
- AUC-ROC
- Precision
- Recall
- F1 Score
- Confusion Matrix

## Results
| Metric | Value |
| :--- | :--- |
| Accuracy | 0.5339 |
| AUC-ROC | 0.6353 |
| Precision | 0.2155 |
| Recall | 0.7229 |
| F1 Score | 0.3320 |

## How to Run
1. Open `notebooks/03_model1_logistic_regression.ipynb` in Jupyter.
2. Ensure the engineered `.pkl` files are in `datasets/`.
3. Run all cells sequentially.
4. The trained model is saved to `models/model1_logistic.pkl`.

