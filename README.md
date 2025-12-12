# 🛒 Supermarket Sales – Customer Satisfaction Prediction  
### Business Analytics | Predictive Modeling | SAS

This project analyzes supermarket sales data to **predict customer satisfaction levels** and uncover key behavioral and transactional drivers that influence satisfaction outcomes.

The analysis focuses on distinguishing **satisfied vs. unsatisfied customers** using statistical modeling and machine learning techniques implemented in **SAS**.

---

## 🎯 Objective

- Predict customer satisfaction (Low vs. High)
- Identify key drivers of satisfaction
- Compare multiple classification models
- Provide actionable business insights for marketing and operations

---

## 📊 Dataset

- Source: Kaggle – Supermarket Sales Dataset  
- Records: 1,000 transactions  
- Target Variable: **Rating**
  - 0 → Unsatisfied (Rating ≤ 7)
  - 1 → Satisfied (Rating > 7)

### Key Features
- Customer Type (Member / Normal)
- Gender
- Product Line
- Unit Price
- Quantity
- Tax
- Total
- Gross Income
- Date & Time
- Payment Method

Dataset available in `/data`.

---

## 🔍 Exploratory Data Analysis

- Right-skewed distributions for **Gross Income** and **Tax**
- Strong linear relationship between **Total** and:
  - Unit Price
  - Quantity
  - Tax
  - Gross Income
- Members generate slightly higher revenue than non-members
- Female customers show marginally higher average spend

EDA visuals and summaries are documented in the project report.

---

## 📐 Principal Component Analysis (PCA)

- PCA performed using **correlation matrix** (variables in different units)
- Variance explained:
  - PC1: 61%
  - PC2: 13%
  - First 3 PCs: **86% total variance**
- Key contributors:
  - PC1: Tax, Total, COGS, Gross Income
  - PC2: Date, Time
  - PC3: Quantity

---

## 🤖 Predictive Models (SAS)

The dataset was split **80% training / 20% validation**.

### Models Evaluated
- Logistic Regression
- CART (Gini & Entropy)
- Neural Networks
- Discriminant Analysis

---

### 📌 Model Performance Summary

| Model | Key Observation |
|-----|----------------|
| Logistic Regression | Low predictive power (AUC ≈ 0.56) |
| CART | Strong training performance but overfitting |
| Neural Networks | Improved specificity, moderate overall performance |
| Discriminant Analysis | High specificity, low sensitivity |

**Best Tradeoff Model:** CART (with caution due to overfitting)

---

## 📈 Business Insights

- **Date & Time** are strong predictors of satisfaction
- Total transaction value is a proxy for multiple correlated variables
- Customer satisfaction patterns can inform:
  - Targeted promotions
  - Staffing during peak hours
  - Inventory planning

---

## ⚠️ Limitations

- Dataset size is relatively small
- Data is from 2019 (limited temporal relevance)
- Satisfaction ratings may contain subjective bias

---

## 🚀 Future Improvements

- Expand dataset with recent transactions
- Include customer reviews and feedback
- Apply modern ML models in Python for comparison
- Cross-validation to reduce overfitting

---

## 🛠 Tools Used

- **SAS** (Logistic Regression, CART, Neural Networks, PCA)
- Excel
- Statistical Analysis & Visualization

---

## 👩‍💻 Author

**Vishaka Sharma**  
Business Analytics | Data Science | Predictive Modeling
