---
layout: post
title: "Project 1: Property Valuation via Linear Regression"
date: 2026-09-25 12:00:00 +0100
categories: [Projects, Machine Learning]
tags: [python, scikit-learn, pandas, regression]
description: "An end-to-end implementation of a Linear Regression model to predict continuous house prices using the King County dataset."
---

## Objective
This project implements a foundational supervised machine learning pipeline to predict real estate values. Using the House Sales in King County, USA dataset[cite: 2], the model evaluates numerous property features to predict the continuous target variable: the actual selling price[cite: 2].

## Data Pipeline & Preprocessing
To ensure strict model validity and prevent data leakage, the pipeline was structured with a strict separation between training and testing environments[cite: 2]. 

* **Data Splitting:** The dataset was divided using an 80/20 split, allocating 80% for training and 20% for final performance testing[cite: 2].
* **Exploratory Data Analysis (EDA):** Initial inspection mapped the minimum and maximum values, spread, and shape of the data using Pandas, alongside visual mapping of feature relationships against the target house price using Matplotlib and Seaborn[cite: 2].
* **Feature Selection:** Variables that did not add predictive value were trimmed from the dataset, while features demonstrating strong correlations with the target variable were strategically retained for the algorithm[cite: 2].
* **Dynamic Preprocessing:** To accommodate the algorithm's sensitivity to data variability, dynamic preprocessing was executed using Scikit-Learn[cite: 2]. Scaling and transformation were applied exclusively within the training folds to leave the underlying dataset intact and prevent data leakage[cite: 2].
* **Validation:** K-Fold Cross-Validation was implemented to iteratively train and validate the model, ensuring stability and accuracy across different data subsets[cite: 2].

## Performance Metrics
The Linear Regression model established the baseline predictive performance for this dataset. The evaluation yielded the following metrics[cite: 2]:

| Metric | Value |
| :--- | :--- |
| **$R^2$ Score** | 0.6583[cite: 2] |
| **Mean Absolute Error (MAE)** | $126,761.34[cite: 2] |
| **Root Mean Squared Error (RMSE)** | $227,275.50[cite: 2] |
| **Mean Squared Error (MSE)** | $51,654,153,770.71[cite: 2] |

While the linear model successfully captured the broader pricing trends, the $R^2$ variance score of 0.6583 indicates that more complex, non-linear relationships within the property features require an ensemble approach for higher accuracy[cite: 2].