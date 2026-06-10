Here's a professional GitHub README for your project:

# Comparative Analysis of Machine Learning Models for Global TB Burden Classification

## Overview

This project presents a comprehensive machine learning analysis of global tuberculosis (TB) burden classification using WHO TB burden estimates from 2016–2022. The study compares multiple supervised learning algorithms and evaluates their effectiveness in classifying countries into **Low**, **Medium**, and **High** TB burden categories.

The project follows a complete machine learning pipeline including data cleaning, exploratory data analysis (EDA), feature engineering, model training, evaluation, clustering analysis, and interpretation of results.

---

## Dataset

**Source:** World Health Organization (WHO) Global TB Burden Estimates

**Time Period:** 2016–2022

### Target Variable

Countries are classified into three TB burden categories based on TB incidence per 100,000 population:

* **Low Burden:** < 100 cases
* **Medium Burden:** 100–300 cases
* **High Burden:** > 300 cases

---

## Project Objectives

* Analyze global TB burden patterns.
* Compare the performance of multiple machine learning algorithms.
* Identify the most important predictors of TB burden.
* Evaluate whether natural clusters in the data align with WHO burden categories.
* Provide a reproducible framework for public health classification tasks.

---

## Machine Learning Models Evaluated

The study benchmarks **10 machine learning models**:

1. Support Vector Machine (RBF)
2. K-Nearest Neighbors (KNN)
3. Decision Tree
4. Random Forest
5. Gradient Boosting
6. AdaBoost
7. XGBoost
8. Stacking Ensemble
9. Gaussian Naive Bayes
10. Neural Network (MLP)

---

## Methodology

### Data Preprocessing

* Filtered data for years 2016–2022
* Created WHO-aligned TB burden classes
* Missing value imputation using regional medians
* Feature scaling using StandardScaler
* Class imbalance handling using SMOTE
* Time-based train-test split

### Train-Test Strategy

To avoid temporal data leakage:

* **Training:** 2016–2020
* **Testing:** 2021–2022

---

## Exploratory Data Analysis (EDA)

The notebook includes:

* TB burden class distribution
* Incidence distribution by burden category
* WHO region burden analysis
* Correlation heatmaps
* Temporal TB incidence trends
* Feature relationship exploration

---

## Evaluation Metrics

Models are evaluated using:

* Accuracy
* Precision
* Recall
* Macro F1-Score
* Confusion Matrix

---

## Clustering Analysis

The project also applies **K-Means Clustering** to investigate whether naturally occurring patterns in the data align with WHO-defined burden categories.

### Metric Used

* Adjusted Rand Index (ARI)

This provides insight into the consistency between unsupervised clustering and official TB burden classifications.

---

## Feature Importance

Random Forest feature importance analysis is used to identify the most influential variables contributing to TB burden prediction.

This helps improve model interpretability and highlights key public health indicators associated with TB prevalence.

---

## Novel Contributions

* First systematic benchmark of **10 machine learning models** on WHO TB burden classification.
* Uses a **time-based split** instead of random splitting to improve real-world validity.
* Incorporates **SMOTE** to address multi-class imbalance.
* Introduces **K-Means alignment analysis** with WHO burden categories.
* Evaluates a **Stacking Ensemble** combining:

  * SVM
  * Gradient Boosting
  * KNN
  * Logistic Regression Meta-Learner

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* XGBoost
* Imbalanced-Learn (SMOTE)

---

## Project Structure

```text
TB_ML_Analysis.ipynb
│
├── Data Loading & Inspection
├── Data Cleaning & Preprocessing
├── Exploratory Data Analysis
├── Feature Engineering
├── Model Training
├── Model Evaluation
├── Feature Importance Analysis
├── K-Means Clustering Analysis
└── Research Findings & Conclusions
```

---

## Future Improvements

* Incorporate socioeconomic indicators such as GDP and healthcare expenditure.
* Include environmental factors such as air pollution metrics.
* Perform hyperparameter optimization.
* Explore deep learning architectures with larger datasets.
* Develop an interactive dashboard for TB burden prediction.

---

## Author

**Hareem Jawad**
Business Analytics Student | FAST NUCES Lahore
Interested in Data Analytics, Machine Learning, and Public Health Applications of AI

---


This project is intended for educational and research purposes. Please cite the original WHO dataset and relevant sources when using or extending this work.
