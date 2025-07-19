# 🎧 Spotify Top Tracks (2000–2022): Unsupervised Machine Learning Analysis

![Python](https://img.shields.io/badge/Python-3.9-blue)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

> 🔍 A deep dive into two decades of top-charting music using unsupervised learning techniques.

---

## 📌 Overview

This project analyzes Spotify's **Top 100 Tracks per Year (2000–2022)** using unsupervised machine learning techniques like **PCA** and **clustering**. The goal is to uncover musical trends, genre evolution, and feature correlations using a combination of data preprocessing, dimensionality reduction, and clustering algorithms.

---

## 📁 Dataset

- **Rows**: 2,300 tracks  
- **Time span**: 2000–2022  
- **Features**:
  - 13 numeric audio features (e.g., `danceability`, `energy`, `acousticness`, etc.)
  - 9 nominal features (e.g., `artist_name`, `track_name`, `genre`, etc.)
  - Genres: Over 437 unique values, grouped into 6 major categories

---

## 🔧 Data Preparation

- ✅ Removed missing values (1 column dropped)
- ✅ Normalized numeric features using `StandardScaler`
- ✅ Categorized genres into 6 main classes (pop, rock, hip-hop, electronic, etc.)
- ✅ Implemented both **exclusive** and **non-exclusive** genre classification

---

## 📊 Techniques Applied

### 📉 Principal Component Analysis (PCA)
- Revealed low overall variance in first 2 components (under 40%)
- Identified key correlations:
  - High correlation between **track popularity** and **artist popularity**
  - Pop & hip-hop closely aligned with popularity
  - Rock genre appeared inversely related to popularity

### 🧩 Clustering Methods
- **Agglomerative Clustering** + dendrogram visualization
- **DBSCAN** with `eps=4` and `min_samples=4`
- **Elbow Method** used to determine optimal cluster count

**Note:** Clustering on the full dataset had limited impact. Better results were seen when segmenting by **year** and **genre**.

---

## 📈 Key Insights

- 📉 **Track durations have dropped** from ~4.1 to ~3.3 minutes on average
- 🎤 **Pop** is the dominant genre and strongly correlates with popularity
- 🧠 **No strong global correlations** among all features
- 🧍‍♂️ Artist concentration in top tracks has increased over time
- 🎵 **Acousticness** and **energy** are strongly negatively correlated (−0.54)

---

## 🧾 Conclusion

- PCA and clustering revealed subtle but meaningful trends in music over 20+ years.
- The evolution of genre popularity (esp. pop and hip-hop) shows the changing nature of mainstream music.
- Clustering top tracks remains complex due to overlapping musical characteristics and rapid industry shifts.

---

## 👨‍🔬 Authors

Ricardo Fernandez | Sarra Mahmoudi | Chenjie Qian | Soumiya Razzouk | Daniel Teran

---

## 📂 Repository Structure

```bash
.
├── docs/                           # Graphs and plots for PCA, clustering
├── Notebook                        # Jupyter notebooks for analysis
├── README.md                       # Project Overview
├── Report.pdf                      # Project Report
└── playlist_2010to2022.csv         # Raw dataset
****
