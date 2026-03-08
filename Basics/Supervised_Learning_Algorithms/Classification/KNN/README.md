# 🎬 KNN Movie Rating Classifier

> Predict whether a movie is **High Rated** or **Low Rated** using K-Nearest Neighbors

![Python](https://img.shields.io/badge/Python-3.8+-blue) ![scikit-learn](https://img.shields.io/badge/scikit--learn-latest-orange) ![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange) ![Dataset](https://img.shields.io/badge/Dataset-TMDB-green)

---

## 📌 Project Overview

This project uses the **K-Nearest Neighbors (KNN)** algorithm to classify movies as:
- ⭐ **High Rated** → `vote_average >= 6.0`
- 👎 **Low Rated** → `vote_average < 6.0`

Key techniques used:
- **SMOTE** to fix class imbalance
- **Distance-weighted KNN** for better minority class prediction
- **Cross-validation** to auto-tune the best K

---

## 📁 Project Structure

```
knn-movie-rating/
│
├── knn_movie_rating.ipynb     ← Main Jupyter notebook
├── your_movies.csv            ← Dataset (add your own)
├── k_vs_accuracy.png          ← Generated: K tuning plot
├── confusion_matrix.png       ← Generated: confusion matrix
└── README.md                  ← This file
```

---

## 📊 Dataset

**Source:** TMDB (The Movie Database) — movies metadata CSV

| Column | Type | Usage |
|--------|------|-------|
| `vote_average` | Float | Target variable → converted to High/Low |
| `budget` | Integer | Feature |
| `popularity` | Float | Feature |
| `runtime` | Integer | Feature |
| `revenue` | Integer | Feature |
| `vote_count` | Integer | Feature |
| `genres` | JSON string | Feature → encoded as genre dummies |
| `belongs_to_collection` | String/NaN | Feature → 1 if part of series, else 0 |

---

## ⚙️ Requirements

```bash
pip install pandas numpy scikit-learn imbalanced-learn matplotlib seaborn
```

| Library | Purpose |
|---------|---------|
| `pandas` | Data loading & manipulation |
| `numpy` | Numerical operations |
| `scikit-learn` | KNN, scaling, evaluation |
| `imbalanced-learn` | SMOTE oversampling |
| `matplotlib` & `seaborn` | Visualizations |

---

## 🚀 How to Run

1. Place your CSV file in the same folder as the notebook
2. Open `knn_movie_rating.ipynb` in Jupyter
3. Update the filename in **Cell 3**:
   ```python
   df = pd.read_csv("your_movies.csv")  # ← change this
   ```
4. Run all cells top to bottom (**Cell 1 → Cell 13**)

---

## 📓 Notebook Structure

| Cell | Title | Description |
|------|-------|-------------|
| 1 | Install Dependencies | Installs all required libraries |
| 2 | Imports | Loads all Python libraries |
| 3 | Load Data | Reads CSV, shows shape and preview |
| 4 | Create Target | Converts `vote_average` → High/Low + bar chart |
| 5 | Feature Engineering | Encodes genres, creates `in_collection` flag |
| 6 | Train/Test Split | 80/20 stratified split |
| 7 | Scale Features | StandardScaler — critical for KNN |
| 8 | SMOTE | Fixes class imbalance by oversampling minority |
| 9 | Find Best K | Cross-validation K=1 to 20 + elbow plot |
| 10 | Train Model | Fits KNN with best K and `weights='distance'` |
| 11 | Evaluate | Accuracy, precision, recall, F1 report |
| 12 | Confusion Matrix | Heatmap of actual vs predicted |
| 13 | Predict New Movie | Input custom values to get a prediction |

---

## 🧠 Model Details

### Algorithm: K-Nearest Neighbors (KNN)

```
New movie → find K most similar movies in training data → majority vote → High or Low
```

### Parameters

| Parameter | Value | Reason |
|-----------|-------|--------|
| `n_neighbors` | Auto-tuned via CV | Best K found by cross-validation |
| `metric` | `euclidean` | Standard distance for numeric features |
| `weights` | `distance` | Closer neighbors have more influence |

### Fixes Applied

| Fix | What | Why |
|-----|------|-----|
| ✅ Fix 1 | Threshold = `6.0` (not 7.0) | Balances class distribution |
| ✅ Fix 2 | `weights='distance'` | Reduces majority class bias |
| ✅ Fix 3 | SMOTE oversampling | Generates synthetic minority samples |

---

## 📈 Results

| Metric | Before Fixes | After Fixes |
|--------|-------------|-------------|
| Overall Accuracy | 78% | ~80–85% |
| High Rated Recall | 15% | ~65–75% |
| High Rated F1 | 0.23 | ~0.65–0.75 |
| Low Rated Recall | 97% | ~80–85% |

> **Root cause of poor initial results:** 77% of movies were low-rated, causing KNN to almost always predict "Low".

---

## 🎥 Predicting a New Movie

In **Cell 13**, modify the values to predict any movie:

```python
new_movie = pd.DataFrame([{
    'budget':        50000000,    # budget in USD
    'popularity':    25.0,        # TMDB popularity score
    'runtime':       120,         # minutes
    'revenue':       200000000,   # box office earnings in USD
    'vote_count':    3000,        # number of ratings
    'in_collection': 1,           # 1 = part of series, 0 = standalone
}])

new_movie['genre_Action'] = 1    # set your movie's main genre
```

**Output:**
```
Prediction : ⭐ HIGH rated
Confidence : Low=0.23  High=0.77
```

---

## ⚠️ Limitations

- `vote_count` is used as a feature — in production this would be unknown for unreleased movies
- Genre is simplified to the **first/main genre** only
- Movies with `vote_average = 0` (unrated) are excluded from training
- KNN is slow on very large datasets — consider Approximate Nearest Neighbors (ANN) for scale

---

## 🛠️ Tech Stack

- **Language:** Python 3.8+
- **ML Library:** scikit-learn
- **Imbalance Fix:** imbalanced-learn (SMOTE)
- **Environment:** Jupyter Notebook
- **Dataset:** TMDB Movies Metadata

---

*Built as part of a machine learning classification project using the TMDB dataset.*