# 🌲 Ensemble Methods

> **Part of:** MACHINE_LEARNING → Basics → Ensemble_Methods

Ensemble methods multiple models ko combine karke better predictions dete hain kisi bhi single model se.

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
- Models **parallel** train hote hain
- Har model alag random subset pe train hota hai
- Final prediction = **majority vote** (classification) ya **average** (regression)
- **Reduces: Variance**

| Notebook | Topic |
|---|---|
| `Bagging/Random_Forest.ipynb` | Bagging + Random Forest + Feature Importance |

---

### 🔴 2. Boosting
- Models **sequentially** train hote hain
- Har model pichle ki **galtiyan fix** karta hai
- **Reduces: Bias**

| Notebook | Topic |
|---|---|
| `Boosting/XGBoost.ipynb` | XGBoost + Early Stopping + ROC Curve |
| `Boosting/LightGBM.ipynb` | LightGBM + Leaf-wise Growth |

---

### 🔵 3. Comparison
| Notebook | Topic |
|---|---|
| `Comparison.ipynb` | All models ek dataset pe compare |

---

## ⚡ Quick Comparison

| Method | Training | Reduces | Speed | Best For |
|---|---|---|---|---|
| Bagging | Parallel | Variance | Fast | High variance models |
| Random Forest | Parallel | Variance | Fast | General purpose |
| XGBoost | Sequential | Bias | Medium | Structured/tabular data |
| LightGBM | Sequential | Bias | Very Fast | Large datasets |

---

## 🧠 Key Concepts

```
Bagging:
  └── Bootstrap samples → Train trees independently → Vote

Boosting:
  └── Tree 1 → Errors → Tree 2 (fix errors) → Errors → Tree 3 → Final Sum

Random Forest vs XGBoost:
  ├── RF: uncorrelated trees, parallel, reduces variance
  └── XGB: sequential trees, gradient descent, reduces bias
```

---

## 🛠️ Requirements

```bash
pip install scikit-learn xgboost lightgbm matplotlib seaborn pandas numpy
```

---

## 📚 Learning Order

```
1️⃣  Random_Forest.ipynb   → Bagging concept samjho
2️⃣  XGBoost.ipynb         → Boosting + industry standard
3️⃣  LightGBM.ipynb        → Faster alternative
4️⃣  Comparison.ipynb      → Sab ek saath compare karo
```

---

## 🔗 Related Topics

- [`Supervised_Learning_Algorithms/`](../Supervised_Learning_Algorithms/) — Base models
- [`Comparing_Models/`](../Comparing_Models/) — Model evaluation techniques

---

> 💡 **Tip:** Ensemble methods real-world aur Kaggle competitions mein sabse zyada use hote hain. Random Forest se shuru karo, phir XGBoost try karo!