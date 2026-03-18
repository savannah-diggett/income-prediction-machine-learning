# Income Classification and Customer Segmentation

## Overview
This project uses the UCI Adult Income dataset to evaluate both supervised and unsupervised learning approaches for customer targeting in a banking context.

The business goal was to identify high-income individuals (earning more than $50K annually) as strong loan candidates while minimizing false positives. In other words, the bank wanted to avoid offering loans to lower-income individuals who were incorrectly classified as high-income.

## Business Objective
The primary objective was to minimize false positives, making precision and specificity the most important evaluation metrics. Recall was also considered important, but only after reducing the risk of approving the wrong customers.

## Methods
This project includes two tasks:

### 1. K-Nearest Neighbors (KNN) Classification
I trained and compared multiple KNN models with different values of k to predict whether a customer earned more than $50K.

### 2. K-Means Clustering
I tested multiple clustering specifications using different feature sets, scaling approaches, and numbers of clusters. Models were compared using silhouette scores.

## Dataset
UCI Adult Income dataset

The data was downloaded directly from the UCI Machine Learning Repository inside the R workflow.

## Tools Used
- R
- caret
- ggplot2
- dplyr
- kknn
- factoextra
- cluster
- kableExtra

## Key Results

### KNN Results
Three KNN models were tested using k = 2, 3, and 5.

The best model was **KNN with k = 5**:
- Accuracy: 77.36%
- Precision: 54.47%
- Recall: 36.29%
- Specificity: 90.38%

This model was selected because it best aligned with the bank’s main goal of avoiding false positives.

### K-Means Results
Five K-Means models were compared using silhouette scores. Model 3 performed best, using the highest-correlation features, unscaled data, and k = 2, with a silhouette score of 0.5271.

## Visualizations

The figures below summarize the final KNN model comparison and K-Means silhouette results.

![KNN Metrics](figures/knn_metrics.png)

![K-Means Silhouette Scores](figures/kmeans_silhouette.png)

## Repository Contents
- `income_classification_segmentation.Rmd`: full analysis
- `income_classification_segmentation.pdf`: knitted report
- `figures/`: exported visualizations
- `scripts/`: helper functions if needed

## Takeaway
KNN was more useful for the bank’s decision problem because the task involved predicting income class, while K-Means was better suited for exploratory segmentation.

