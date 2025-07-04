# 🛍️ Mall Customer Segmentation using K-Means Clustering

This project applies **unsupervised learning** techniques to segment customers based on their behavior, specifically their **annual income** and **spending score**. The dataset used is the popular [Mall Customers dataset](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python).

---

## 📁 Dataset Overview

The dataset contains:
- **CustomerID**
- **Gender**
- **Age**
- **Annual Income (k$)**
- **Spending Score (1–100)**

Only relevant numerical features were used for clustering.

---

## ✅ Objective

The goal is to:
- Segment customers into distinct groups using **K-Means clustering**
- Identify optimal number of clusters using the **Elbow Method** and **Silhouette Score**
- Visualize the clusters to derive meaningful insights
- Provide **business recommendations** for marketing strategies

---

## 🛠️ Tools and Libraries Used

- **Python**
- `pandas` for data handling
- `matplotlib` and `seaborn` for data visualization
- `scikit-learn` for:
  - `KMeans` clustering
  - `StandardScaler` for normalization
  - `PCA` for dimensionality reduction
  - `silhouette_score` for evaluation

---

## 🔄 Workflow

### 1. Data Preprocessing
- Removed categorical features like `Gender`,`UserID`.
- Selected numerical features (`Annual Income`, `Spending Score`)

### 2. Choosing Optimal Clusters

- **Elbow Method**:  
  Plotted number of clusters (K) vs. inertia (within-cluster sum of squares)

- **Silhouette Score**:  
  Measured clustering quality (cohesion vs. separation).  
  Found highest score at **K = 5**

### 3. Model Training

- Applied `KMeans(n_clusters=5)`
- Cluster labels were assigned to each customer

### 4. Visualization

- Plotted clusters using PCA-reduced 2D data
- Each point color-coded based on cluster label

### 5. Evaluation

- Compared inertia and silhouette scores across different `k` values
- Found optimal K = **5**, giving well-separated and meaningful clusters

---

## 📊 Results

- **Optimal clusters: 5**
- **Key customer groups identified:**

| Cluster | Description                            |
|---------|----------------------------------------|
| 0       | High income, high spenders             |
| 1       | Low income, low spenders               |
| 2       | Young customers with high spending     |
| 3       | Moderate income, average spenders      |
| 4       | High income, cautious spenders         |

---

## 📌 Future Improvements

- Try **hierarchical clustering** or **DBSCAN**
- Include more features like `Age`, `Gender`
- Integrate real-time customer behavior data

---

## 📎 References

- [Scikit-learn Documentation](https://scikit-learn.org/stable/)
- [K-Means Clustering - Wikipedia](https://en.wikipedia.org/wiki/K-means_clustering)
- [Mall Customer Dataset - Kaggle](https://www.kaggle.com/vjchoudhary7/customer-segmentation-tutorial)

---

## 🧾 License

This project is for educational purposes.
