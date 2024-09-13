# Customer-segmentation-using-k-means-with-PyTorch

This project focuses on customer segmentation using K-Means clustering and PyTorch. The goal is to group customers with similar characteristics, which is useful for targeted marketing and personalized services. By clustering customers based on their annual income and spending scores, we can identify distinct segments for improved business strategies.

**Overview of Clustering**

Clustering is a type of unsupervised learning that involves grouping similar data points together based on their characteristics. K-Means is a widely used clustering algorithm that partitions the dataset into K clusters, assigning each data point to the nearest centroid.

In this project, K-means clustering is combined with a neural network to leverage intrinsic data patterns for better segmentation.

**Project Steps**

**Step 1: Data Preparation**

We work with a mall customer dataset containing features like annual income and spending score. The goal is to segment customers based on these features.

Dataset: Mall Customer Segmentation
Features used for clustering:
Annual Income (k$)
Spending Score (1-100)
The dataset is loaded, and the relevant features are extracted and converted to PyTorch tensors for processing.

**Step 2: Applying K-Means Clustering**

Using the K-Means algorithm, the dataset is partitioned into K=5 clusters. The number of clusters is chosen based on the structure of the dataset and can be tuned using metrics like the silhouette score.

The silhouette score measures how well-defined the clusters are, with values ranging from -1 to 1. A high score close to 1 indicates that data points are well-separated between clusters.

Silhouette Score for 5 clusters: 0.553

**Step 3: Visualizing the Clusters**

Cluster visualization helps gain insights into the data structure and validate the clustering results. We plot the data points with:

- X-axis: Annual Income (k$)
- Y-axis: Spending Score (1-100)
- The color represents the cluster each point belongs to, and the cluster centroids are marked for clarity.
  
**Step 4: Making Predictions**

Finally, we perform inference on new customer data. Given a new data point:

Annual Income: 20

Spending Score: 60

The model assigns the data point to the closest cluster based on its Euclidean distance to the centroids.

Predicted cluster for the new data point: Cluster 0

**Results**

- Number of Clusters: 5
- Silhouette Score: 0.553
- Predicted Cluster for New Customer (Annual Income = 20, Spending Score = 60): Cluster 0

**License**

This project is licensed under the MIT License - see the LICENSE file for details.
