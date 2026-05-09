# 📊 Customer Churn Prediction and Customer Segmentation

This project analyzes and predicts customer churn using machine learning techniques. The goal is to identify customers at risk of leaving and provide actionable business insights to improve customer retention and reduce churn.

---

## 🚀 Project Overview

Customer churn is a critical problem in telecom businesses. Retaining existing customers is often more cost-effective than acquiring new ones.

In this project:
- Cleaned and preprocessed real-world telecom data
- Performed exploratory data analysis (EDA)
- Applied customer segmentation to understand behavioral patterns
- Built multiple machine learning models for churn prediction
- Evaluated models using key metrics
- Derived business insights for customer retention

---

## 📂 Dataset

This project uses the **Telco Customer Churn dataset** from Kaggle.

- - Source: [Telco Customer Churn Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

The dataset contains customer demographics, subscription details, and service usage information used to predict churn behavior.

---

## 👥 Customer Segmentation

K-Means clustering was used to segment customers based on behavior patterns.

### Features used:
- Tenure
- Monthly Charges
- Total Charges

### Why these features?
These variables represent customer loyalty, spending behavior, and overall value, making them suitable for grouping customers into meaningful segments.

### Outcome:
Customers were grouped into distinct segments such as:
- High-value loyal customers
- High-risk new customers
- Budget customers

---

## 🧠 Machine Learning Pipeline

- Data Cleaning (handling missing values, type conversion)
- Feature Engineering (encoding categorical variables)
- Feature Scaling (StandardScaler)
- Model Training:
  - Logistic Regression
  - Random Forest
  - XGBoost
- Model Evaluation:
  - Accuracy, Precision, Recall, F1-score
  - Confusion Matrix
- Feature Importance Analysis

---

## 📈 Model Performance

| Model               | Accuracy | Precision | Recall | F1-score |
|--------------------|----------|-----------|--------|----------|
| Logistic Regression| 82.19%   | 68.71%    | 60.05% | 64.09%   |
| Random Forest      | 79.35%   | 66.14%    | 45.04% | 53.59%   |
| XGBoost            | 79.13%   | 62.70%    | 52.28% | 57.02%   |

📍 Logistic Regression was selected as the final model based on better recall and overall balance.

---

## 🎯 Key Insights

- Customers with **fiber optic internet** are more likely to churn
- Customers with **long-term contracts (2-year)** are less likely to churn
- **High monthly charges** increase churn risk
- **Low tenure customers** are more likely to leave

---

## 💼 Business Recommendations

- Offer incentives for long-term contracts
- Provide targeted discounts for high-charge customers
- Focus retention strategies on new customers
- Improve service quality for fiber optic users

---

## 🛠️ Tech Stack

- Python
- pandas, NumPy
- seaborn, matplotlib
- scikit-learn
- XGBoost

---

## 🔄 How to Use the Saved Model

The final selected model (Logistic Regression) is saved as a `.pkl` file and can be reused without retraining.

### Load the model

```python
import pickle

model = pickle.load(open("models/churn_model.pkl", "rb"))

```

### ⚠️ Note
The input data must be preprocessed (encoded and scaled) in the same way as during training before making predictions. This ensures consistency and accurate results.

---

## 🔮 Future Improvements

- Hyperparameter tuning for better performance
- Deploy model using Streamlit
- Real-time churn prediction system

---

## 📌 Key Highlights

- Combined supervised learning (churn prediction) with unsupervised learning (clustering)
- Business-driven feature selection and interpretation
- End-to-end ML pipeline from data cleaning to insights

---

## 📄 License

Copyright (c) 2026 Tayrin Tunzina

This project is licensed under the MIT License.
