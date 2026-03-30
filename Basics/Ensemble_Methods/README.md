# 🌲 Ensemble Methods

> **Part of:** MACHINE_LEARNING → Basics → Ensemble_Methods

Ensemble methods combine multiple models to produce better predictions than any single model alone.

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

| Notebook | Topic |
|---|---|
| `Bagging/Random_Forest.ipynb` | Bagging + Random Forest + Feature Importance |

---

### 🔴 2. Boosting
- Models are trained **sequentially**
- Each new model **fixes the errors** of the previous one
- **Reduces: Bias**

| Notebook | Topic |
|---|---|
| `Boosting/XGBoost.ipynb` | XGBoost + Early Stopping + ROC Curve |
| `Boosting/LightGBM.ipynb` | LightGBM + Leaf-wise Growth |

---

### 🔵 3. Comparison
| Notebook | Topic |
|---|---|
| `Comparison.ipynb` | All models compared on the same dataset |

---

## ⚡ Quick Comparison

| Method | Training | Reduces | Speed | Best For |
|---|---|---|---|---|
| Bagging | Parallel | Variance | Fast | High variance models |
| Random Forest | Parallel | Variance | Fast | General purpose |
| XGBoost | Sequential | Bias | Medium | Structured / tabular data |
| LightGBM | Sequential | Bias | Very Fast | Large datasets |

---

## 🧠 Key Concepts

```
Bagging:
  └── Bootstrap samples → Train trees independently → Vote

Boosting:
  └── Tree 1 → Errors → Tree 2 (fix errors) → Errors → Tree 3 → Final Sum

Random Forest vs XGBoost:
  ├── RF:  uncorrelated trees, parallel training, reduces variance
  └── XGB: sequential trees, gradient descent, reduces bias
```

---

## 🛠️ Requirements

```bash
pip install scikit-learn xgboost lightgbm matplotlib seaborn pandas numpy
```

---

## 📚 Recommended Learning Order

```
1️⃣  Random_Forest.ipynb   → Understand the Bagging concept
2️⃣  XGBoost.ipynb         → Boosting + industry standard algorithm
3️⃣  LightGBM.ipynb        → Faster alternative to XGBoost
4️⃣  Comparison.ipynb      → Compare all models together
```

---

## 🔗 Related Topics

- [`Supervised_Learning_Algorithms/`](../Supervised_Learning_Algorithms/) — Base models (Decision Tree, Logistic Regression)
- [`Comparing_Models/`](../Comparing_Models/) — Model evaluation techniques

---

> 💡 **Tip:** Ensemble methods are the most widely used algorithms in real-world projects and Kaggle competitions. Start with Random Forest, then move to XGBoost!