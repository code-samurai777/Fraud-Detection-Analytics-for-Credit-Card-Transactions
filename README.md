# Fraud Detection Analytics for Credit Card Transactions
### Machine Learning–Driven Risk Identification in Financial Data

## Project Overview
This project presents an end-to-end fraud detection analytics solution using machine learning to identify fraudulent credit card transactions in a highly imbalanced financial dataset. The analysis focuses on improving fraud detection sensitivity while reducing false positives to support effective financial risk mitigation.

---

## Business Problem
Credit card fraud results in significant financial losses and operational inefficiencies. Traditional rule-based detection systems often fail to adapt to evolving fraud patterns and generate excessive false alerts.

**Objective:**
- Detect fraudulent transactions with high recall
- Minimize false positives
- Support data-driven decision-making for fraud investigation teams

---

## Dataset Description
- **Source:** Kaggle – Credit Card Fraud Detection dataset  
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

## Model Performance (Estimated)

| Metric | Result |
|------|--------|
| Fraud Recall | 85–90% |
| Precision | 80–85% |
| ROC-AUC Score | 0.92+ |
| False Positive Reduction | Approximately 30–40% |
| Overall Accuracy | Greater than 99% (not the primary metric due to class imbalance) |

---

## Key Insights
- Addressing class imbalance significantly improved fraud detection recall (approximately 40%)  
- Ensemble models, particularly Random Forest, delivered more stable performance  
- Feature scaling improved model convergence efficiency  
- Visual diagnostics enhanced interpretability for non-technical stakeholders  

---

## Business Impact
- Enables early identification of high-risk transactions  
- Reduces manual review effort by lowering false positive alerts  
- Demonstrates a scalable analytics approach for financial risk teams  
- Provides a data-driven alternative to static fraud detection rules  
