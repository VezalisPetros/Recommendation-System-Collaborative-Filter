
# 🎬 Movie Recommendation System – Collaborative Filtering

## 📌 Overview

This project implements an item-based collaborative filtering recommendation system using the **MovieLens 100K dataset**. The goal was to analyze the impact of similarity measures, neighborhood sizes, and popularity-aware weighting on predictive performance. The system is rigorously evaluated using metrics such as **Mean Absolute Error (MAE)**, **Macro Average Precision**, and **Macro Average Recall** under varying experimental conditions.

> 🎯 **Focus**: Collaborative Filtering (Item-based)  
> 🗂️ **Dataset**: [MovieLens 100K](https://grouplens.org/datasets/movielens/100k/)  
> 👨‍💻 **Author**: Petros Vezalis – Programming Assignment, University of Macedonia  
> 📅 **Date**: February 2025

---

## 🎯 Objectives

- Build a scalable item-based collaborative filtering system.
- Compare **Cosine Similarity** and **Pearson Correlation**.
- Implement 3 prediction functions:
  - Basic Weighted Average
  - Popularity-Favoring Weighted Average
  - Low-Popularity-Favoring Weighted Average
- Conduct experiments by varying:
  - `N` (nearest neighbors),
  - `T` (training size),
  - `M`, `M'` (minimum ratings per movie/user)
- Evaluate results using **MAE**, **Precision**, **Recall**, and **Confusion Matrices**.

---

## 🛠 Techniques & Tools

| Component | Techniques / Tools |
|----------|---------------------|
| **Filtering** | Movies and users filtered by rating count |
| **Similarity Measures** | Cosine Similarity, Pearson Correlation |
| **Prediction Functions** | Basic, Popularity-Favoring, Low-Popularity-Favoring |
| **Evaluation Metrics** | MAE, Macro Precision, Macro Recall |
| **Validation** | K-Fold Cross-Validation |
| **Visualization** | Matplotlib, Seaborn |
| **Language** | Python, NumPy, Pandas, Scikit-learn |

---

## 📊 Key Results

### 🔢 Best Configuration (N=90, Pearson, Basic Weighted Avg)
| Metric | Value |
|--------|-------|
| MAE    | **0.690** |
| Macro Precision | **0.616** |
| Macro Recall | **0.614** |

- **Pearson Correlation** consistently outperforms Cosine in **Precision** and **Recall**.
- **Cosine Similarity** yields lower **MAE** in dense data (after filtering).
- Popularity-based methods increase **Recall** but reduce **MAE** accuracy.
- Low-popularity methods promote diversity with comparable MAE.

---

## 🧪 Experiments Conducted

### 1. **Varying Number of Nearest Neighbors (N = 20–90)**
- Increasing `N` improves MAE.
- Best MAE: 0.690 (N=90, Pearson, Basic Weighted Avg).

### 2. **Impact of Training Size (T = 50%, 70%, 90%)**
- Slight MAE improvement as training data increases.
- Model performance saturates beyond 70%.

### 3. **Filtering Thresholds (M, M')**
- Higher `M` values (minimum ratings per movie) improve MAE and matrix density.
- Higher `M'` (active users) lowers data sparsity but has limited effect on MAE.

---

## 📂 Repository Structure

```bash
📁 Recommender-System
├── 📄 README.md
├── 📄 Recommendation System Collaborative Filter.pdf   # Full Report
├── 📄 Recommendation_System.ipynb                      # Jupyter Notebook with code
└── 📊 data/                                             # (Data not included)
```

> ⚠️ Dataset not included due to license – download from [MovieLens](https://grouplens.org/datasets/movielens/100k/)

---

## 📈 Visualization Insights

- 📌 **MAE** drops as N increases.
- 📌 **Precision/Recall** benefits more from Pearson than Cosine.
- 📌 **Filtering** makes rating matrices denser → better recommendations.

---

## 💡 Future Work

- Incorporate **matrix factorization** (SVD, NMF) and **neural collaborative filtering**.
- Adjust relevance threshold to “avg rating + delta” instead of user average.
- Combine content-based features for hybrid recommendations.
- Implement **real-time recommendation dashboard** using Streamlit or Dash.

---

## 🤝 Contact

I'm actively seeking opportunities in AI/Data Science & Recommender Systems.

- 📧 **ics22106@uom.edu.gr**
- 💼 LinkedIn: *(optional – add your profile)*

