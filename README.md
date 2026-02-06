# Fraud Detection Analytics for Credit Card Transactions
### Machine Learning–Driven Risk Identification in Financial Data

## Project Overview
This project presents an end-to-end fraud detection analytics solution using machine learning to identify fraudulent credit card transactions in a highly imbalanced financial dataset. The analysis focuses on improving fraud detection sensitivity while reducing false positives to support effective financial risk mitigation.

---

## Problem Statement
Credit card fraud results in significant financial losses and operational inefficiencies. Traditional rule-based detection systems often fail to adapt to evolving fraud patterns and generate excessive false alerts.

**Objective:**
- Detect fraudulent transactions with high recall
- Minimize false positives
- Support data-driven decision-making for fraud investigation teams

---

## Dataset Description
- **Source:** Kaggle — Credit Card Fraud Detection Dataset  
  https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud
- **Total Transactions:** 284,807  
- **Fraud Cases:** 492 (approximately 0.17%)  
- **Primary Challenge:** Extreme class imbalance  

### Key Features
- `Time` – Time elapsed between transactions  
- `V1–V28` – Anonymized PCA-transformed features  
- `Amount` – Transaction amount  
- `Class` – Target variable (0 = Legitimate, 1 = Fraud)

---

## Tools and Technologies
- **Programming Language:** Python  
- **Data Analysis:** Pandas, NumPy  
- **Data Visualization:** Matplotlib, Seaborn  
- **Machine Learning:** Scikit-learn  
- **Development Environment:** Jupyter Notebook  

---

## Analytical Approach

### 1. Data Preparation
- Processed over 284,000 transaction records  
- Standardized numerical features to improve model performance  
- Validated data integrity and class distributions  

### 2. Exploratory Data Analysis (EDA)
- Analyzed transaction distributions and fraud frequency  
- Identified a 99.83% non-fraud and 0.17% fraud class imbalance  
- Evaluated limitations of accuracy as a primary evaluation metric  

### 3. Handling Class Imbalance
- Applied SMOTE (Synthetic Minority Oversampling Technique)  
- Increased minority class representation to improve fraud detection sensitivity  

### 4. Model Development
Developed and compared multiple classification models:
- Logistic Regression  
- Decision Tree Classifier  
- Random Forest Classifier  

### 5. Model Evaluation
Models were evaluated using:
- Precision, Recall, and F1-Score  
- ROC-AUC score  
- Confusion matrix  

Recall was prioritized to minimize missed fraudulent transactions.

---

## Model Performance Summary

The Random Forest classifier achieved the strongest trade-off between fraud detection and false alerts:

- Fraud Recall: High sensitivity to fraudulent transactions
- ROC-AUC: Strong class separability
- Precision: Maintained acceptable false alert rates
- Accuracy: >99% (reported for completeness, not used for optimization)

Threshold tuning was applied to improve recall for the fraud class.

#### Threshold Optimization

Instead of using the default probability threshold (0.5), decision thresholds were adjusted to improve fraud recall.

Lowering the threshold increased the detection of fraudulent transactions at the expense of additional false positives, reflecting a realistic fraud investigation trade-off.


---

## Key Insights

- Extreme class imbalance (0.17% fraud) renders accuracy an unreliable performance metric
- Recall-focused optimization significantly improved fraud detection coverage
- Ensemble models provided more stable predictions under imbalanced conditions
- Fraudulent transactions exhibit distinct patterns in PCA-transformed feature space
- Model outputs can be directly integrated into risk-scoring workflows for investigation teams

---

## Business Impact
- Enables early identification of high-risk transactions  
- Reduces manual review effort by lowering false positive alerts  
- Demonstrates a scalable analytics approach for financial risk teams  
- Provides a data-driven alternative to static fraud detection rules  

---

## Limitations and Assumptions

- The dataset uses PCA-transformed features, limiting direct business interpretability
- SMOTE may introduce synthetic patterns not present in real fraud behavior
- Temporal transaction patterns were not modeled
- Dataset represents historical data and may not reflect evolving fraud strategies

Future improvements include cost-based optimization, temporal modeling, and real-time scoring simulations.
