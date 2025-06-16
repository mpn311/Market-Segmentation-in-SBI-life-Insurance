# 🧠 Customer Segmentation for SBI Life Insurance

🔗 **Google Colab Notebook:** [Open in Colab](https://colab.research.google.com/drive/1leq8wT4kIlASNu2mo9UBVE0OsnDV-6k3?usp=sharing)  
📂 **Dataset:** [Kaggle - Credit Card Data](https://www.kaggle.com/datasets/arjunbhasin2013/ccdata)

---

## 📌 Overview

This project focuses on building a **customer segmentation model** for **SBI Life Insurance** using behavioral data of credit card holders. By identifying unique customer clusters, SBI Life can:

- Tailor financial products (savings, loans, wealth management)
- Boost customer engagement
- Enhance targeted marketing strategies

---

## 📊 Dataset Details

- **Source**: Kaggle  
- **Records**: ~9,000 active credit card holders  
- **Duration**: 6 months of transactional behavior  
- **Features**: 18 behavioral metrics including:
  - Balance
  - Purchases
  - Cash Advances
  - Credit Limits
  - Payments, etc.

---

## 🧩 Problem Statement

> How can we segment customers based on behavior to help SBI Life Insurance offer **customized financial products**?

---

## 🔧 Methodology

### 🔹 Data Preprocessing

- Applied **Log Transformation** to handle skewness.
- Used **MinMaxScaler** to normalize feature values.
- Reduced dimensionality using **Principal Component Analysis (PCA)** for visualization and improved model performance.

### 🔹 Clustering Algorithms

| Algorithm              | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| **K-Means**            | Evaluated multiple k values to find optimal clusters                        |
| **Agglomerative**      | Used dendrograms and hierarchical strategies for grouping                   |
| **DBSCAN**             | Density-based approach to identify clusters of arbitrary shape and noise    |

---

## 📈 Evaluation

**Metric**: *Silhouette Score*

| Clustering Algorithm   | Silhouette Score        |
|------------------------|-------------------------|
| **K-Means**            | 0.6865                  |
| **Agglomerative**      | 0.6862                  |
| **DBSCAN**             | **0.6429**              |

> ✅ **DBSCAN** was chosen for its ability to:
- Handle **noise** and **outliers**
- Identify **non-spherical** clusters
- Avoid requiring a predefined number of clusters

---

## 🧠 Cluster Insights & Business Recommendations

| Cluster | Behavior                          | Recommendation                                              |
|--------:|-----------------------------------|-------------------------------------------------------------|
| 0       | Installment Purchasers            | Promote installment plans & reward timely payments          |
| 1       | Cash Advance Users                | Offer better terms and encourage responsible usage          |
| 2       | One-Off Purchasers                | Provide cashback/rewards & increase credit limits           |
| 3       | Low Spenders (No Installments)    | Incentivize with installment-based benefits                 |
| 4       | Big Spenders (No Cash Advances)   | Retain using loyalty programs and premium services          |
| 5       | Low Financial Usage               | Target with promotional offers to increase usage            |
| 6       | High Credit, Diverse Usage        | Reward with perks, points & personalized experiences        |
| 7       | Niche Segment                     | Tailor offers to unique needs and behavioral patterns       |

---

## 📊 Visualizations

- Used **PCA** for 3D projection of clusters  
- Enabled **visual differentiation** and pattern recognition between segments

---

## 🔭 Future Scope

- ✅ Explore **advanced clustering techniques** (e.g., Autoencoders, GMMs)
- ✅ Integrate **richer datasets** (e.g., transaction logs, demographics)
- ✅ Implement **real-time segmentation pipelines**
- ✅ Launch **personalized campaign engines** for each segment

---

## 🧑‍💼 Impact

A well-structured segmentation strategy allows **SBI Life Insurance** to deliver:
- Higher customer satisfaction
- Increased ROI on marketing
- Better product-market fit
