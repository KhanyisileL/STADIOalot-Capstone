# Model 2 Performance: HistGradientBoostingClassifier

## Overview
This document presents the performance results of Model 2 (HistGradientBoostingClassifier) applied to the Avazu CTR dataset.

## Performance Calculation File
The performance metrics for Model 2 are calculated in `notebooks/04_model2_gradientboosting.ipynb` (Cells 6 and 7).

## How to Use
1. Open `notebooks/04_model2_gradientboosting.ipynb` in Jupyter.
2. Ensure the engineered `.pkl` files are in `datasets/`.
3. Run all cells sequentially.
4. The final evaluation cell produces the metrics below.

## Evaluation Metrics

- Accuracy:  0.6489
- AUC-ROC:   0.7596
- Precision: 0.2801
- Recall:    0.7589
- F1 Score:  0.4092

## Confusion Matrix

- True Negatives (Actual No-Click, Predicted No-Click): 105,455
- False Positives (Actual No-Click, Predicted Click):    62,501
- False Negatives (Actual Click, Predicted No-Click):     7,727
- True Positives (Actual Click, Predicted Click):        24,317

## Classification Report

- Class 0 (No Click): Precision=0.93, Recall=0.63, F1=0.75, Support=167,956
- Class 1 (Click):    Precision=0.28, Recall=0.76, F1=0.41, Support=32,044

## Statistical Interpretation

### AUC-ROC = 0.7596
The AUC-ROC of 0.7596 represents a substantial improvement over Model 1 (0.6353). The model correctly ranks a random click above a random no-click 76% of the time. This indicates strong discriminative power.

### Precision vs Recall Trade-off
- Precision (0.2801): Improved by 30% compared to Model 1 (0.2155).
- Recall (0.7589): Slightly improved over Model 1 (0.7229).
- F1 Score (0.4092): Improved by 23% over Model 1 (0.3320).

### Why Gradient Boosting Performs Better
1. Non-linear decision boundaries: Tree-based models capture complex feature interactions that Logistic Regression cannot.
2. Automatic feature interactions: Gradient boosting combines features through splits, effectively capturing higher-order relationships.
3. Robust to outliers: Tree-based methods are less sensitive to extreme feature values.
4. Built-in regularisation: The max_depth and learning_rate parameters prevent overfitting.

### Statistical Strength
The confusion matrix shows:
- 24,317 True Positives (correctly identified clicks)
- 7,727 False Negatives (missed clicks)
- 62,501 False Positives (wrongly flagged clicks)
- 105,455 True Negatives (correctly identified non-clicks)

Compared to Model 1, Model 2 reduced false positives from 84,341 to 62,501 (a 26% reduction) while catching slightly more true clicks.

## Conclusion
Model 2 (Gradient Boosting) substantially outperforms Model 1 (Logistic Regression) across every evaluation metric. The improvement in AUC-ROC from 0.6353 to 0.7596 demonstrates the value of tree-based ensemble methods for CTR prediction.
