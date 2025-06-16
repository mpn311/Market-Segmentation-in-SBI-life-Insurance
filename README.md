# Customer-Segmentation-for-SBI-Life-Insurance

Google Colab Link : https://colab.research.google.com/drive/1leq8wT4kIlASNu2mo9UBVE0OsnDV-6k3?usp=sharing

## Overview
This project aims to develop a customer segmentation model for SBI Life Insurance using behavioral data from credit card holders. By identifying distinct customer groups, SBI Life Insurance can better target products such as savings plans, loans, and wealth management services.

## Dataset
- Source: Kaggle
- Dataset Link : https://www.kaggle.com/datasets/arjunbhasin2013/ccdata
- Description: Behavioral data of ~9,000 active credit card holders over six months.
- Features: 18 behavioral variables (e.g., balance, purchases, cash advances, credit limits).


## Problem Statement
Accurate segmentation allows SBI Life Insurance to tailor marketing strategies, improve customer engagement, and optimize financial product recommendations.

## Steps and Methodology


## Data Preprocessing:

- Skewed data normalized using Log Scaling.
- Features scaled using MinMaxScaler.
- Dimensionality reduced using Principal Component Analysis (PCA) for visualization and performance improvement.


## Clustering Algorithms Applied:

- K-Means Clustering: Tested with different values of k
- Agglomerative Clustering: Used hierarchical techniques with dendrograms.
- DBSCAN: Density-based clustering to identify arbitrary-shaped clusters and noise.


## Evaluation Metrics:

- Silhouette Score calculated for each algorithm to determine clustering performance.

| Clustering Algorithm | Silhouette Score         |
|-----------------------|--------------------------|
| K-Means              | 0.6865277503916535       |
| Hierarchical         | 0.6862802533330135       |
| DBSCAN               | 0.6429220048286987       |

We have chosen DBSCAN as the best model.

### DBSCAN outperformed K-Means and Agglomerative Clustering due to its ability to:
- Handle noise and outliers effectively.
- Identify arbitrarily shaped clusters.
- Avoid reliance on a predefined number of clusters.


## Visualization:

- Clusters visualized in 3D scatter plots using PCA-reduced data.


## Cluster Insights and Recommendations


| Cluster | Behavior                                | Recommendation                                           |
|---------|-----------------------------------------|---------------------------------------------------------|
| Cluster 0 | Installment Purchasers                 | Promote installment plans and reward timely payments.   |
| Cluster 1 | Cash Advance Users                     | Offer better cash advance terms and promote card usage. |
| Cluster 2 | One-Off Purchasers                     | Provide cashback/rewards and increase credit limits.    |
| Cluster 3 | Low Spenders (No Installments)         | Incentivize spending with installment benefits.         |
| Cluster 4 | Big Spenders (No Cash Advances)        | Retain high-value customers with loyalty programs.      |
| Cluster 5 | Low Financial Usage                    | Target with promotional offers for trial usage.        |
| Cluster 6 | High Credit Limit, Diverse Usage       | Reward with points, perks, and personalized benefits.   |
| Cluster 7 | Niche Segment                          | Tailor offers to specific preferences.                  |




### Future Scope
- Enhanced Models: Explore advanced clustering methods like deep learning.
- Customer Insights: Include richer datasets, such as transaction history.
- Business Applications: Develop personalized marketing campaigns and product recommendations.
