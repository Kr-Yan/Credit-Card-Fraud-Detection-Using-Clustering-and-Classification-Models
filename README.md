# Credit Card Fraud Detection Using Clustering and Classification Models

## Overview

Credit card fraud is a significant issue in today's digital economy, leading to substantial financial losses for individuals and institutions. This project aims to explore the relationships between transaction amount, time, and various other variables to differentiate between fraudulent and non-fraudulent transactions. By applying clustering and classification models, we seek to identify key patterns and variables that are most indicative of fraudulent behavior.

## Project Objectives

The primary goals of this project are:

1. **Data Exploration**: Understand the dataset and identify key variables that correlate with fraudulent transactions.
2. **Feature Engineering**: Create meaningful features to enhance the model's ability to detect fraud.
3. **Model Development**: Apply various clustering and classification algorithms to differentiate between fraudulent and non-fraudulent transactions.
4. **Model Evaluation**: Assess the performance of the models using precision, recall, F1 score, Silhouette Index, and Calinski-Harabasz Index.
5. **Ensemble Learning**: Combine the results of individual models to improve overall detection accuracy.

## Data Description

The dataset used in this project contains 284,807 transactions, each represented by 31 variables:

- **Time**: Duration since the first transaction.
- **Amount**: Transaction amount.
- **Class**: Binary label indicating whether the transaction is fraudulent (`1`) or non-fraudulent (`0`).
- **V1-V28**: 28 anonymized features derived from the original data to protect privacy.

### Feature Engineering

We employed several feature engineering techniques to extract the most informative variables for our models. The variables that showed the most significant impact on the time and amount of fraudulent transactions were V13, V15, V19, V24, and V26. These features were identified through methods like PCA (Principal Component Analysis) and t-SNE (t-Distributed Stochastic Neighbor Embedding).

## Methodology

### 1. Clustering and Classification Models

We applied four different algorithms to cluster and classify the data:

- **K-means++**: A clustering algorithm that initializes centroids to minimize within-cluster variance.
- **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**: A clustering method that groups together points that are closely packed and marks as outliers the points that lie alone in low-density regions.
- **Logistic Regression**: A classification model used to predict the probability of a binary outcome.
- **Zero-Inflated Model**: A statistical model that accounts for an excess of zero-count observations in the data.

### 2. Performance Evaluation

The performance of each model was evaluated using the following metrics:

- **Precision**: The proportion of true positive results among the total positive predictions.
- **Recall**: The proportion of true positive results among the total actual positives.
- **F1 Score**: The harmonic mean of precision and recall.
- **Silhouette Index**: Measures how similar a point is to its own cluster compared to other clusters.
- **Calinski-Harabasz Index**: Assesses the ratio of the sum of between-cluster dispersion and of inter-cluster dispersion.

### 3. Ensemble Learning

To improve model performance, we applied ensemble learning techniques such as Max-Voting and Stacking to combine the predictions of the four models.


### Visualizations

- **PCA and t-SNE Plots**: Showed distinct clusters for fraudulent and non-fraudulent transactions.
- **Histograms**: Displayed the distribution of transaction amounts and times, highlighting the patterns in fraudulent cases.
- **Pairplots**: Revealed relationships among the top five variables, helping to understand the variance in transaction behavior.

## Limitations

While our study identified key variables and effective models, it was limited by the dataset size and potential selection bias. The data may not be fully representative due to differences in transaction sources and risk levels. Additionally, the study could benefit from cross-validation to better assess model performance and generalizability.

## Conclusion

This project provides insights into the characteristics of fraudulent transactions and demonstrates the application of clustering and classification models to detect fraud. While the DBSCAN model showed the best performance, there is room for improvement by expanding the dataset and refining the feature engineering process.

## Files in This Repository

- `data/`: Contains the dataset used for analysis.
- `scripts/`: Includes the Python scripts for data preprocessing, model training, and evaluation.
- `models/`: Saved models and performance metrics.
- `results/`: Visualizations and model performance summaries.
- `ensemble/`: Ensemble learning scripts and results.

## How to Run

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Kr-Yan/credit-card-fraud-detection.git
   cd credit-card-fraud-detection
