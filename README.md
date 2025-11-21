

---

# ✅ **Task 4 — Logistic Regression (Binary Classification)**

### Professional, Organized, Table-Structured README

---

## **1. Project Summary**

This project implements a complete **binary classification pipeline** using **Logistic Regression**, including data preprocessing, feature standardization, model training, performance evaluation, ROC analysis, and threshold tuning.

---

## **2. Dataset Information**

| Attribute    | Description                                 |
| ------------ | ------------------------------------------- |
| Dataset Name | Breast Cancer Wisconsin Diagnostic Dataset  |
| Source       | Scikit-learn built-in datasets              |
| Samples      | 569 rows                                    |
| Features     | 30 numerical features                       |
| Target       | 0 = Malignant, 1 = Benign                   |
| Format       | Numpy arrays converted to Pandas DataFrames |

---

## **3. Repository Structure**

| File Name               | Purpose                                             |
| ----------------------- | --------------------------------------------------- |
| `task4.ipynb`           | Full implementation of logistic regression pipeline |
| `task4_predictions.csv` | Saved probabilities and predicted labels            |
| `task4_model.pkl`       | Serialized trained model (optional)                 |
| `README.md`             | Documentation for Task 4                            |

---

## **4. Machine Learning Pipeline Overview**

| Step                    | Description                                   | Outcome                             |
| ----------------------- | --------------------------------------------- | ----------------------------------- |
| **1. Data Loading**     | Load dataset using `load_breast_cancer()`     | X and y created as DataFrames       |
| **2. Train–Test Split** | 80% training, 20% testing                     | Balanced sets with stratification   |
| **3. Feature Scaling**  | Standardization via `StandardScaler`          | Normalized numeric input features   |
| **4. Model Training**   | Logistic Regression (`max_iter=1000`)         | Trained binary classifier           |
| **5. Prediction**       | Predict labels + probabilities                | Two outputs: class & probability    |
| **6. Evaluation**       | Confusion Matrix, Precision, Recall, Accuracy | Full classification assessment      |
| **7. ROC Curve**        | Measure TPR vs FPR                            | Compute AUC score                   |
| **8. Threshold Tuning** | Adjust threshold 0.3–0.7                      | Analyze precision–recall trade-offs |

---

## **5. Model Evaluation Results**

### **5.1 Confusion Matrix**

|              | Predicted 0 | Predicted 1 |
| ------------ | ----------- | ----------- |
| **Actual 0** | TN          | FP          |
| **Actual 1** | FN          | TP          |

(Actual numerical results appear in the notebook.)

---

### **5.2 Classification Metrics**

| Metric        | Meaning                             |
| ------------- | ----------------------------------- |
| **Accuracy**  | Overall correctness                 |
| **Precision** | Quality of positive predictions     |
| **Recall**    | Coverage of actual positives        |
| **F1-score**  | Harmonic mean of precision & recall |
| **ROC-AUC**   | Ability to separate classes         |

---

## **6. Threshold Tuning Analysis**

| Threshold | Behavior                       | Use Case                                   |
| --------- | ------------------------------ | ------------------------------------------ |
| **0.30**  | Higher recall, lower precision | Medical screening (reduce false negatives) |
| **0.50**  | Balanced                       | Default logistic regression                |
| **0.70**  | Higher precision, lower recall | Fraud detection (reduce false positives)   |

This demonstrates how adjusting probability cutoffs affects model behavior.

---

## **7. Sigmoid Function Explanation**

Logistic regression converts linear outputs into probabilities using the **sigmoid**:

[
\sigma(z) = \frac{1}{1 + e^{-z}}
]

### **Probability Interpretation Table**

| z value       | σ(z) output | Meaning        |
| ------------- | ----------- | -------------- |
| Very Negative | ~0.0        | Strong Class 0 |
| 0             | 0.5         | Uncertain      |
| Very Positive | ~1.0        | Strong Class 1 |

---

## **8. How to Execute the Project**

### **8.1 Requirements**

```
numpy
pandas
matplotlib
seaborn
scikit-learn
```

### **8.2 Run Instructions**

| Step | Action                                 |
| ---- | -------------------------------------- |
| 1    | Open `task4.ipynb` in Jupyter Notebook |
| 2    | Run all cells sequentially             |
| 3    | View performance metrics and plots     |
| 4    | Check generated files (`csv`, `pkl`)   |

---

## **9. Conclusion**

This project delivers a complete binary classification workflow using Logistic Regression.
It covers preprocessing, standardization, model training, ROC analysis, and threshold examination.
The results demonstrate high performance on the Breast Cancer dataset and provide clear insight into how logistic regression behaves under different probability thresholds.

---


