# Heart Disease Risk Prediction

This project aims to build a predictive model for assessing the risk of heart disease using logistic regression. The model is trained on two different datasets: a smaller dataset focusing on blood parameters and a larger dataset containing general health categories. Both oversampling (SMOTE) and undersampling techniques are applied to handle class imbalance.

## Project Overview

The goal of this project is to create reliable models to predict whether an individual is at risk of heart disease based on various features. The datasets contain two classes:
- `0`: Not at risk of heart disease
- `1`: At risk of heart disease

## Table of Contents

- Project Overview
- Datasets
- Preprocessing.
- Handling Imbalanced Data
  - SMOTE (Synthetic Minority Oversampling Technique)
  - Undersampling
- Model Training and Evaluation
- Feature Importance Analysis
- Log Loss Analysis
- Comparison of Datasets
- Tableau Visualization
- Conclusion

## Datasets

### Blood Parameters Dataset
This smaller dataset includes detailed blood parameters used as indicators of heart disease. This is the *heart-blood_data.csv*.

### General Health Categories Dataset
This larger dataset contains a variety of features related to general health categories, providing a broader perspective on factors influencing heart disease risk.
This is the *heart-categories.csv*.
## Preprocessing

- **Standardization:** The features are standardized using `StandardScaler` to have a mean of 0 and a standard deviation of 1.
- **Train-Test Split:** Each dataset is split into training and test sets using an 80-20 split.

## Handling Imbalanced Data

### SMOTE (Synthetic Minority Oversampling Technique)

SMOTE is used to generate synthetic samples for the minority class (`1`) to balance the class distribution.

#### Pros:
- Helps in balancing the class distribution without losing any original data.
- Improves the model's ability to generalize to the minority class.

#### Cons:
- May introduce noise by creating synthetic samples.
- Can lead to overfitting on the minority class.

### Undersampling

Undersampling reduces the number of samples in the majority class (`0`) to balance the class distribution.

#### Pros:
- Simple and effective for handling class imbalance.
- Reduces training time by working with a smaller dataset.

#### Cons:
- Loss of information from the majority class.
- Can lead to underfitting if too much data is removed.

## Model Training and Evaluation

- **Logistic Regression:** The model is trained using logistic regression on both datasets.
- **Metrics:** Precision, recall, F1-score, accuracy, and log loss are used to evaluate the model's performance.
- **Confusion Matrix:** A confusion matrix is generated to visualize the model's performance.

## Feature Importance Analysis

The coefficients of the logistic regression model are analyzed to identify the most influential features in each dataset.

## Log Loss Analysis

The log loss (binary cross-entropy) is analyzed as a function of the training data size to understand how the model's performance improves with more data.

## Comparison of Datasets

The performance of the logistic regression model is compared between the blood parameters dataset and the general health categories dataset to understand the impact of different types of features on the prediction of heart disease risk.

## Tableau Visualization

A Tableau visualization is created to map the cases of heart attacks across the US. This visualization provides a geographic perspective on the distribution and frequency of heart attacks, offering additional insights into regional patterns and risk factors. Please visit this [Tableau Visualization](https://public.tableau.com/shared/67STXKFPH?:display_count=n&:origin=viz_share_link).


## Conclusion

This project demonstrates the use of logistic regression for heart disease risk prediction and highlights the importance of handling imbalanced data. Both SMOTE and undersampling techniques are explored to address class imbalance, and their impacts on the model's performance are analyzed. Additionally, the performance of models trained on different types of datasets is compared to identify the most informative features for heart disease risk prediction.
