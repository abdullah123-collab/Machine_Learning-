# 📊 Linear Regression Projects

Two end-to-end regression projects built with scikit-learn, covering disease progression prediction and house price estimation.

---

## 📋 Table of Contents

- [1: Diabetes Disease Progression](#project-1-diabetes-disease-progression)
- [2: House Price Prediction](#project-2-house-price-prediction)

---

## 1: Diabetes Disease Progression

**File:** `diabetes_regression.ipynb`

### Dataset

| Property | Value |
|----------|-------|
| Source | `sklearn.datasets.load_diabetes()` |
| Samples | 442 |
| Features | 10 (`age`, `sex`, `bmi`, `bp`, `s1`–`s6`) |
| Target | Continuous disease progression score |

### Notebook Walkthrough

| Cell | Description |
|------|-------------|
| 1–2 | Import libraries and scikit-learn modules |
| 3–5 | Load dataset, summary statistics, missing value check |
| 6–8 | Target distribution, correlation heatmap, feature scatter plots |
| 9–10 | Train/test split (80/20) and StandardScaler |
| 11 | Train LinearRegression, display coefficients |
| 12–13 | Predictions and evaluation metrics (MSE, RMSE, MAE, R²) |
| 14–15 | Actual vs Predicted plot and residual analysis |
| 16–17 | Feature importance chart and single-sample prediction |

### Results

| Metric | Value (approx.) |
|--------|-----------------|
| RMSE | ~53–54 |
| MAE | ~42–44 |
| R² | ~0.50–0.55 |

---

## 2: House Price Prediction

**File:** `House_Pricing_Model_.ipynb`

### Dataset

| Property | Value |
|----------|-------|
| Source | `sklearn.datasets.fetch_california_housing()` |
| Samples | 20,640 |
| Features | 8 (`MedInc`, `HouseAge`, `AveRooms`, etc.) |
| Target | Median house value (in $100,000s) |

### Notebook Walkthrough

| Cell | Description |
|------|-------------|
| 1–2 | Import libraries, load dataset into DataFrame |
| 3–4 | Summary statistics, Median Income vs Price scatter plot |
| 5–6 | Train/test split (80/20) and StandardScaler |
| 7–8 | Train LinearRegression, display feature coefficients |
| 9–10 | Predictions on train and test sets, MSE and R² scores |
| 11 | Overfitting check (train MSE vs test MSE) |
| 12–13 | Actual vs Predicted plot and residual plot |
| 14–15 | Best fit line on MedInc feature, final Actual vs Predicted with reference line |

### Results

| Metric | Value (approx.) |
|--------|-----------------|
| Train R² | ~0.61 |
| Test R² | ~0.60 |
| Overfitting | Minimal — model generalizes well |

---

## License

Both projects are for educational purposes. Datasets are part of scikit-learn and available under the BSD license.