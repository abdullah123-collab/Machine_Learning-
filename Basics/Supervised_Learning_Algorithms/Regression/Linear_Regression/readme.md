# 📊 Linear Regression

Linear Regression is a machine learning algorithm used to predict continuous values by fitting the best straight line through data. It models the relationship between input features and a numeric target.

This repository contains **three complete implementations**:
- Two using **scikit-learn**
- One built **from scratch using NumPy**

---

## 📋 Table of Contents

- [1: Diabetes Disease Progression (Sklearn)](#1-diabetes-disease-progression-sklearn)
- [2: House Price Prediction (Sklearn)](#2-house-price-prediction-sklearn)
- [3: Linear Regression From Scratch (NumPy)](#3-linear-regression-from-scratch-numpy)

---

## 1: Diabetes Disease Progression (Sklearn)

**File:** `diabetes_regression.ipynb`

### 📌 Dataset

| Property | Value |
|----------|-------|
| Source | `sklearn.datasets.load_diabetes()` |
| Samples | 442 |
| Features | 10 (`age`, `sex`, `bmi`, `bp`, `s1`–`s6`) |
| Target | Continuous disease progression score |

### ⚙️ Workflow

- Data loading and inspection  
- Data visualization (distribution + correlations)  
- Train/test split (80/20)  
- Feature scaling using `StandardScaler`  
- Model training using `LinearRegression`  
- Evaluation using MSE, RMSE, MAE, R²  
- Residual analysis and visualization  

### 📊 Results (Approx.)

| Metric | Value |
|--------|------|
| RMSE | ~53–54 |
| MAE | ~42–44 |
| R² | ~0.50–0.55 |

---

## 2: House Price Prediction (Sklearn)

**File:** `House_Pricing_Model_.ipynb`

### 📌 Dataset

| Property | Value |
|----------|-------|
| Source | `sklearn.datasets.fetch_california_housing()` |
| Samples | 20,640 |
| Features | 8 (`MedInc`, `HouseAge`, `AveRooms`, etc.) |
| Target | Median house value (in $100,000s) |

### ⚙️ Workflow

- Data exploration and visualization  
- Feature vs target analysis  
- Train/test split (80/20)  
- Feature scaling  
- Model training using `LinearRegression`  
- Evaluation using MSE and R²  
- Overfitting check (train vs test performance)  
- Visualization of predictions  

### 📊 Results (Approx.)

| Metric | Value |
|--------|------|
| Train R² | ~0.61 |
| Test R² | ~0.60 |
| Overfitting | Minimal (good generalization) |

---

## 3: Linear Regression From Scratch (NumPy)

**File:** `linear_regression_scratch.py`

### 🧠 Overview

This implementation builds Linear Regression **completely from scratch using NumPy**, without using scikit-learn for the model.

### 🚀 Features

- Batch Gradient Descent  
- Mean Squared Error (MSE) Loss  
- Manual weight and bias updates  
- Training loss tracking  
- Visualization of training curve  
- Performance comparison with scikit-learn  
- Prediction on unseen data  

---

### 📐 Mathematical Formulation

- **Prediction:**  
  `ŷ = Xw + b`

- **Loss Function (MSE):**  
  `L = (1/n) Σ (ŷ - y)²`

- **Gradients:**  
  - `dL/dw = (2/n) Xᵀ(ŷ - y)`  
  - `dL/db = (2/n) Σ(ŷ - y)`

- **Update Rule:**  
  - `w = w - α * dL/dw`  
  - `b = b - α * dL/db`

---

### ⚙️ Workflow

- Load dataset (`load_diabetes`)  
- Train/test split (80/20)  
- Feature scaling (important for gradient descent)  
- Train custom model using gradient descent  
- Evaluate using MSE and R²  
- Compare results with scikit-learn model  
- Generate visualizations:
  - Training loss curve  
  - Actual vs predicted values  
  - Scratch vs sklearn predictions  

---

### 📊 Output

- Console logs of training progress  
- Final comparison table:
  - Scratch vs Scikit-learn performance  
- Saved plot:  
  `linear_regression_results.png`

---

### ✅ Key Insight

The scratch implementation produces results **very close to scikit-learn**, proving correctness of:
- Gradient calculations  
- Optimization process  
- Model implementation  

---

## 🛠 Requirements

```bash
pip install numpy matplotlib scikit-learn
```

---

## ▶️ How to Run

```bash
python linear_regression_scratch.py
```

---

## 📌 License

All projects are for educational purposes.  
Datasets are provided by **scikit-learn** under the BSD license.
