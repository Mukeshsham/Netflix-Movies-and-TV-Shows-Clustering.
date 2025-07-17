# 🎬 Netflix Movies & TV Shows Clustering

This project applies unsupervised learning techniques to cluster Netflix content (movies and TV shows) based on features like genres, duration, rating, and release year. The clustering helps uncover hidden structures in the data, useful for content recommendation, market segmentation, and trend analysis.

---

## 📌 Objective

- Preprocess and engineer features from the Netflix dataset.
- Apply KMeans, Agglomerative Clustering, and DBSCAN.
- Evaluate and compare clustering results using Silhouette Score.
- Visualize clusters using PCA.

---

## 📂 Dataset

- **Source:** [Netflix Movies and TV Shows (Kaggle)](https://www.kaggle.com/datasets/shivamb/netflix-shows)
- **Attributes Used:**
  - `listed_in` (Genres)
  - `duration`
  - `rating`
  - `release_year`
  - `description`

---

## ⚙️ Feature Engineering

- Multi-genre handling using `MultiLabelBinarizer`
- Description `Converted to vector using Average Word2vec`
- Duration converted to minutes
- Categorical encoding
- Standard scaling for numerical features

---

## 🤖 Clustering Models Used

- **KMeans Clustering**
- **Agglomerative Clustering**
- **DBSCAN** (density-based clustering)

---

## 📏 Evaluation — Silhouette Score

Silhouette Score evaluates how similar each point is to its own cluster compared to other clusters.

### 📊 Model Comparison Table

| Algorithm           | Distance Metric  | Silhouette Score  |
|---------------------|------------------|------------------|
| KMeans              | Euclidean        |    0.24          |
| KMeans              | Manhattan        |    0.34          |
| Agglomerative       | Euclidean        |    0.23          |
| Agglomerative       | Manhattan        |    0.31          |
| DBSCAN              | Euclidean        |    0.12          |
| DBSCAN              | Manhattan        |    0.13          |

> ✅ A higher Silhouette Score indicates better-defined and more cohesive clusters.  
> ❌ DBSCAN struggled due to sparse or overlapping data and sensitive hyperparameters.

---

## 📊 Visualizations

- **Elbow Plot** to determine optimal `k`
- **PCA (2D)** for visualizing clusters

---

## 🛠 Tech Stack

- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Jupyter Notebook

---
