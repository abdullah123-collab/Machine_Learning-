# 📧 Email Spam Detection — Naive Bayes

A clean Machine Learning project to classify emails as **Spam** or **Ham (Not Spam)** using **Complement Naive Bayes** with **TF-IDF** vectorization.

---

## 📊 Results

| Metric | Value |
|--------|-------|
| ✅ Accuracy | **96.86%** |
| 📈 ROC-AUC Score | **0.9912** |
| 🔁 5-Fold CV Accuracy | **97.27% ± 0.46%** |

### Classification Report

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| Ham | 0.99 | 0.97 | 0.98 | 966 |
| Spam | 0.83 | 0.96 | 0.89 | 149 |
| **Weighted Avg** | **0.97** | **0.97** | **0.97** | **1115** |

---

## 📁 Project Structure

```
Naive_Bayes_Email_Spam/
│
├── email.csv                  ← Dataset (place in same folder)
├── spam_detection.ipynb       ← Jupyter Notebook (step-by-step)
├── spam_model.pkl             ← Saved trained model (auto-generated)
└── README.md
```

---

## ⚙️ Setup & Installation

```bash
# 1. Clone the repository
git clone https://github.com/your-username/Naive_Bayes_Email_Spam.git
cd Naive_Bayes_Email_Spam

# 2. Install dependencies
pip install -r requirements.txt
```

> Place `email.csv` in the **same folder** as the script/notebook.

---


## 🧠 Model Details

| Component | Detail |
|-----------|--------|
| Algorithm | Complement Naive Bayes (`ComplementNB`) |
| Vectorizer | TF-IDF (max 5000 features, unigrams + bigrams) |
| Train / Test Split | 80% / 20% (stratified) |
| Cross-Validation | 5-Fold CV |
| Stop Words | English |
| Laplace Smoothing (alpha) | 0.1 |

> **Why Complement NB?**
> It outperforms standard Multinomial NB on **imbalanced datasets** — common in spam detection where ham emails outnumber spam (966 Ham vs 149 Spam).

---

## 🔍 Sample Predictions

```
Email  : Congratulations! You won a FREE iPhone. Click here to claim!!!
Result : 🚨 SPAM  |  Spam: 98.3%  Ham: 1.7%

Email  : Can we reschedule our meeting to 3pm tomorrow?
Result : ✅ Ham   |  Spam: 2.1%   Ham: 97.9%

Email  : URGENT: Your bank account is suspended. Verify immediately.
Result : 🚨 SPAM  |  Spam: 96.7%  Ham: 3.3%

Email  : Please review the attached report before the standup.
Result : ✅ Ham   |  Spam: 1.4%   Ham: 98.6%
```

---
