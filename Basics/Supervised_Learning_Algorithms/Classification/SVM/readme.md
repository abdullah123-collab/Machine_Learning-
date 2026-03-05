# Support Vector Machine (SVM) — Titanic Survival Prediction

A classification model using Support Vector Machine (SVC) to predict passenger survival on the Titanic dataset.

---

## Dataset

| Property | Details |
|---|---|
| **Dataset** | Titanic (`train_and_test2.csv`) |
| **Rows** | 1,309 passengers |
| **Target** | `Survived` (0 = Did not survive, 1 = Survived) |
| **Features Used** | Age, Fare, Sex, Sibsp, Parch, Pclass, Embarked |

---

## Results

| Metric | Score |
|---|---|
| **Training Accuracy** | 87.58% |
| **Test Accuracy** | 86.26% |

### Classification Report

| Class | Precision | Recall | F1-Score | Support |
|---|---|---|---|---|
| 0 (Not Survived) | 0.87 | 0.95 | 0.91 | 194 |
| 1 (Survived) | 0.82 | 0.60 | 0.69 | 68 |
| **Weighted Avg** | **0.86** | **0.86** | **0.86** | **262** |

### Confusion Matrix (%)

| | Predicted: 0 | Predicted: 1 |
|---|---|---|
| **Actual: 0** | 95.36% | 4.64% |
| **Actual: 1** | 39.71% | 60.29% |

---

## Project Workflow

1. **Data Loading** — Load Titanic dataset from CSV
2. **Data Preprocessing**
   - Drop irrelevant columns (Name, Ticket, Cabin)
   - Fill missing Age with median
   - Fill missing Embarked with mode
   - Encode categorical features (Sex, Embarked) using LabelEncoder
3. **Train/Test Split** — 80% train / 20% test (stratified)
4. **Feature Scaling** — StandardScaler (fit on train, transform both)
5. **Model Training** — SVC with RBF kernel
6. **Evaluation** — Accuracy, Classification Report, Confusion Matrix

---

## Model Details

| Parameter | Value |
|---|---|
| **Algorithm** | Support Vector Classifier (SVC) |
| **Kernel** | RBF (Radial Basis Function) |
| **C** | 1.0 |
| **Gamma** | scale |
| **Probability** | True |

---

##  How to Run

### 1. Install dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### 2. Place dataset
Make sure `train_and_test2.csv` is in the same folder as the notebook.

### 3. Run the notebook
```bash
jupyter notebook svc.ipynb
```

---

## Tech Stack

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3-orange?logo=scikit-learn)
![Pandas](https://img.shields.io/badge/Pandas-2.0-green?logo=pandas)
![Seaborn](https://img.shields.io/badge/Seaborn-0.12-lightblue)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)

---

##  Files

| File | Description |
|---|---|
| `svc.ipynb` | Main Jupyter notebook with full implementation |
| `train_and_test2.csv` | Titanic dataset |
| `README.md` | Project documentation |