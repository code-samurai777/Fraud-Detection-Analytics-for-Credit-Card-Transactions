# 🔍 Fraud Detection Analytics for Credit Card Transactions  
### Machine Learning–Driven Risk Identification in Financial Data

## 📌 Project Overview
This project applies **data analytics and machine learning techniques** to identify fraudulent credit card transactions within a highly imbalanced financial dataset. The objective is to support **risk mitigation and fraud prevention** by accurately distinguishing fraudulent activity from legitimate transactions.

The project demonstrates an end-to-end analytical workflow, from data exploration and preprocessing to model evaluation and business insight generation.

---

## 🎯 Business Problem
Credit card fraud causes significant financial losses and operational inefficiencies. Traditional rule-based systems often fail to adapt to evolving fraud patterns and generate high false-positive rates.

**Goal:**  
Develop a predictive analytics solution to:
- Detect fraudulent transactions with high recall
- Minimize false positives
- Support decision-making for fraud investigation teams

---

## 📊 Dataset Description
- **Source:** Kaggle – Credit Card Fraud Detection dataset  
- **Total Transactions:** 284,807  
- **Fraudulent Transactions:** 492 (~0.17%)  
- **Challenge:** Extremely imbalanced dataset  

### Key Features
- `Time` – Time elapsed between transactions  
- `V1–V28` – Anonymized features (PCA transformed)  
- `Amount` – Transaction amount  
- `Class` – Target variable (0 = Legitimate, 1 = Fraud)

---

## 🛠 Tools & Technologies
- **Programming Language:** Python  
- **Data Analysis:** Pandas, NumPy  
- **Data Visualization:** Matplotlib, Seaborn  
- **Machine Learning:** Scikit-learn  
- **Environment:** Jupyter Notebook

---

## 🧱 Analytical Approach

### 1️⃣ Data Cleaning & Preparation
- Loaded and validated transaction data  
- Checked for missing values and data consistency  
- Scaled numerical features for model compatibility

### 2️⃣ Exploratory Data Analysis (EDA)
- Analyzed transaction distribution and fraud frequency  
- Visualized class imbalance and transaction patterns  
- Identified challenges posed by skewed data

### 3️⃣ Handling Class Imbalance
- Applied **SMOTE (Synthetic Minority Oversampling Technique)**  
- Evaluated sampling strategies to improve fraud detection performance

### 4️⃣ Model Development
Trained and evaluated multiple classification models:
- Logistic Regression  
- Decision Tree Classifier  
- Random Forest Classifier  

### 5️⃣ Model Evaluation
Models were assessed using:
- Precision, Recall, F1-Score  
- ROC-AUC Score  
- Confusion Matrix  

Priority was given to **recall and balanced performance**, critical for fraud detection scenarios.

---

## 📈 Key Insights
- Class imbalance significantly impacts model performance if not addressed  
- Oversampling techniques improved fraud detection recall  
- Ensemble models (Random Forest) delivered more stable results  
- Visual analytics helped interpret model behavior for non-technical stakeholders

---

## 💡 Business Value
- Demonstrates how analytics can reduce financial risk  
- Improves fraud detection accuracy compared to basic rules  
- Highlights trade-offs between detection sensitivity and false alarms  
- Provides a scalable framework for real-world fraud analysis

---

## ▶️ How to Run the Project
1. Clone the repository  
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
