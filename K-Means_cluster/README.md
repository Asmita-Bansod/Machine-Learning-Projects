Wine Dataset – K-Means Clustering
📌 Project Overview

This project applies K-Means Clustering to the Wine dataset to identify natural groups of wines based on their chemical characteristics.

K-Means is an unsupervised machine learning algorithm that groups similar data points into clusters without requiring predefined target labels.

🎯 Objectives
Explore and understand the Wine dataset.
Perform data preprocessing and feature scaling.
Apply K-Means clustering.
Determine a suitable number of clusters using the Elbow Method.
Evaluate clustering quality using the Silhouette Score.
Apply PCA (Principal Component Analysis) for dimensionality reduction and visualization.
Visualize the resulting clusters.
📊 Dataset

The project uses the Wine dataset, which contains chemical measurements of different wine samples.

🛠️ Technologies Used
Python
NumPy
Pandas
Matplotlib
Scikit-learn
PCA
K-Means Clustering

🔄 Project Workflow
Wine Dataset
     ↓
Data Exploration
     ↓
Data Preprocessing
     ↓
Feature Scaling
     ↓
Elbow Method
     ↓
Select Optimal K
     ↓
K-Means Clustering
     ↓
Silhouette Score
     ↓
PCA
     ↓
Cluster Visualization
     ↓
Conclusion

🤖 K-Means Clustering

K-Means divides the observations into K clusters.

The algorithm works by:

Selecting K initial centroids.
Assigning each data point to the nearest centroid.
Recalculating the centroids.
Repeating the process until the centroids stabilize.

📈 Elbow Method

The Elbow Method is used to help determine a suitable number of clusters.

It calculates the Within-Cluster Sum of Squares (WCSS) for different values of K.

📏 Silhouette Score

The Silhouette Score measures how well-separated the clusters are.

PCA Visualization

PCA is used to reduce the 13-dimensional feature space to two principal components so that the clusters can be visualized.

✅ Results

K-Means successfully identified groups of wine samples based on their chemical characteristics.

PCA provided a two-dimensional representation of the dataset, making the cluster structure easier to visualize.

The obtained Silhouette Score of approximately 0.299 suggests that the clusters have some meaningful structure, but the separation between clusters is not very strong.