# Comparison of Model 1 and Model 2

## Overview

This document compares **Model 1 (Logistic Regression)** and **Model 2 (HistGradientBoostingClassifier)** for predicting Click-Through Rate (CTR) using the Avazu dataset.

## Model Performance Comparison

* **Accuracy:** Model 1 = 0.5339, Model 2 = 0.6489 → Model 2 improved by 21.5%.
* **AUC-ROC:** Model 1 = 0.6353, Model 2 = 0.7596 → Model 2 improved by 19.6%.
* **Precision:** Model 1 = 0.2155, Model 2 = 0.2801 → Model 2 improved by 30%.
* **Recall:** Model 1 = 0.7229, Model 2 = 0.7589 → Model 2 improved by 5%.
* **F1 Score:** Model 1 = 0.3320, Model 2 = 0.4092 → Model 2 improved by 23.3%.

Overall, **Model 2 performed better on all the measured metrics**.

## Confusion Matrix Comparison

* **True Positives:** Model 1 = 23,166, Model 2 = 24,317 → Model 2 correctly identified more clicks.
* **True Negatives:** Model 1 = 83,615, Model 2 = 105,455 → Model 2 correctly identified more non-clicks.
* **False Positives:** Model 1 = 84,341, Model 2 = 62,501 → Model 2 made fewer incorrect positive predictions.
* **False Negatives:** Model 1 = 8,878, Model 2 = 7,727 → Model 2 missed fewer actual clicks.

### Key Finding

Model 2 had **fewer False Positives** and **more True Positives**. This means it was better at identifying clicks while making fewer incorrect predictions.

## Statistical Analysis

### AUC-ROC

Model 2 had an AUC-ROC of **0.7596**, compared with **0.6353** for Model 1.

This shows that Model 2 was better at **distinguishing between users who clicked and users who did not click**.

### McNemar's Test

McNemar's test can be used to compare two models when they are tested on the same data.

The differences between the two models suggest that there may be a **statistically significant difference** between their results. However, an actual McNemar's test should be performed to confirm this.

### Improvement in Performance

* **F1 Score:** improved from 0.3320 to 0.4092.
* **Precision:** improved from 0.2155 to 0.2801.
* **AUC-ROC:** improved from 0.6353 to 0.7596.

These results show that Model 2 performed better than Model 1.

## Business Meaning

For **STADIOalot**, the better performance of Model 2 could provide several benefits:

1. **Higher Precision:** The model is better at identifying users who are likely to click an ad.
2. **Better Recall:** The model identifies more of the actual clicks.
3. **Fewer False Positives:** The model makes fewer incorrect click predictions.
4. **Better AUC-ROC:** The model is better at ranking sponsored products based on the likelihood of a user clicking.

## Conclusion

Based on the results, **Model 2 performed better than Model 1 across all the measured metrics**.

* AUC-ROC improved by **20%**.
* F1 Score improved by **23%**.
* Precision improved by **30%**.
* Recall improved by **5%**.

The results suggest that **HistGradientBoostingClassifier is a strong model for this CTR prediction task**.

## Next Steps

1. Test and tune Model 2 further to see if its performance can improve.
2. Try different settings and parameters for the model.
3. Add more useful features to improve the predictions.
4. Test the model in a real advertising environment to see how it performs in practice.
