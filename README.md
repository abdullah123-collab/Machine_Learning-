# Machine Learning

A structured repository covering Machine Learning algorithms implemented using Python and scikit-learn — organized by category for easy navigation and learning.

ii
---

## 📁 Repository Structure

```
Machine_Learning/
│
├── Basics/
│   ├── Supervised_Learning_Algorithms/
│   │   ├── Regression/
│   │   │   ├── Linear_Regression/
│   │   │   │   ├── Diabetes_regression.ipynb
│   │   │   │   └── House_Pricing_Model.ipynb
│   │   │   └── Logistic_Regression/
│   │   │       └── Iris_logistic_regression.ipynb
│   │   └── Classification/
│   │       ├── SVM/
│   │       │   └── Titanic_svm.ipynb
│   │       ├── Naive_Bayes/
│   │       │   └── Spam_Email_naive_bayes.ipynb
│   │       ├── KNN/
│   │       │   └── Movie_Ranking_knn.ipynb
│   │       └── DecisionTree/
│   │           ├── Iris_decision_tree.ipynb
│   │           └── Heart_Disease_decision_tree.ipynb
│   │
<<<<<<< HEAD
│   ├── Ensemble_Methods/                         
=======
│   ├── Ensemble_Methods/
>>>>>>> 1341a2db899c67641292529f7c576a8b0845c1b6
│   │   ├── Bagging/
│   │   │   └── Random_Forest.ipynb
│   │   ├── Boosting/
│   │   │   ├── XGBoost.ipynb
│   │   │   └── LightGBM.ipynb
│   │   ├── Comparison.ipynb
│   │   └── README.md
│   │
│   ├── Unsupervised_Learning/                     # 🔜 Coming Soon
│   │   ├── KMeans/
│   │   │   └── KMeans_clustering.ipynb
│   │   └── DBSCAN/
│   │       └── DBSCAN_clustering.ipynb
│   │
│   └── Comparing_Models/
│       └── Diabetes/
│           └── model_comparison.ipynb
│
└── Projects/                                      
```

---

## ✅ Completed

| Algorithm | Category | Dataset | Metric | Score | Status |
|---|---|---|---|---|---|
| Linear Regression | Supervised / Regression | Diabetes | R² | 45.26% | ✅ Done |
| Linear Regression | Supervised / Regression | California Housing | R² | 57.58% | ✅ Done |
| Logistic Regression | Supervised / Classification | Iris | Accuracy | 93.33% | ✅ Done |
| SVM (SVC) | Supervised / Classification | Titanic | Accuracy | 86.26% | ✅ Done |
| Naive Bayes | Supervised / Classification | Email Spam | Accuracy | 96.86% | ✅ Done |
| KNN | Supervised / Classification | Movie Recommendation | Accuracy | 62.00% | ✅ Done |
| Decision Tree | Supervised / Classification | Iris | Accuracy | 98.00% | ✅ Done |
| Decision Tree | Supervised / Classification | Heart Disease | Accuracy | 78.80% | ✅ Done |
| Model Comparison | Supervised | Diabetes | R² | Multiple | ✅ Done |
| Random Forest | Supervised / Ensemble | Breast Cancer | Accuracy | — | ✅ Done |
| XGBoost | Supervised / Ensemble | Breast Cancer | Accuracy | — | ✅ Done |
| LightGBM | Supervised / Ensemble | Breast Cancer | Accuracy | — | ✅ Done |
| Ensemble Comparison | Supervised / Ensemble | Breast Cancer | Multiple | — | ✅ Done |

---

## 🔜 Coming Soon

| Topic | Category | Status |
|---|---|---|
| K-Means Clustering | Unsupervised | 🔜 Planned |
| DBSCAN | Unsupervised | 🔜 Planned |
| End-to-end Project #1 | Projects | 🔜 Planned |

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/abdullah123-collab/Machine_Learning-.git
cd Machine_Learning-
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run any notebook

```bash
# Example: Linear Regression on Diabetes dataset
cd Basics/Supervised_Learning_Algorithms/Regression/Linear_Regression
jupyter notebook Diabetes_regression.ipynb

# Example: Random Forest
cd Basics/Ensemble_Methods/Bagging
jupyter notebook Random_Forest.ipynb

# Example: XGBoost
cd Basics/Ensemble_Methods/Boosting
jupyter notebook XGBoost.ipynb

# Example: LightGBM
cd Basics/Ensemble_Methods/Boosting
jupyter notebook LightGBM.ipynb

# Example: Ensemble Comparison
cd Basics/Ensemble_Methods
jupyter notebook Comparison.ipynb
```

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3-orange?logo=scikit-learn)
![Pandas](https://img.shields.io/badge/Pandas-2.0-green?logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-1.24-lightblue?logo=numpy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.7-red)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![XGBoost](https://img.shields.io/badge/XGBoost-1.7-blue)
![LightGBM](https://img.shields.io/badge/LightGBM-4.0-brightgreen)

---

## 📦 Requirements

```
numpy>=1.24.0
pandas>=2.0.0
matplotlib>=3.7.0
seaborn>=0.12.0
scikit-learn>=1.3.0
jupyter>=1.0.0
xgboost>=1.7.0
lightgbm>=4.0.0
```

---

## 📌 Notes

- **Logistic Regression** is a *classification* algorithm despite the name — it predicts discrete class labels, not continuous values. It is placed under `Regression/` folder only for naming convention reasons.
- The `Comparing_Models/` folder benchmarks multiple algorithms on the same dataset side by side.
- The `Ensemble_Methods/` folder covers Bagging and Boosting techniques including Random Forest, XGBoost, and LightGBM.
- All notebooks include data preprocessing, model training, evaluation metrics, and visualizations.

---

## 👤 Author

**Muhammad Abdullah**

- GitHub: [@abdullah123-collab](https://github.com/abdullah123-collab)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
