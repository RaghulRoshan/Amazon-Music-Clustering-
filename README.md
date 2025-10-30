# Amazon-Music-Clustering-

# 🎧 Song Clustering using Machine Learning

This project explores how to group songs based on their musical characteristics using **unsupervised learning**.  
It applies **K-Means**, **DBSCAN**, and **Hierarchical Clustering** to analyze audio features like **energy, danceability, acousticness, tempo, and mood**.

The main objective is to identify patterns and similarities between songs, allowing for better **music recommendation**, **playlist generation**, and **genre discovery**.

---

## 🚀 Project Overview

### 🎯 Goal
Cluster songs with similar characteristics based on audio features extracted from the dataset.

### 📂 Dataset
`single_genre_artists (1).csv` — contains various attributes of songs, such as:
- `danceability`
- `energy`
- `loudness`
- `speechiness`
- `acousticness`
- `instrumentalness`
- `liveness`
- `valence`
- `tempo`
- `duration_ms`

These features describe rhythm, mood, energy, and instrumentation — perfect for music clustering.

---

## 🧩 Machine Learning Workflow

### 1️⃣ Data Exploration
- Loaded dataset and viewed shape, columns, and datatypes  
- Checked for missing values and duplicates  
- Removed unnecessary columns (`track_name`, `artist_name`, `track_id`)

### 2️⃣ Feature Selection
Focused on audio features that best describe song sound & feel.

### 3️⃣ Feature Scaling
Used **StandardScaler** to standardize features before clustering.

### 4️⃣ Dimensionality Reduction (for Visualization)
- Applied **PCA** for 2D visualization
- Optionally used **t-SNE** for more complex patterns

### 5️⃣ Clustering Techniques
- **K-Means:** simple, effective baseline
- **DBSCAN:** detects noise & arbitrary-shaped clusters
- **Hierarchical Clustering:** visualized with dendrograms

### 6️⃣ Cluster Evaluation
Measured cluster quality using:
- **Silhouette Score** → higher is better  
- **Davies-Bouldin Index** → lower is better  
- **Inertia (SSE)** → compactness of clusters (for K-Means)

### 7️⃣ Visualization
- 2D PCA plots of clusters  
- Bar charts showing feature means per cluster  
- Heatmaps comparing clusters  
- Distribution plots for `danceability`, `energy`, `tempo`, etc.

### 8️⃣ Final Analysis & Export
- Added cluster labels to dataset  
- Grouped songs by cluster  
- Exported final results as:
  - `final_song_clusters.csv`
  - `cluster_summary_report.csv`

---

## 📊 Example Insights

| Cluster | Characteristics | Description |
|----------|----------------|--------------|
| 0 | High energy & danceability | 🎉 **Party / EDM Tracks** |
| 1 | High acousticness, low loudness | ☕ **Chill / Acoustic Tracks** |
| 2 | High speechiness | 🎤 **Rap / Spoken Word** |
| 3 | High valence & tempo | 😊 **Happy / Pop Songs** |
| 4 | High instrumentalness | 🎻 **Instrumental / Ambient** |

---

## 📈 Visual Examples

### PCA Cluster Visualization
Shows songs grouped by similarity in 2D feature space.  
*(You can save and attach images like these in your repo’s `/images` folder)*


---

## 💾 Output Files

| File | Description |
|------|--------------|
| `final_song_clusters.csv` | Full dataset with cluster labels |
| `cluster_summary_report.csv` | Mean feature values per cluster |
| `project_4.ipynb` | Jupyter notebook containing the full workflow |

