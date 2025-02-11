Cryptocurrency Clustering with K-Means and PCA
This project applies K-Means clustering to a dataset of cryptocurrency market data, using both the original data and data transformed by Principal Component Analysis (PCA) to reduce dimensionality. The goal is to analyze the clusters formed and understand the impact of using fewer features on clustering results.

Table of Contents
Introduction

Data Description

Project Setup

Data Preprocessing

K-Means Clustering

PCA Transformation

Cluster Analysis

Elbow Curve Analysis

Conclusion

Acknowledgements

Introduction
This project explores the clustering of cryptocurrency market data using K-Means clustering algorithm. We employ PCA to reduce the number of features and compare the clustering results using both original and PCA-transformed data.

Data Description
The dataset crypto_market_data.csv contains various attributes of different cryptocurrencies. The coin_id serves as the unique identifier for each cryptocurrency. Key features include price change percentages, trading volume, market cap, and more.

Project Setup
Clone the repository:

bash
git clone <repository-url>
cd <repository-directory>
Install required dependencies:

bash
pip install -r requirements.txt
Load the dataset:

python
import pandas as pd
df_market_data = pd.read_csv("Resources/crypto_market_data.csv", index_col="coin_id")
Data Preprocessing
Standardization: Use StandardScaler to standardize the numeric features.

DataFrame Creation: Create DataFrame for standardized data and ensure coin_id is the index.

K-Means Clustering
Compute inertia for a range of k-values (1 to 11) using original data.

Plot the Elbow curve to determine the optimal number of clusters.

PCA Transformation
Apply PCA to reduce the dataset to three principal components.

Create a new DataFrame for PCA-transformed data.

Cluster Analysis
Perform K-Means clustering on both the original and PCA-transformed data.

Analyze and interpret the resulting clusters.

Elbow Curve Analysis
Plot the Elbow curves for both original and PCA-transformed data.

Compare the clustering results and discuss the impact of using fewer features.

Conclusion
Summarize the findings from the cluster analysis and discuss the benefits and drawbacks of using PCA for dimensionality reduction in clustering.
