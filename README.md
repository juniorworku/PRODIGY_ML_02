# Customer Segmentation using K-Means Clustering

This project aims to perform customer segmentation for a retail store based on customer data. The goal is to group customers based on their purchase history using K-means clustering, enhanced with feature engineering (including `Age` and `Gender`), and Principal Component Analysis (PCA) to visualize the clusters.

## Table of Contents
1. [Overview](#overview)
2. [Dataset](#dataset)
3. [Requirements](#requirements)
4. [Project Workflow](#project-workflow)
5. [Feature Engineering](#feature-engineering)
6. [PCA for Dimensionality Reduction](#pca-for-dimensionality-reduction)
7. [Clustering and Evaluation](#clustering-and-evaluation)
8. [Results](#results)
9. [Conclusion](#conclusion)

## Overview
Customer segmentation is a key strategy for businesses to understand their customers' behaviors and preferences. This project uses K-means clustering to group customers into distinct segments that can then be used for marketing strategies, loyalty programs, and targeted campaigns. By incorporating feature engineering (Age, Gender), and dimensionality reduction (PCA), we provide a more robust and visual understanding of these segments.

## Dataset

The dataset used in this project is from Kaggle: [Mall Customers Dataset](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python). It contains customer details like:
- CustomerID
- Gender
- Age
- Annual Income (k$)
- Spending Score (1-100)

This dataset is preprocessed, and features are engineered to include additional variables like `Age` and `Gender`.

## Requirements

The project is implemented using Python, with the following libraries required:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `sklearn`

You can install the required packages by running:

```sh
pip install pandas numpy matplotlib seaborn scikit-learn

```

## Project Workflow

1. Data Preprocessing: Load the dataset and explore it. Preprocess the data to handle any missing values and standardize the features for clustering.
2. Feature Engineering: Transform the Gender column into numerical values (Male = 1, Female = 0), and include Age, Annual Income, and Spending Score as additional features.
3. PCA: Apply PCA to reduce the dataset dimensions from 4 to 2 for better visualization while retaining the most important variance in the data.
4. K-Means Clustering: Apply K-means clustering to the PCA-reduced data, determining the optimal number of clusters using the Elbow method.
5. Evaluation: Evaluate the clusters based on customer behavior and characteristics, identifying opportunities for marketing, loyalty programs, and campaigns.
6. Visualization: Visualize the clusters in 2D using the principal components from PCA.

## Feature Engineering

To enhance the clustering process, include additional features such as Age and Gender. The Gender column is encoded as follows:

- Male = 1
- Female = 0
These features are combined with Annual Income and Spending Score for clustering.

## PCA for Dimensionality Reduction

To visualize the clusters, reduce the dimensionality of the dataset using PCA (Principal Component Analysis) from 4 dimensions to 2. PCA helps in retaining the essential variance while simplifying the clustering problem.

## Clustering and Evaluation

Apply K-means clustering to the PCA-reduced data, using the Elbow method to determine the optimal number of clusters (in this case, K=5). The clusters are evaluated by analyzing customer characteristics like age, income, and spending behavior.

## Visualizing Clusters

## Results
The customer segmentation yielded 5 clusters, each with distinct characteristics based on spending behavior, income, and demographic variables. Here are some observations from the clusters:

- Cluster 0: High income, high spending – Premium customer group, perfect for loyalty programs.
- Cluster 1: Low income, high spending – Value-focused group, sensitive to discounts and offers.
- Cluster 2: High income, low spending – Potential upsell candidates, prefer quality over quantity.
- Cluster 3: Low income, low spending – Budget-conscious group, focus on essential items and promotions.
- Cluster 4: Average income and spending – Balanced customers, may benefit from general offers.

## Conclusion

By clustering customers based on their age, gender, income, and spending behavior, gained valuable insights that can drive targeted marketing strategies. Through feature engineering and PCA, the model successfully segmented customers into distinct groups, providing actionable insights for designing loyalty programs, marketing campaigns, and personalized promotions.