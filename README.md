#  Warehouse Sales Clustering
This repository contains a notebook for clustering products based on monthly sales patterns using Warehouse & Retail Sales data. The workflow includes data preprocessing, time-series panel construction, feature transformation, optimal cluster selection, and PCA-based visualization.

---
## Description 
The notebook processes retail and warehouse sales data, reshapes it into a monthly time-series per product, and applies clustering to identify groups of products with similar sales behavior.
K-Means is used as the main clustering algorithm, while PCA is used for 2-dimensional visualization.

---
## Project Motivation / Problem Statement
Retail and warehouse environments often manage hundreds of products with unpredictable and inconsistent sales patterns. Treating all products equally leads to inefficient inventory planning, poor forecasting, and missed business opportunities.
This project aims to identify groups of products with similar monthly sales behavior using clustering, enabling better segmentation, inventory strategies, and data-driven decision-making.

---

## Dataset
The dataset contains monthly sales records per product, including retail sales, retail transfers, warehouse sales, year, month, item code, and item description. A TOTAL_SALES column is created by summing all sales fields. A DATE column is generated from year–month, and the data is reshaped into a complete monthly time-series for each product. Only products with at least 12 months of data are kept. The final pivoted dataset represents each product’s monthly sales (1–12) and is used as input for clustering.

---

## Project Pipeline
1.Load & Inspect Data
Read the dataset, examine structure, data types, and missing values.
2.Preprocessing
Convert numeric columns, fill missing values, create TOTAL_SALES, and generate a unified DATE column.
3.Time-Series Panel Construction
Build complete monthly sequences per product, fill missing months, and keep only items with ≥12 months of data.
4.Pivot to Wide Format
Transform the data into an ITEM CODE × MONTH matrix representing monthly sales.
5.Feature Scaling
Standardize the pivoted data using StandardScaler.
6.Cluster Selection
Test K=2–8 and choose the best number of clusters using the Silhouette Score.
7.K-Means Clustering
Fit the model and assign cluster labels to each product.
8.PCA Visualization
Reduce dimensions to 2 components using PCA and visualize cluster separation.

---

##  Results
-The optimal number of clusters was determined using Silhouette Score, producing a clear separation of product sales patterns.
-Each product was successfully assigned to a cluster based on its monthly sales distribution.
-The pivoted time-series matrix revealed distinct seasonal and volume-based differences across product groups.
-PCA visualization showed well-defined cluster groupings, confirming that the chosen clustering structure captures meaningful variations in sales behavior.
-The final output provides:
-Cluster labels for each product
-A complete monthly sales panel for further analysis
-A 2D scatter plot illustrating cluster separation

