# Diabetes Prediction Analysis

This repository contains four Jupyter notebooks that explore different machine learning
models to predict diabetes based on various health metrics.

## Dataset Overview

All analyses use the **Pima Indians Diabetes** dataset, which consists of 768 samples
and 9 columns.

- **Total Samples**: 768
- **Target Variable**: `Outcome` (0 = No Diabetes, 1 = Diabetes)
- **Features**:
  - Pregnancies
  - Glucose
  - Blood Pressure
  - Skin Thickness
  - Insulin
  - BMI
  - Diabetes Pedigree Function
  - Age

---

## Models Implemented

### 1. K-Nearest Neighbors (KNN)
The `KNN.ipynb` notebook implements a K-Nearest Neighbors classifier.

- **Key Libraries**: `scikit-learn`, `pandas`, `numpy`, `seaborn`, `matplotlib`
- **Preprocessing**: `StandardScaler` to normalize feature scales — critical for
  distance-based algorithms like KNN
- **Evaluation**: Cross-validation scores and accuracy metrics to determine best K

### 2. Logistic Regression
The `Logistic_Regression.ipynb` notebook implements a Logistic Regression model.

- **Key Libraries**: `sklearn.linear_model.LogisticRegression`, `pandas`, `numpy`
- **Analysis**: Final model summary comparing training/testing sizes with detailed
  recall metrics for both classes
- **Evaluation**: Accuracy score, confusion matrix, classification report

### 3. Support Vector Machine (SVM)
The `SVM.ipynb` notebook implements a Support Vector Machine classifier.

- **Key Libraries**: `scikit-learn`, `pandas`, `numpy`, `seaborn`, `matplotlib`
- **Preprocessing**: `StandardScaler` — essential for margin-based algorithms like SVM
- **Kernel**: RBF (Radial Basis Function) by default
- **Evaluation**: Accuracy score, confusion matrix, classification report

### 4. Random Forest
The `Random_Forest.ipynb` notebook implements an ensemble-based Random Forest classifier.

- **Key Libraries**: `scikit-learn`, `pandas`, `numpy`, `seaborn`, `matplotlib`
- **Preprocessing**: Minimal scaling required — tree-based methods are scale-invariant
- **Hyperparameters**: Number of estimators, max depth, and min samples tuning
- **Evaluation**: Accuracy score, confusion matrix, classification report

---

## Performance Metrics

All notebooks evaluate performance using:

- **Accuracy Score**: Overall percentage of correct predictions
- **Confusion Matrix**: Counts for True Positives, True Negatives, False Positives,
  and False Negatives
- **Classification Report**: Per-class Precision, Recall, and F1-score

---

## Results Comparison

| Metric                   | KNN    | Logistic Regression | SVM    | Random Forest |
|--------------------------|--------|---------------------|--------|---------------|
| **Accuracy**             | ~75%   | ~77–80%             | 74.03% | 72.73%        |
| No Diabetes — Precision  | —      | —                   | 0.78   | 0.76          |
| No Diabetes — Recall     | —      | —                   | 0.84   | 0.85          |
| No Diabetes — F1-score   | —      | —                   | 0.81   | 0.80          |
| Diabetes — Precision     | —      | —                   | 0.65   | 0.64          |
| Diabetes — Recall        | —      | —                   | 0.56   | 0.50          |
| Diabetes — F1-score      | —      | —                   | 0.60   | 0.56          |
| Macro Avg F1             | —      | —                   | 0.70   | 0.68          |
| Weighted Avg F1          | —      | —                   | 0.73   | 0.72          |

> **Note**: KNN and Logistic Regression metrics marked `—` are approximate from
> notebook summaries. Update with exact values after final runs.
> **SVM & Random Forest test set**: 154 samples — 100 No Diabetes, 54 Diabetes.

---

## Model Comparison & Analysis

### 🏆 Ranking by Accuracy
1. **Logistic Regression** — ~77–80% *(best overall)*
2. **KNN** — ~75%
3. **SVM** — 74.03%
4. **Random Forest** — 72.73%

### Strengths & Weaknesses

| Model               | Strengths                                      | Weaknesses                                  |
|---------------------|------------------------------------------------|---------------------------------------------|
| KNN                 | Simple, no training phase, intuitive           | Slow at prediction, sensitive to scale      |
| Logistic Regression | Fast, interpretable, probabilistic output      | Assumes linear boundary, limited complexity |
| SVM                 | Effective in high dimensions, robust to noise  | Slower on large data, kernel tuning needed  |
| Random Forest       | Handles non-linearity, feature importance      | Prone to overfitting, less interpretable    |

### Key Observations

- **Logistic Regression achieves the highest accuracy** (~77–80%), making it the
  strongest baseline for this dataset despite its simplicity
- **SVM outperforms Random Forest** on all reported metrics (74.03% vs 72.73%)
- **Both SVM and Random Forest show low Diabetes recall** (0.56 and 0.50), meaning
  they miss a significant portion of actual diabetic cases — a critical issue in
  medical prediction
- **No Diabetes recall is consistently high** across SVM (0.84) and Random Forest
  (0.85), reflecting the class imbalance (majority class dominates predictions)
- **KNN** benefits most from `StandardScaler` since it is purely distance-based

---

## Future Work

- Address class imbalance using **SMOTE** or `class_weight='balanced'`
- Hyperparameter tuning via **GridSearchCV** / **RandomizedSearchCV**
- Apply **k-fold cross-validation** for all four models consistently
- Explore **XGBoost** or **Neural Networks** for potential accuracy gains
- Add **ROC-AUC curves** for a fuller picture of classifier performance