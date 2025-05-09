# 🎧 Spotify Data Analysis

## 📌 Introduction

This project focuses on analyzing data collected from Spotify to better understand user behavior, music preferences, and factors influencing song popularity.

## 🧹 Data Preprocessing & 📊 Exploratory Data Analysis (EDA)

### ✅ Data Preprocessing

* Handled missing values.
* Encoded categorical variables.
* Scaled numerical features to standardize the data.

### 📈 Exploratory Data Analysis (EDA)

* **Distribution Analysis**: Histograms were used to understand the distribution of features.
* **Outlier Detection**: Boxplots helped visualize the spread, central tendency, and detect any remaining outliers.
* **Feature Relationships**: A heatmap was generated to explore correlations between features in the cleaned dataset.

### 🔍 Streams vs Features

* **Heatmap**: Used to identify patterns that might influence a song's popularity.
* **Scatter Plots**: Visualized the relationships between stream counts and features like BPM, Danceability, and Playlist Inclusions.

---

## 🤖 Modeling

Two predictive models were used:

1. **Random Forest Classifier**
2. **Logistic Regression**

After preprocessing, these models were trained to predict the **popularity of songs**.

### 🎯 Genre Classification (Unsupervised)

* Since the dataset lacked an explicit *genre* column, **KMeans Clustering** was applied to group songs into genre-like clusters based on musical features.
* These genre clusters were then used to explore genre-based popularity predictions.

---

## 📊 Model Evaluation

### 🔵 Logistic Regression (Popularity Prediction)

* **Accuracy**: 91.86% — Very strong overall performance.
* **Class 0 (Not Popular)**: High precision and recall.
* **Class 1 (Popular)**:

  * **Recall**: 0.69 — Room for improvement; some popular songs were missed.
  * **Precision**: 0.89 — Most songs predicted as popular were indeed popular.
* **F1 Scores**:

  * **Macro Average**: 0.86
  * **Weighted Average**: 0.91
* **Key Influential Features**: Playlist and chart-related metrics were most predictive.
* **Cross-Validation Accuracy**: Mean = **90.95%** — Indicates strong generalizability and low risk of overfitting.

---

### 🟢 Random Forest Classifier (Popularity Prediction)

* **Test Accuracy**: 89.5%
* **Class 0 (Not Popular)**:

  * Precision: 0.92
  * Recall: 0.95
  * F1-score: 0.93
* **Class 1 (Popular)**:

  * Precision: 0.79
  * Recall: 0.72
  * F1-score: 0.76
* **F1 Scores**:

  * **Macro Average**: 0.84
  * **Weighted Average**: 0.89
* **Cross-Validation Accuracy**:

  * Range: 86.8% – 95.4%
  * Mean: **91.5%**, aligning well with test accuracy and indicating model stability.

---

## ✅ Conclusion

* Both models performed strongly in predicting song popularity.
* Playlist inclusion and chart appearance are top predictors.
* Genre classification using KMeans added an extra dimension to understanding music trends.
* Future improvements could involve boosting recall for popular songs and enhancing minority class detection.

