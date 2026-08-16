# 🤖 Machine Learning — Python & Scikit-Learn

> A structured Machine Learning repository containing practical implementations of supervised learning, classification, regression, ensemble methods, and model comparison using Python and Scikit-Learn.

This repository documents my hands-on learning and implementation of **Machine Learning algorithms**, from fundamental supervised learning techniques to ensemble methods.

Each implementation focuses on understanding the complete workflow:

```text id="mlflow01"
Dataset
   ↓
Data Preprocessing
   ↓
Feature Engineering
   ↓
Model Training
   ↓
Prediction
   ↓
Evaluation
   ↓
Model Comparison
```

---

## 🧠 Machine Learning Topics

### Supervised Learning

#### Regression

* Linear Regression
* Model evaluation using R²
* Model comparison

#### Classification

* Logistic Regression
* Support Vector Machine (SVM)
* Naive Bayes
* K-Nearest Neighbors (KNN)
* Decision Trees

### Ensemble Learning

* Random Forest
* XGBoost
* LightGBM
* Ensemble model comparison

### Model Comparison

The repository also includes experiments comparing multiple algorithms on the same dataset to understand their relative performance.

---

## 📊 Implemented Algorithms

| Algorithm           | Type           | Dataset              | Evaluation       |
| ------------------- | -------------- | -------------------- | ---------------- |
| Linear Regression   | Regression     | Diabetes             | R²               |
| Linear Regression   | Regression     | California Housing   | R²               |
| Logistic Regression | Classification | Iris                 | Accuracy         |
| SVM (SVC)           | Classification | Titanic              | Accuracy         |
| Naive Bayes         | Classification | Email Spam           | Accuracy         |
| KNN                 | Classification | Movie Recommendation | Accuracy         |
| Decision Tree       | Classification | Iris                 | Accuracy         |
| Decision Tree       | Classification | Heart Disease        | Accuracy         |
| Random Forest       | Ensemble       | Breast Cancer        | Accuracy         |
| XGBoost             | Ensemble       | Breast Cancer        | Accuracy         |
| LightGBM            | Ensemble       | Breast Cancer        | Accuracy         |
| Ensemble Comparison | Ensemble       | Breast Cancer        | Multiple Metrics |
| Model Comparison    | Regression     | Diabetes             | Multiple Models  |

---

## 📈 Selected Results

Some completed experiments include:

| Experiment          | Dataset              |   Metric | Result |
| ------------------- | -------------------- | -------: | -----: |
| Linear Regression   | Diabetes             |       R² | 45.26% |
| Linear Regression   | California Housing   |       R² | 57.58% |
| Logistic Regression | Iris                 | Accuracy | 93.33% |
| SVM                 | Titanic              | Accuracy | 86.26% |
| Naive Bayes         | Email Spam           | Accuracy | 96.86% |
| KNN                 | Movie Recommendation | Accuracy | 62.00% |
| Decision Tree       | Iris                 | Accuracy | 98.00% |
| Decision Tree       | Heart Disease        | Accuracy | 78.80% |

> Results depend on preprocessing, feature selection, train/test split, and model configuration used in each notebook.

---

## 🗂️ Repository Structure

```text id="mlstructure"
Machine_Learning-/
│
├── Basics/
│   │
│   ├── Supervised_Learning_Algorithms/
│   │   │
│   │   ├── Regression/
│   │   │   ├── Linear_Regression/
│   │   │   │   ├── Diabetes_regression.ipynb
│   │   │   │   └── House_Pricing_Model.ipynb
│   │   │   │
│   │   │   └── Logistic_Regression/
│   │   │       └── Iris_logistic_regression.ipynb
│   │   │
│   │   └── Classification/
│   │       ├── SVM/
│   │       │   └── Titanic_svm.ipynb
│   │       │
│   │       ├── Naive_Bayes/
│   │       │   └── Spam_Email_naive_bayes.ipynb
│   │       │
│   │       ├── KNN/
│   │       │   └── Movie_Ranking_knn.ipynb
│   │       │
│   │       └── DecisionTree/
│   │           ├── Iris_decision_tree.ipynb
│   │           └── Heart_Disease_decision_tree.ipynb
│   │
│   ├── Ensemble_Methods/
│   │   ├── Bagging/
│   │   │   └── Random_Forest.ipynb
│   │   │
│   │   ├── Boosting/
│   │   │   ├── XGBoost.ipynb
│   │   │   └── LightGBM.ipynb
│   │   │
│   │   ├── Comparison.ipynb
│   │   └── README.md
│   │
│   ├── Comparing_Models/
│   │   └── Diabetes/
│   │       └── model_comparison.ipynb
│   │
│   └── Unsupervised_Learning/
│
└── Projects/
```

