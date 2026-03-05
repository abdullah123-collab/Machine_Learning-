# 📚 Basics of Machine Learning

This section covers the fundamental concepts of Machine Learning, focusing on the difference between **Supervised** and **Unsupervised Learning** along with the models that fall under each category.

## 📊 Types of Machine Learning

```
Machine Learning
│
├── Supervised Learning        → Learns from labeled data
│   ├── Classification         → Predicts a category
│   └── Regression             → Predicts a number
│
├── Unsupervised Learning      → Learns from unlabeled data
│   ├── Clustering             → Groups similar data
│   └── Dimensionality Red.    → Reduces number of features
│
└── Reinforcement Learning     → Learns from rewards & penalties
```

---

## 🟢 Supervised Learning

> The model is trained on **labeled data** — meaning every input has a known output.

### 🔑 Key Idea
- You provide the model with input **(X)** and the correct answer **(y)**
- The model learns the mapping from X → y
- Then predicts y for new, unseen X

### 📌 Types & Models

#### 🔷 Classification — Predicts a **category/class**

| Model | Description |
|---|---|
| **Logistic Regression** | Predicts probability of a class (e.g., spam or not) |
| **Support Vector Machine (SVM)** | Finds best boundary between classes |
| **K-Nearest Neighbors (KNN)** | Classifies based on nearest data points |
| **Decision Tree** | Uses a tree of if/else rules |
| **Random Forest** | Combines many decision trees |
| **Naive Bayes** | Based on probability theory |
| **Neural Networks** | Mimics the human brain |

#### 🔷 Regression — Predicts a **continuous number**

| Model | Description |
|---|---|
| **Linear Regression** | Predicts a value using a straight line |
| **Polynomial Regression** | Predicts using a curved line |
| **Ridge / Lasso Regression** | Linear regression with regularization |
| **SVR** | Support Vector Machine for regression |
| **Decision Tree Regressor** | Tree-based regression |

### ✅ Examples
- Predicting house prices → **Regression**
- Detecting spam emails → **Classification**
- Predicting Titanic survival → **Classification**

---

## 🔴 Unsupervised Learning

> The model is trained on **unlabeled data** — meaning there are no correct answers given.

### 🔑 Key Idea
- You provide only input **(X)**, no labels
- The model finds **hidden patterns** or **groups** on its own
- No "right or wrong" answer — just structure in data

---

## ⚖️ Supervised vs Unsupervised — Key Differences

| Feature | Supervised | Unsupervised |
|---|---|---|
| **Data** | Labeled (X + y) | Unlabeled (X only) |
| **Goal** | Predict output | Find hidden patterns |
| **Feedback** | Yes (correct answers given) | No (no right/wrong) |
| **Complexity** | Easier to evaluate | Harder to evaluate |
| **Examples** | Classification, Regression | Clustering, Dimensionality Reduction |
| **Use Case** | Spam detection, Price prediction | Customer segmentation, Anomaly detection |

---
