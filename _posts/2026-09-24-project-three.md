---
layout: post
title: "Automated Premium Property Classification using Logistic Regression"
date: 2026-09-24 10:00:00 +0100
categories: [Projects, Machine Learning]
tags: [python, scikit-learn, classification, logistic-regression, pandas, eda]
description: "A business-focused classification project demonstrating how machine learning can automate real estate portfolio segmentation by identifying premium assets."
---

In the real estate sector, rapidly identifying premium properties at scale is critical for investment targeting and automated valuation. This project demonstrates how machine learning can streamline portfolio segmentation by building a predictive engine to classify higher-than-standard quality properties based on the King County, USA housing dataset.

## Translating Subjective Metrics into Actionable Business Logic
Raw business data is rarely formatted for immediate algorithmic use. The dataset contained a subjective `grade` feature evaluating construction and design on a 1–13 scale. To align this with a clear business objective—flagging premium assets—I engineered a binary target variable. 

Properties exceeding the standard baseline (grade > 7) were classified as premium (1), while all others were categorized as standard (0). This feature engineering step converted a nuanced, subjective grading system into a strict, actionable metric tailored for automated classification tasks.

## Data Diagnostics and Overcoming Visual Noise
Effective feature selection requires a deep understanding of the underlying data distribution. I initially utilized correlation scatterplots and histograms to map the boundaries between standard and premium properties.

However, real-world datasets present immediate scaling challenges. The sheer volume of housing records led to severe visual congestion, rendering traditional scatterplots difficult to interpret. Recognizing this limitation, I adapted the analytical approach to rely on programmatic statistical correlations rather than visual diagnostics alone. This adaptability ensures that feature selection remains accurate, scalable, and data-driven regardless of dataset volume.

## High-Confidence Predictive Performance
The engineered features were processed through a Logistic Regression pipeline to establish a reliable, computationally inexpensive production baseline. The model's performance was evaluated using metrics that directly translate to business reliability:

* **Precision (0.85) & Recall (0.85):** Demonstrates a balanced, highly accurate ability to correctly identify premium properties without overwhelming the system with false alarms (false positives) or missing valuable assets (false negatives).
* **F1 Score:** 0.85
* **ROC AUC:** 0.930

The standout metric here is the ROC AUC of 0.930. This indicates the model has a 93% probability of correctly ranking a premium asset higher than a standard one. From a business perspective, this establishes Logistic Regression as a highly effective, reliable first-pass filter for real estate portfolio segmentation and automated investment targeting.