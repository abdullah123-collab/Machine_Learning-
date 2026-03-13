# Diabetes Prediction Analysis

This repository contains two Jupyter notebooks that explore different machine learning models to predict diabetes based on various health metrics.

## Dataset Overview
Both analyses use the **Pima Indians Diabetes** dataset, which consists of 768 samples and 9 columns.

* **Total Samples**: 768
* **Target Variable**: `Outcome` (0 for healthy, 1 for diabetes)
* **Features**:
    * Pregnancies
    * Glucose
    * Blood Pressure
    * Skin Thickness
    * Insulin
    * BMI
    * Diabetes Pedigree Function
    * Age

## Models Implemented

### 1. K-Nearest Neighbors (KNN)
The `KNN.ipynb` notebook implements a K-Nearest Neighbors classifier.
* **Key Libraries**: `scikit-learn`, `pandas`, `numpy`, `seaborn`, and `matplotlib`.
* **Preprocessing**: Includes `StandardScaler` to normalize feature scales, which is critical for distance-based algorithms like KNN.
* **Evaluation**: Uses cross-validation scores and accuracy metrics to determine the best value for 'K'.

### 2. Logistic Regression
The `Logistic_Regression.ipynb` notebook implements a Logistic Regression model for binary classification.
* **Key Libraries**: `sklearn.linear_model.LogisticRegression`, `pandas`, and `numpy`.
* **Analysis**: Includes a final model summary comparing training and testing sizes, as well as detailed recall metrics for both classes.

## Performance Metrics
Both notebooks evaluate performance using:
* **Accuracy Score**: The overall percentage of correct predictions.
* **Confusion Matrix**: Provides counts for True Positives, True Negatives, False Positives, and False Negatives.
* **Classification Report**: Includes Precision, Recall, and F1-score for both healthy and diabetic outcomes.

## Comparison
Based on the final summaries provided in the notebooks:
* **Logistic Regression Accuracy**: Approximately 77–80%.
* **KNN Accuracy**: Performance is compared directly against the Logistic Regression baseline within the KNN notebook to see which yields better predictive power.