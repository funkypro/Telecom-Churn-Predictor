# 📊 Telecom Customer Churn Predictor

## 📋 Project Overview
This project aims to predict customer attrition (Churn) for a telecommunications company. By identifying high-risk customers, the business can proactively offer incentives to improve retention rates.

## 🛠️ The Data Stack
* **Language:** Python
* **Environment:** @Google Colab
* **Libraries:** Pandas, Scikit-Learn, Seaborn, Matplotlib

## 🧹 Engineering Highlights
* **Data Cleaning:** Converted `TotalCharges` from string to numeric and handled missing values via median imputation.
* **Feature Engineering:** Dropped irrelevant identifiers (`customerID`) and implemented **One-Hot Encoding** for categorical variables to make them machine-readable.
* **Data Splitting:** Utilized an 80/20 Train-Test split to ensure unbiased evaluation.

## 📈 Initial Performance (Single Decision Tree)
| Metric | Score |
| :--- | :--- |
| **Accuracy** | 80.62% |
| **Recall (Churners)** | 46% |
| **Precision (Churners)** | 70% |

> **Critical Analysis:** While the 80% accuracy looks strong, the **Recall** of 46% indicates the model is missing over half of the actual churners. This is a classic "Class Imbalance" problem where the model leans toward the majority class (Loyal Customers).

## Implemented Random Forest to fix the recall
| Metric | Score |
| :--- | :--- |
| **Accuracy** | 79.91% |
| **Recall (Churners)** | 47% |
| **Precision (Churners)** | 67% |
Insight: Despite moving from a Single Decision Tree to an Ensemble Random Forest, Churn Recall remained capped at ~47%. This suggests that "Churn" behavior in this dataset may be driven by factors not captured in the current features (e.g., customer service satisfaction scores or competitor pricing).
