# Machine Learning: Regression and Classification

This repository contains implementations and examples of algorithms used for regression and classification problems using Python and the **scikit-learn** library.

---

# Regression

## What is Regression?
Regression is a supervised learning technique used to predict **continuous numerical values**.  
It models the relationship between input features and a continuous target variable.

### Example
Predicting the **price of a house** based on:
- Size of the house
- Number of rooms
- Location

Output: Numeric value (e.g., 250000)

### Common Regression Algorithms
- Linear Regression
- Polynomial Regression
- Ridge Regression
- Lasso Regression
- Elastic Net
- Decision Tree Regressor
- Random Forest Regressor
- Support Vector Regression (SVR)
- Gradient Boosting Regressor

---

# Classification

## What is Classification?
Classification is a supervised learning technique used to predict **categorical labels or classes**.  
The model learns from labeled data and predicts which category new data belongs to.

### Example
Email spam detection:
- Spam
- Not Spam

Another example is **Iris flower classification**:
- Setosa
- Versicolor
- Virginica

### Common Classification Algorithms
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree Classifier
- Random Forest Classifier
- Support Vector Machine (SVM)
- Naive Bayes
- Gradient Boosting
- AdaBoost
- Neural Networks

---

# Difference Between Regression and Classification

| Feature | Regression | Classification |
|--------|------------|---------------|
| Output | Continuous numerical value | Discrete class label |
| Example | House price prediction | Spam detection |
| Goal | Predict numeric values | Predict categories |
| Evaluation Metrics | MSE, RMSE, R² | Accuracy, Precision, Recall, F1-score |

---

# Tools and Libraries
The following tools and libraries are used in this project:

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn


# Conclusion
Regression and Classification are fundamental techniques in machine learning. Regression is used when the output is a **continuous number**, while classification is used when the output is a **category or class label**.

Understanding these concepts helps in selecting the right algorithm for solving real-world machine learning problems.
