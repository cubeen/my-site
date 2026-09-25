---
layout: post
title: "Logistic Regression for Property Quality Classification"
date: 2026-09-24 10:00:00 +0100
categories: [Projects, Machine Learning]
tags: [python, scikit-learn, classification, logistic-regression, pandas, eda]
description: "A binary classification project identifying high-quality properties using Logistic Regression and feature engineering."
---

This project implements a Logistic Regression model to solve a supervised binary classification problem[cite: 3]. The objective is to identify properties of higher-than-standard construction and design quality utilizing the House Sales in King County, USA dataset[cite: 3].

## Feature Engineering and Target Definition
The original dataset includes a `grade` feature representing construction and design quality on a scale spanning from 1 to 13, where 7 denotes an average quality level[cite: 3]. Because the goal of this task is to isolate properties that exceed this standard, the continuous scale required transformation into a binary target variable[cite: 3]. 

The records were separated into two distinct categories: properties with a grade strictly greater than 7 were assigned a value of 1 (representing higher quality), while all remaining properties were assigned a value of 0[cite: 3]. This custom array formed the foundation for the classification task[cite: 3].

## Exploratory Data Analysis
Before model training, histograms and correlation scatterplots were generated to understand data distribution, spread, and the shape of the features[cite: 3]. Two distinct colors were mapped to the scatterplots to differentiate between the standard and higher-quality property categories[cite: 3]. 

A key challenge identified during the visual inspection was data congestion[cite: 3]. The scatterplots suffered from the overlay of multiple data points on top of one another[cite: 3]. This density made the data relatively more difficult to interpret visually compared to linear regression tasks where relationships are often more immediately apparent[cite: 3]. 

## Model Evaluation
The dataset was processed through a Logistic Regression pipeline. To ensure a comprehensive evaluation of the model's predictive capabilities on this binary classification task, multiple performance metrics were captured[cite: 3]:

* **Precision:** 0.85[cite: 3]
* **Recall:** 0.85[cite: 3]
* **F1 Score:** 0.85[cite: 3]
* **ROC AUC:** 0.930[cite: 3]

These metrics establish a strong baseline performance, demonstrating that the Logistic Regression algorithm can reliably distinguish between standard and premium property grades based on the selected feature set.