---

## 🔬 What I Practice in These Notebooks

The notebooks are focused on applying the standard machine learning workflow rather than only importing and training a model.

### Data Preparation

* Loading datasets
* Understanding data
* Data cleaning
* Handling missing values where required
* Feature and target selection
* Train/test splitting

### Feature Processing

* Feature scaling
* Encoding
* Feature preparation
* Basic feature engineering

### Model Training

* Selecting appropriate algorithms
* Training models
* Generating predictions
* Comparing different approaches

### Model Evaluation

Depending on the problem, evaluation includes metrics such as:

* Accuracy
* R²
* Model comparison
* Classification performance analysis

---

## 🌳 Ensemble Methods

The repository includes practical implementations of several ensemble learning techniques.

### Bagging

**Random Forest**

Random Forest combines multiple decision trees to improve predictive performance and reduce overfitting compared with a single decision tree.

### Boosting

**XGBoost**

Gradient boosting implementation widely used for structured/tabular machine learning problems.

**LightGBM**

A gradient boosting framework designed for efficient training on large datasets.

### Ensemble Comparison

The repository includes a comparison notebook for evaluating ensemble approaches on the same dataset.

---

## 🔎 Model Comparison

Model comparison is an important part of this repository.

Instead of assuming that one algorithm is always better, multiple models can be trained and evaluated on the same problem.

```text id="compare01"
Dataset
   │
   ├── Model A ──► Evaluation
   │
   ├── Model B ──► Evaluation
   │
   ├── Model C ──► Evaluation
   │
   └── Model D ──► Evaluation
                    │
                    ▼
             Compare Results
```

This helps understand how different algorithms behave on the same dataset.

---

## 📚 Learning Roadmap

### Completed

* [x] Linear Regression
* [x] Logistic Regression
* [x] SVM
* [x] Naive Bayes
* [x] KNN
* [x] Decision Trees
* [x] Random Forest
* [x] XGBoost
* [x] LightGBM
* [x] Model Comparison
* [x] Ensemble Comparison

### Next

* [ ] K-Means Clustering
* [ ] DBSCAN
* [ ] More Unsupervised Learning
* [ ] End-to-End Machine Learning Projects

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash id="mlclone"
git clone https://github.com/abdullah123-collab/Machine_Learning-.git
cd Machine_Learning-
```

### 2. Install Dependencies

```bash id="mlinstall"
pip install -r requirements.txt
```

### 3. Launch Jupyter Notebook

```bash id="mljupyter"
jupyter notebook
```

Then open any notebook from the repository.

For example:

```text id="mlexample"
Basics/
└── Supervised_Learning_Algorithms/
    └── Regression/
        └── Linear_Regression/
            └── Diabetes_regression.ipynb
```

---

## 🛠️ Tech Stack

| Technology       | Purpose                     |
| ---------------- | --------------------------- |
| Python           | Programming language        |
| NumPy            | Numerical computing         |
| Pandas           | Data manipulation           |
| Matplotlib       | Data visualization          |
| Seaborn          | Statistical visualization   |
| Scikit-Learn     | Machine Learning            |
| XGBoost          | Gradient boosting           |
| LightGBM         | Gradient boosting           |
| Jupyter Notebook | Interactive experimentation |

---

## 📦 Requirements

```text
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

## 🎯 Purpose

This repository is part of my ongoing Machine Learning learning journey.

The goal is to move from understanding individual algorithms to building complete machine learning systems involving:

```text id="mljourney"
Machine Learning Fundamentals
          ↓
Model Evaluation
          ↓
Model Comparison
          ↓
Feature Engineering
          ↓
End-to-End Projects
          ↓
Deployment
```

The repository will continue evolving as I work on more advanced machine learning concepts and practical projects.

---

## 👨‍💻 Author

**Muhammad Abdullah**

BSCS Student | Python | Data Science | Machine Learning

GitHub: [@abdullah123-collab](https://github.com/abdullah123-collab)

---

## 📄 License

This repository is intended primarily as a learning and reference project.

See the repository license for applicable terms.

---

⭐ **Building practical Machine Learning skills one algorithm and project at a time.**
