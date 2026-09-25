---
layout: post
title: "Random Forest Regression Optimization for Property Valuation"
date: 2026-09-24 12:00:00 +0100
categories: [Projects, Machine Learning]
tags: [python, regression, random-forest, scikit-learn]
description: "Implementing an optimized Random Forest Regression model to predict real estate prices, featuring dynamic preprocessing and K-Fold cross-validation."
---

## Project Overview

This project focuses on predicting continuous target variables—specifically, the actual selling value of properties—using the House Sales in King County, USA dataset[cite: 2]. While linear models establish a baseline understanding of feature relationships, predicting property prices in a highly dimensional dataset often requires algorithms capable of capturing complex, non-linear interactions. This case study details the implementation and optimization of a Random Forest Regression model.

## Data Pipeline and Preprocessing

To safeguard against data leakage, the dataset was strictly partitioned using an 80/20 train-test split[cite: 2]. This ensured that 80% of the data was dedicated to model training while the remaining 20% was held back to evaluate generalized performance[cite: 2].

Prior to training, the feature space underwent rigorous inspection to understand minimum and maximum values, spread, and the shape of the data distributions[cite: 2]. Because different algorithms exhibit varying sensitivities to data variance, dynamic preprocessing was utilized exclusively during the training phase[cite: 2]. 

Key pipeline steps included:
*   **Dynamic Scaling:** Transformations such as feature scaling were applied dynamically within the pipeline only for algorithms that computationally benefited from it, leaving the raw dataset intact to prevent unfair bias in comparative model testing[cite: 2].
*   **K-Fold Cross-Validation:** The model was iteratively trained and validated across multiple folds to guarantee accuracy and ensure the model did not overfit to a specific training subset[cite: 2].
*   **Feature Selection:** Variables were strategically assessed for correlation with the house price target variable, and the feature space was trimmed to remove variables that did not add predictive value[cite: 2].

## Model Optimization and Performance

Following the baseline training, hyperparameter tuning was conducted to identify the optimal set of parameters that yielded the best performance for the Random Forest algorithm[cite: 2]. 

The resulting model demonstrated robust predictive capabilities, significantly outperforming linear baseline models. The Random Forest Regressor captured 87% of the variance in the target variable, compared to the 65.83% variance captured by a standard Linear Regression model[cite: 2].

### Evaluation Metrics

The final optimized model was evaluated against the isolated 20% test set using the following strict continuous performance metrics[cite: 2]:

| Metric | Random Forest Regression Performance |
| :--- | :--- |
| **R squared** | 0.8703 |
| **Mean Absolute Error (MAE)** | $75,768.29 |
| **Root Mean Sq. Error (RMSE)** | $140,043.31 |
| **Mean Squared Error (MSE)** | $19,612,128,403.70 |