# Metrics

In machine learning, evaluation metrics help assess the performance of models. The choice of metric depends on the problem (classification, regression, ranking, etc.). Below are key classification metrics:

---

### 1. **Accuracy**

- Measures the proportion of correctly predicted instances out of the total instances.
- Formula:  
  \[
  Accuracy = \frac{TP + TN}{TP + TN + FP + FN}
  \]
- **Best for**: Balanced datasets where classes are equally represented.
- **Limitations**: Can be misleading in imbalanced datasets (e.g., if 95% of data is class A, a model predicting all A still gets 95% accuracy).

---

### 2. **Precision (Positive Predictive Value)**

- Measures how many of the predicted positive instances are actually correct.
- Formula:  
  \[
  Precision = \frac{TP}{TP + FP}
  \]
- **Best for**: When false positives (FP) are costly (e.g., spam detection—wrongly marking a legitimate email as spam is bad).
- **Limitations**: Doesn’t consider false negatives (FN), which may be important in some cases.

---

### 3. **Recall (Sensitivity or True Positive Rate)**

- Measures how many actual positive instances were correctly predicted.
- Formula:  
  \[
  Recall = \frac{TP}{TP + FN}
  \]
- **Best for**: When missing positive cases is costly (e.g., medical diagnoses—missing a cancer case is worse than a false alarm).
- **Limitations**: Doesn’t consider false positives (FP), which might matter in some cases.

---

### 4. **F1 Score (Harmonic Mean of Precision and Recall)**

- Balances precision and recall. It is useful when both false positives and false negatives matter.
- Formula:  
  \[
  F1 = 2 \times \frac{Precision \times Recall}{Precision + Recall}
  \]
- **Best for**: Imbalanced datasets where both false positives and false negatives are costly.
- **Limitations**: Doesn’t reflect the true negatives (TN).

---

### 5. **Specificity (True Negative Rate)**

- Measures how well the model identifies actual negatives.
- Formula:  
  \[
  Specificity = \frac{TN}{TN + FP}
  \]
- **Best for**: When correctly identifying negatives is important (e.g., fraud detection—wrongly flagging a non-fraudulent transaction can annoy customers).

---

### 6. **ROC Curve (Receiver Operating Characteristic)**

- Plots the **True Positive Rate (Recall)** vs. **False Positive Rate (FPR)** across different classification thresholds.
- **Best for**: Comparing classifiers across different probability thresholds.

---

### 7. **AUC-ROC (Area Under ROC Curve)**

- Measures the ability of the model to distinguish between classes.
- **Best for**: Assessing overall model performance across different threshold values.

---

### 8. **PR Curve (Precision-Recall Curve)**

- Plots **Precision** vs. **Recall** at different classification thresholds.
- **Best for**: Highly imbalanced datasets.

---

### 9. **Log Loss (Logarithmic Loss)**

- Measures how uncertain a model’s probability predictions are.
- **Best for**: Evaluating probabilistic models.

---

### 10. **Matthews Correlation Coefficient (MCC)**

- A balanced measure of classification quality.
- **Best for**: Imbalanced datasets.

---

### Summary Table

| Metric          | Formula                                 | Best For             | Weakness                             |
| --------------- | --------------------------------------- | -------------------- | ------------------------------------ |
| **Accuracy**    | \( \frac{TP + TN}{TP + TN + FP + FN} \) | Balanced datasets    | Fails on imbalanced data             |
| **Precision**   | \( \frac{TP}{TP + FP} \)                | When FP is costly    | Ignores FN                           |
| **Recall**      | \( \frac{TP}{TP + FN} \)                | When FN is costly    | Ignores FP                           |
| **F1 Score**    | \( 2 \times \frac{P \times R}{P + R} \) | Imbalanced data      | Ignores TN                           |
| **Specificity** | \( \frac{TN}{TN + FP} \)                | When TN is important | Ignores FN                           |
| **AUC-ROC**     | -                                       | Model comparison     | Can be misleading on imbalanced data |
| **PR Curve**    | -                                       | Imbalanced data      | -                                    |
