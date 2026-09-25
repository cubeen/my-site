---
layout: post
title: "Project 4: Random Forest Classifier for Property Grade Identification"
date: 2026-09-25 12:00:00 +0100
categories: [Projects, Machine Learning]
tags: [python, classification, random-forest, scikit-learn]
description: "Implementing a Random Forest Classifier to identify high-quality properties in the King County housing dataset."
---

This project implements a Random Forest Classifier to solve a binary classification problem using the House Sales in King County, USA dataset[cite: 3]. The objective was to identify properties that possess a higher than standard construction and design quality grade[cite: 3].

### Feature Engineering the Target Variable
The original dataset features a `grade` column with values spanning from 1 to 13, where 7 represents an average level of construction and design quality[cite: 3]. To frame this as a supervised binary classification task, the data was separated into two distinct categories[cite: 3]. 

A new array of integers was engineered to store this separation[cite: 3]. Properties with a quality grade score strictly higher than 7 were assigned a value of `1`, indicating higher than standard quality[cite: 3]. All remaining properties (grade 7 and below) were assigned a value of `0`[cite: 3].

### Exploratory Data Analysis
Histograms and correlation scatterplots were utilized to understand the foundational qualities of the data, including the distribution, spread, and shape of the features[cite: 3]. 

When visualizing the data to identify the best features for the model, two colors were used to differentiate between the newly created binary categories[cite: 3]. The scatterplots presented challenges due to the congestion and overlay of multiple data points, making the data relatively more difficult to interpret visually compared to linear relationships[cite: 3]. 

### Model Performance
The Random Forest Classifier was evaluated against several classification metrics. It demonstrated robust predictive capabilities in identifying high-grade properties, outperforming the logistic regression baseline. The model achieved the following results:

| Performance Metric | Random Forest Classifier Score |
| :--- | :--- |
| **Precision** | 0.89[cite: 3] |
| **Recall** | 0.89[cite: 3] |
| **F1 Score** | 0.89[cite: 3] |
| **ROC AUC** | 0.957[cite: 3] |

The ensemble nature of the Random Forest algorithm allowed it to effectively map the complex relationships within the property features, resulting in a highly accurate classification boundary for premium real estate.