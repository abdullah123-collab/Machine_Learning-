# 📊 Ensemble Methods — Full Comparison

> **Part of:** MACHINE_LEARNING → Basics → Ensemble_Methods

This section covers ensemble learning techniques — methods that combine multiple models to produce better predictions than any single model alone.

---

## 📁 Folder Structure

```
Ensemble_Methods/
├── Bagging/
│   └── Random_Forest.ipynb
├── Boosting/
│   ├── XGBoost.ipynb
│   └── LightGBM.ipynb
├── Comparison.ipynb
└── README.md
```

---

## 📌 Techniques Covered

### 🟢 1. Bagging (Bootstrap Aggregating)
- Models are trained **in parallel**
- Each model trains on a different **random subset** of data
- Final prediction = **majority vote** (classification) or **average** (regression)
- **Reduces: Variance**

| Notebook | Algorithm | Dataset | Accuracy |
|---|---|---|---|
| `Bagging/Random_Forest.ipynb` | Random Forest | Breast Cancer | — |

---

### 🔴 2. Boosting
- Models are trained **sequentially**
- Each new model **fixes the errors** of the previous one
- **Reduces: Bias**

| Notebook | Algorithm | Dataset | Accuracy |
|---|---|---|---|
| `Boosting/XGBoost.ipynb` | XGBoost | Breast Cancer | — |
| `Boosting/LightGBM.ipynb` | LightGBM | Breast Cancer | — |

---

### 🔵 3. Comparison

| Notebook | What it Covers |
|---|---|
| `Comparison.ipynb` | Accuracy, Precision, Recall, F1, AUC-ROC, Speed — all models side by side |

---

## ⚡ Quick Comparison

| Model | Type | Training | Reduces | Speed | Best For |
|---|---|---|---|---|---|
| Decision Tree | Baseline | Single | — | Fast | Interpretability |
| Random Forest | Bagging | Parallel | Variance | Fast | General purpose |
| XGBoost | Boosting | Sequential | Bias | Medium | Structured data |
| LightGBM | Boosting | Sequential | Bias | **Very Fast** | Large datasets |

---

## 🧠 Key Concepts

```
Bagging:
  └── Bootstrap samples → Train trees independently → Vote

Boosting:
  └── Tree 1 → Errors
             → Tree 2 (fix errors) → Errors
                                   → Tree 3 → Final Sum

XGBoost  → Level-wise tree growth
LightGBM → Leaf-wise tree growth (faster, more accurate)
```

---

## 🏆 Results Summary

| Criteria | Winner |
|---|---|
| Best Accuracy | XGBoost / LightGBM |
| Best AUC-ROC | XGBoost / LightGBM |
| Fastest Training | LightGBM |
| Most Interpretable | Decision Tree |
| Best Overall | LightGBM |

---

## 📚 Recommended Learning Order

```
1️⃣  Bagging/Random_Forest.ipynb   → Understand Bagging & feature importance
2️⃣  Boosting/XGBoost.ipynb        → Boosting + industry standard
3️⃣  Boosting/LightGBM.ipynb       → Faster alternative + speed comparison
4️⃣  Comparison.ipynb              → All models compared side by side
```

---

## 🛠️ Requirements

```bash
pip install scikit-learn xgboost lightgbm matplotlib seaborn pandas numpy
```

---

## 🔗 Related Topics

- [`Supervised_Learning_Algorithms/`](../Supervised_Learning_Algorithms/) — Base models (Decision Tree, SVM, KNN)
- [`Comparing_Models/`](../Comparing_Models/) — Model evaluation on Diabetes dataset

---

> 💡 **Tip:** Always compare models on the **same dataset** with the **same train/test split** for a fair evaluation. Ensemble methods consistently outperform single models on structured/tabular data.