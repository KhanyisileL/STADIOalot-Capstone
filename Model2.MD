# Model 2: Gradient Boosting (HistGradientBoostingClassifier)

## Overview
This document describes Model 2 (HistGradientBoostingClassifier) applied 
to the Avazu CTR dataset. This is a tree-based gradient boosting model 
from scikit-learn, chosen as an alternative to XGBoost due to macOS 
library dependency issues.

## Notebook
The Model 2 code is located in 
`notebooks/04_model2_gradientboosting.ipynb`.

## Technique
HistGradientBoostingClassifier - a gradient boosting decision tree 
algorithm built into scikit-learn. It is functionally equivalent to 
XGBoost/LightGBM, but ships natively with sklearn, avoiding external 
library dependencies.

## Data Preprocessing
- Used the same preprocessed and feature-engineered data as Model 1.
- 27 features total: 24 scaled base features + 3 frequency-encoded 
features.

## Feature Engineering
- Day of week and hour of day (extracted during preprocessing).
- Frequency encoding for device_id, device_ip, device_model.

## Hyperparameters
| Parameter | Value |
| :--- | :--- |
| max_iter | 100 |
| max_depth | 6 |
| learning_rate | 0.1 |
| random_state | 42 |
| class_weight | balanced |

## Handling Class Imbalance
The Avazu dataset has an imbalance ratio of 5.24:1 (671,825 negatives to 
128,175 positives in the training set). Addressed with 
`class_weight='balanced'`.

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
| Accuracy | 0.6489 |
| AUC-ROC | 0.7596 |
| Precision | 0.2801 |
| Recall | 0.7589 |
| F1 Score | 0.4092 |

### Confusion Matrix
- True Negatives:  105,455
- False Positives: 62,501
- False Negatives: 7,727
- True Positives:  24,317

## How to Run
1. Open `notebooks/04_model2_gradientboosting.ipynb` in Jupyter.
2. Ensure the engineered `.pkl` files are in `datasets/`.
3. Run all cells sequentially.
4. The trained model is saved to `models/model2_histgradient.pkl`.

