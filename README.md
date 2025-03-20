# Credit Card Fraud Detection

## Overview
Credit card fraud detection is a critical task in the financial industry. This project aims to build a robust fraud detection system using machine learning techniques, including Logistic Regression, Random Forest, and XGBoost. The dataset used consists of anonymized credit card transactions, where the goal is to distinguish fraudulent transactions from legitimate ones.

## Dataset
The dataset contains transaction details with the following features:
- **V1 to V28**: Principal components obtained using PCA.
- **Amount**: Transaction amount.
- **Class**: Target variable (0 = Non-Fraudulent, 1 = Fraudulent).

The dataset is highly imbalanced, with fraudulent transactions making up a very small percentage of the data.

## Project Workflow
1. **Data Preprocessing**
   - Normalization of transaction amount.
   - Removal of unnecessary features (e.g., Time column).
   - Handling class imbalance using **ROSE (Random Over-Sampling Examples)**.

2. **Exploratory Data Analysis (EDA)**
   - Class distribution visualization.
   - Feature correlation analysis and heatmap.
   - Distribution of transaction amounts.

3. **Model Training**
   - **Logistic Regression**: Baseline model.
   - **Random Forest**: Captures complex interactions.
   - **XGBoost**: Gradient boosting for improved precision and recall.

4. **Evaluation Metrics**
   - Confusion Matrix (Accuracy, Precision, Recall, F1-score)
   - Precision-Recall (PR) Curve
   - Feature Importance Analysis

## Installation
To run this project, install the required R packages:
```r
install.packages(c("tidyverse", "data.table", "ggplot2", "caret", "ROSE", "PRROC", "xgboost", "randomForest", "e1071", "gridExtra", "patchwork"))
```

## Running the Project
1. Load the dataset:
   ```r
   data <- fread("creditcard.csv")
   ```
2. Preprocess the data and handle class imbalance.
3. Train models using Logistic Regression, Random Forest, and XGBoost.
4. Evaluate and compare model performances.
5. Visualize results (PR curves, feature importance, correlation heatmaps).

## Results & Insights
- **Logistic Regression** performs moderately but struggles with class imbalance.
- **Random Forest** improves performance by capturing non-linear relationships.
- **XGBoost** achieves the best results with the highest precision-recall score, making it the most effective for fraud detection.

## Authors
Aishwarya Anil Kumar

## License
This project is for educational purposes and is open-source under the MIT License.

