# Customer Churn Analysis & Prediction

## Overview

This project focuses on analyzing customer churn behavior in a telecom company and building machine learning models to predict whether a customer is likely to leave the service.

The project combines:

* Exploratory Data Analysis (EDA)
* Churn Reason Analysis
* Data Preprocessing
* Feature Engineering
* Machine Learning Classification
* Model Performance Evaluation

The objective is to help businesses identify at-risk customers and improve customer retention strategies.

---

## Business Problem

Customer churn is one of the biggest challenges faced by subscription-based businesses. Acquiring a new customer is significantly more expensive than retaining an existing one.

This project aims to:

* Identify key factors responsible for customer churn.
* Analyze customer behavior patterns.
* Predict customers who are likely to churn.
* Support data-driven retention strategies.

---

## Dataset Information

The dataset contains telecom customer information including:

* Customer demographics
* Subscription details
* Internet services
* Payment methods
* Revenue information
* Churn categories and churn reasons

### Target Variable

**Customer_Status**

Classes:

* Stayed
* Joined
* Churned

For machine learning, the target variable is transformed into:

| Value | Meaning         |
| ----- | --------------- |
| 0     | Stayed / Joined |
| 1     | Churned         |

---

## Project Workflow

### 1. Data Cleaning

The following columns were removed because they either contain identifiers or information unavailable before churn occurs:

* Customer_ID
* Churn_Category
* Churn_Reason

---

### 2. Target Variable Creation

A new binary column named **Churn** was created:

```python
1 = Churned
0 = Stayed or Joined
```

---

### 3. Exploratory Data Analysis (EDA)

The project includes:

* Churn distribution analysis
* Churn category analysis
* Customer behavior exploration
* Correlation analysis

Visualization libraries used:

* Matplotlib
* Seaborn

---

### 4. Missing Value Treatment

Missing values were handled using:

* "No" for categorical features
* 0 for numerical features

---

### 5. Feature Encoding

Categorical variables were transformed into numerical format using:

```python
LabelEncoder
```

---

### 6. Correlation Analysis

A heatmap was generated to understand relationships among variables and identify features strongly associated with churn.

---

### 7. Train-Test Split

The dataset was divided into:

* Training Set: 80%
* Testing Set: 20%

Using:

```python
train_test_split()
```

with stratified sampling.

---

## Machine Learning Models

### Logistic Regression

A baseline classification model used for churn prediction.

### Random Forest Classifier

An ensemble learning method that improves prediction performance through multiple decision trees.

### XGBoost Classifier

A gradient boosting model known for high predictive accuracy and efficiency.

---

## Model Evaluation Metrics

The models were evaluated using:

* Accuracy Score
* Classification Report
* Precision
* Recall
* F1-Score
* Confusion Matrix

---

## Technologies Used

### Programming Language

* Python

### Libraries

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* XGBoost

---

## Project Structure

```text
Customer-Churn-Analysis/
│
├── Customer_Data.csv
├── codes.ipynb
├── README.md
│
├── Data Cleaning
├── Exploratory Data Analysis
├── Feature Engineering
├── Machine Learning Models
│   ├── Logistic Regression
│   ├── Random Forest
│   └── XGBoost
│
└── Model Evaluation
```

---

## Key Outcomes

* Identified major factors contributing to customer churn.
* Performed churn category analysis.
* Built multiple machine learning models for churn prediction.
* Compared model performance using standard evaluation metrics.
* Generated actionable business insights for customer retention.

---

## Future Improvements

* Hyperparameter tuning using GridSearchCV.
* Feature selection techniques.
* SMOTE for class imbalance handling.
* Deployment using Flask or Streamlit.
* Interactive Power BI dashboard integration.
* Deep Learning-based churn prediction models.

---

## Author

**Randhir Kumar**

B.Tech – Metallurgical & Materials Science Engineering

Interested in:

* Data Analytics
* Machine Learning
* Deep Learning
* Business Analytics
