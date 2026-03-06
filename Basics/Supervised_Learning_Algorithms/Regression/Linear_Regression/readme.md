# 🩺 Diabetes Disease Progression — Linear Regression

A end-to-end machine learning project that applies **Linear Regression** to scikit-learn's built-in diabetes dataset to predict disease progression one year after baseline measurements.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Notebook Walkthrough](#notebook-walkthrough)
- [Results](#results)

---

## Overview

This project demonstrates a complete supervised regression pipeline:

1. Load and explore the data
2. Visualize feature distributions and correlations
3. Preprocess with `StandardScaler`
4. Train a `LinearRegression` model
5. Evaluate with MSE, RMSE, MAE, and R²
6. Analyze residuals and feature coefficients

---

## Dataset

**Source:** `sklearn.datasets.load_diabetes()`

| Property | Value |
|----------|-------|
| Samples | 442 |
| Features | 10 |
| Target | Continuous (disease progression score) |
| Missing values | None |

**Features:** `age`, `sex`, `bmi`, `bp`, `s1`, `s2`, `s3`, `s4`, `s5`, `s6`  
(All features are already normalized in the original dataset.)

---

## Notebook Walkthrough

| Cell | Description |
|------|-------------|
| 1 | Import core libraries (numpy, pandas, matplotlib, seaborn) |
| 2 | Import scikit-learn modules (dataset, model, metrics, scaler) |
| 3 | Load diabetes dataset, build DataFrame, preview shape and head |
| 4 | Print dataset description and summary statistics |
| 5 | Check for missing values and data types |
| 6 | Plot target variable distribution (histogram + KDE) |
| 7 | Correlation heatmap across all features |
| 8 | Scatter plots: each feature vs target (2×5 grid) |
| 9 | Train/test split — 80% train / 20% test (`random_state=42`) |
| 10 | Feature scaling with `StandardScaler` (fit on train, transform test) |
| 11 | Train `LinearRegression` model, display intercept and coefficients |
| 12 | Generate predictions, preview Actual vs Predicted vs Residual |
| 13 | Compute evaluation metrics: MSE, RMSE, MAE, R² |
| 14 | Scatter plot: Actual vs Predicted values |
| 15 | Residual analysis: Residuals vs Predicted + Residuals Distribution |
| 16 | Feature importance bar chart (green = positive, red = negative) |
| 17 | Single-sample prediction demo from the test set |

---

## Results

Typical results on a 80/20 split with `random_state=42`:

| Metric | Value (approx.) |
|--------|-----------------|
| MSE | ~2900 |
| RMSE | ~53–54 |
| MAE | ~42–44 |
| R² | ~0.50–0.55 |

An R² of ~0.52 means the model explains roughly **52% of the variance** in disease progression — reasonable for a simple linear model on this dataset.

---

## License

This project is for educational purposes. The diabetes dataset is part of scikit-learn and is publicly available under the BSD license.