# Unsupervised_Learning_Iris_Dataset_Classification

## Objective
The objective of this project is to apply clustering techniques to the Iris dataset in order to explore how unsupervised learning can group data points based on similarities in their features. The clustering algorithms used in this project are **KMeans** and **Hierarchical Clustering**.

## Dataset
The project utilizes the well-known **Iris dataset** available in the `sklearn` library. The dataset consists of 150 data points, each with 4 features:
- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

These features are used for clustering, with the target species label excluded as it is not needed for the clustering task.

## Key Components

### 1. **Loading and Preprocessing**
- The Iris dataset is loaded using the `sklearn.datasets.load_iris()` function.
- The target species column is excluded, as the focus is on unsupervised learning (clustering).

### 2. **Clustering Algorithms**
Two clustering techniques are applied to the dataset:

#### A) **KMeans Clustering**
- **Description:** KMeans is a popular clustering algorithm that partitions data into `K` clusters by minimizing the variance within each cluster. The algorithm iteratively assigns data points to clusters and updates the cluster centroids until convergence.
  
- **Why KMeans for Iris:** KMeans is suitable for this dataset because the Iris dataset is known to have clear cluster structures (based on species), and KMeans can efficiently partition the data into `K=3` clusters.
  
- **Steps:** 
  - Apply KMeans with 3 clusters.
  - Visualize the clusters.
  - Calculate the Silhouette score to evaluate the clustering performance.

#### B) **Hierarchical Clustering**

- **Description:** Hierarchical clustering builds a tree-like structure called a dendrogram. It groups data points into clusters based on a similarity measure, either agglomerative (bottom-up) or divisive (top-down).
  
- **Why Hierarchical Clustering for Iris:**
- Hierarchical clustering is useful for understanding the data's structure, especially when we want to examine how clusters merge or split. It also doesn’t require specifying the number of clusters beforehand, making it flexible for exploratory analysis.
  
- **Steps:**
  
  - Apply Hierarchical clustering (Agglomerative).
  - Visualize the resulting clusters using a dendrogram.
  - Calculate the Silhouette score to evaluate the clustering performance.

### 3. **Silhouette Score**

- The **Silhouette Score** is used to measure the quality of clusters. A higher Silhouette score indicates that the data points are well-clustered.
  
- The score ranges from -1 to 1, where:
  - 1 indicates the clusters are well-separated.
  - 0 indicates overlapping clusters.
  - Negative values suggest that data points are incorrectly clustered.

## Requirements
- Python 3.x
- Libraries:
  - `pandas`
  - `sklearn`
  - `matplotlib`
  - `seaborn`
