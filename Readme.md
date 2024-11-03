
# CryptoClustering Project

## Overview

This project is an analysis and clustering of cryptocurrency market data using unsupervised learning techniques, specifically K-Means clustering and Principal Component Analysis (PCA). The primary goal is to classify cryptocurrencies based on their price fluctuations across various timeframes, providing insights into potential investment and trading strategies.

## Project Objectives

1. **Normalize Data**: Use standard scaling techniques to normalize cryptocurrency price fluctuation data, ensuring consistency for clustering.
2. **Optimal Clustering with K-Means**:
   - Identify the best number of clusters (k) using the elbow method.
   - Cluster cryptocurrencies based on their price changes, using both the original scaled data and PCA-reduced data.
3. **Dimensionality Reduction with PCA**:
   - Apply PCA to reduce the number of features and retain only the most important components.
   - Visualize and analyze the resulting clusters in two dimensions to gain insights into cryptocurrency groupings.
4. **Analyze Feature Importance**:
   - Examine the influence of each original feature on the principal components, revealing which price fluctuations most strongly impact each component.

## Methods and Tools

### Data Preparation
- **StandardScaler** from `sklearn.preprocessing` is used to normalize the price fluctuation data, ensuring that features are on a similar scale for effective clustering.

### Clustering
- **K-Means Clustering** from `sklearn.cluster`: This unsupervised learning algorithm groups similar cryptocurrencies together based on their normalized price fluctuations.
- **Elbow Method**: Applied to both the original and PCA-reduced data to determine the optimal number of clusters, minimizing inertia (sum of squared distances within clusters).

### Dimensionality Reduction
- **Principal Component Analysis (PCA)** from `sklearn.decomposition`: PCA reduces the dataset to three principal components, simplifying clustering while retaining most of the data's variance.

### Visualization
- **Matplotlib**: Used to visualize the elbow curve for choosing the optimal number of clusters.
- **hvPlot**: Used for interactive scatter plots that display clusters in two dimensions, with each point representing a cryptocurrency and colored by its cluster assignment.

## Results and Insights

1. **Optimal Clusters**: Using the elbow method, the optimal number of clusters was determined for both the original and PCA-reduced data.
2. **Cluster Analysis**:
   - Clustering on the original data provides an overview of cryptocurrency groupings based on full-feature information.
   - Clustering on PCA-reduced data simplifies the visualization, showing similar groupings in a reduced dimension space.
3. **Feature Influence**:
   - Analysis of PCA component weights reveals which price fluctuations (e.g., 24-hour, 7-day, 1-year changes) have the strongest influence on each principal component.
   - This insight allows for potential identification of long-term vs. short-term trading characteristics among the clustered cryptocurrencies.

## How to Use

To run this notebook:
1. Install the required packages: `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `hvplot`, and `holoviews`.
2. Open the `Crypto_Clustering.ipynb` file in Jupyter Notebook or Jupyter Lab.
3. Execute each cell to process, cluster, and visualize the cryptocurrency data.

## Dependencies

This project relies on the following Python libraries:
- **pandas**: Data manipulation
- **numpy**: Numerical operations
- **scikit-learn**: Machine learning algorithms for scaling, clustering, and dimensionality reduction
- **matplotlib**: Data visualization
- **hvplot** and **holoviews**: Interactive plotting for Jupyter environments

## License

This project is licensed under the MIT License.
