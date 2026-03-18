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
Five K-Means models were compared using silhouette scores.

The best clustering model was **Model 3**:
- Highest-correlation features
- Unscaled data
- k = 2
- Silhouette score: 0.5271

Although K-Means produced useful segmentation patterns, supervised learning remained more appropriate for the bank’s prediction task.

## Repository Contents
- `income_classification_segmentation.Rmd`: full analysis
- `income_classification_segmentation.pdf`: knitted report
- `figures/`: exported visualizations
- `scripts/`: helper functions if needed

## Takeaway
This project demonstrates model selection based on business priorities, comparison of classification and clustering methods, and the interpretation of results in a decision-making context.
