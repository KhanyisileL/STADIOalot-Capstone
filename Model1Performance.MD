# Model 1 Performance: Logistic Regression

## Overview
This document presents the performance results of Model 1 (Logistic Regression) applied to the Avazu CTR dataset.

## Performance Calculation File
The performance metrics for Model 1 are calculated in `notebooks/03_model1_logistic_regression.ipynb` (Cells 5 and 6).

## How to Use
1. Open `notebooks/03_model1_logistic_regression.ipynb` in Jupyter.
2. Ensure the engineered `.pkl` files are in `datasets/`.
3. Run all cells sequentially.
4. The final evaluation cell produces the metrics below.

## Evaluation Metrics

- Accuracy:  0.5339
- AUC-ROC:   0.6353
- Precision: 0.2155
- Recall:    0.7229
- F1 Score:  0.3320

## Confusion Matrix

- True Negatives (Actual No-Click, Predicted No-Click):  83,615
- False Positives (Actual No-Click, Predicted Click):    84,341
- False Negatives (Actual Click, Predicted No-Click):     8,878
- True Positives (Actual Click, Predicted Click):        23,166

## Classification Report

- Class 0 (No Click): Precision=0.90, Recall=0.50, F1=0.64, Support=167,956
- Class 1 (Click):    Precision=0.22, Recall=0.72, F1=0.33, Support=32,044

## Statistical Interpretation

### AUC-ROC = 0.6353
The AUC-ROC score of 0.6353 indicates that the Logistic Regression model performs meaningfully better than random (0.5). It correctly ranks a random click observation above a random no-click observation approximately 63.5% of the time.

### Precision vs Recall Trade-off
- Precision (0.2155): Of all predicted clicks, only ~22% were actual clicks. This means many false positives.
- Recall (0.7229): The model correctly identified 72% of all actual clicks.
- The model was tuned with class_weight='balanced' to favour recall, which is appropriate for advertising where missing a potential click (false negative) is costly.

### Limitations
- The accuracy of 0.5339 is low because the dataset is imbalanced (only 16% clicks).
- Precision is limited by the linear decision boundary of Logistic Regression.
- AUC-ROC of 0.64 suggests the model captures some signal but misses non-linear feature interactions.

## Conclusion
Logistic Regression provides a reasonable baseline for CTR prediction, but its linear nature limits its ability to capture complex patterns in the Avazu dataset.
