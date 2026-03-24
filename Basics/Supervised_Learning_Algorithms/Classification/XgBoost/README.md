# 🌲 XGBoost Classification — Breast Cancer Dataset

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)
![XGBoost](https://img.shields.io/badge/XGBoost-1.7%2B-orange)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.0%2B-yellowgreen?logo=scikit-learn)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![License](https://img.shields.io/badge/License-MIT-green)

A complete, step-by-step implementation of **XGBoost for Binary Classification** using the classic **Breast Cancer Wisconsin dataset** from scikit-learn. Designed for GitHub with clean commit-by-commit progression.

---

## 📁 Repository Structure

```
xgboost-classification/
│
├── XGBoost_Classification.ipynb   # Main Jupyter Notebook
├── xgboost_breast_cancer.json     # Saved model (generated after running)
└── README.md                      # This file
```

---

## 📌 Dataset Overview

| Property     | Details                                      |
|--------------|----------------------------------------------|
| **Name**     | Breast Cancer Wisconsin (Diagnostic)         |
| **Source**   | `sklearn.datasets.load_breast_cancer()`      |
| **Samples**  | 569                                          |
| **Features** | 30 (tumor measurements)                      |
| **Classes**  | 2 — `Malignant (0)` / `Benign (1)`           |
| **Task**     | Binary Classification                        |

---

## 🗂️ Notebook Parts & Git Commits

The notebook is structured into **8 parts**, each mapped to a GitHub commit:

| Part | Description | Commit Message |
|------|-------------|----------------|
| **1** | Imports & Environment Setup | `feat: add imports and environment setup` |
| **2** | Load & Explore Dataset | `feat: load and explore breast cancer dataset` |
| **3** | Data Preprocessing & Train-Test Split | `feat: preprocess data and create train-test split` |
| **4** | Build & Train XGBoost Model | `feat: build and train XGBoost classifier` |
| **5** | Model Evaluation (Accuracy, AUC, ROC) | `feat: evaluate model with metrics and confusion matrix` |
| **6** | Feature Importance Plot | `feat: plot feature importance` |
| **7** | Save & Load Model | `feat: save and reload trained model` |
| **8** | Scikit-learn API (Bonus) | `feat: add sklearn-compatible XGBoost API example` |

---

## 🚀 How to Push Part by Part to GitHub

### Initial Setup
```bash
git init
git remote add origin https://github.com/your-username/xgboost-classification.git
```

### Push Each Part Separately

```bash
# ── Commit 1 ──
git add README.md
git commit -m "docs: add README"
git push -u origin main

# ── Commit 2 ──
# After completing Part 1 & 2 in notebook (save notebook)
git add XGBoost_Classification.ipynb
git commit -m "feat: add imports and environment setup"
git push

# ── Commit 3 ──
git add XGBoost_Classification.ipynb
git commit -m "feat: load and explore breast cancer dataset"
git push

# ── Commit 4 ──
git add XGBoost_Classification.ipynb
git commit -m "feat: preprocess data and create train-test split"
git push

# ── Commit 5 ──
git add XGBoost_Classification.ipynb
git commit -m "feat: build and train XGBoost classifier"
git push

# ── Commit 6 ──
git add XGBoost_Classification.ipynb
git commit -m "feat: evaluate model with metrics and confusion matrix"
git push

# ── Commit 7 ──
git add XGBoost_Classification.ipynb
git commit -m "feat: plot feature importance"
git push

# ── Commit 8 ──
git add XGBoost_Classification.ipynb xgboost_breast_cancer.json
git commit -m "feat: save and reload trained model"
git push

# ── Commit 9 ──
git add XGBoost_Classification.ipynb
git commit -m "feat: add sklearn-compatible XGBoost API example"
git push
```

---

## ⚙️ Installation

```bash
# Clone the repo
git clone https://github.com/your-username/xgboost-classification.git
cd xgboost-classification

# Install dependencies
pip install xgboost scikit-learn pandas numpy matplotlib seaborn notebook
```

---

## ▶️ Run the Notebook

```bash
jupyter notebook XGBoost_Classification.ipynb
```

---

## 📊 Results

| Metric       | Score     |
|--------------|-----------|
| **Accuracy** | ~97–98%   |
| **ROC-AUC**  | ~0.995    |

---

## 🔑 Key XGBoost Parameters Used

| Parameter          | Value | Purpose                          |
|--------------------|-------|----------------------------------|
| `objective`        | `binary:logistic` | Binary classification   |
| `max_depth`        | 4     | Controls tree complexity         |
| `learning_rate`    | 0.1   | Step size per boosting round     |
| `subsample`        | 0.8   | Row sampling — prevents overfit  |
| `colsample_bytree` | 0.8   | Feature sampling per tree        |
| `reg_alpha`        | 0.1   | L1 regularisation                |
| `reg_lambda`       | 1.0   | L2 regularisation                |
| `early_stopping`   | 15    | Stop if no improvement           |

---

## 📦 Dependencies

```
xgboost>=1.7.0
scikit-learn>=1.0.0
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
notebook>=6.0.0
```

---

## 📄 License

This project is licensed under the **MIT License** — free to use and modify.

---

