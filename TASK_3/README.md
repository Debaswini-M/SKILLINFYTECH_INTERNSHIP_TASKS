# 🎓 Student Performance Prediction System

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Regression-orange.svg)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen.svg)

---

## 📌 Project Overview

This project implements a Machine Learning regression model to predict a student’s final academic grade (G3) using academic, demographic, and lifestyle factors.

The system follows a complete end-to-end ML workflow — from data preprocessing and feature engineering to model evaluation and prediction.

The objective is to apply supervised learning techniques to real-world education data and evaluate model performance using regression metrics such as MAE and RMSE.

---

## 🎯 Assignment Objective

- Collect and preprocess student academic and social data  
- Train a regression model (Linear Regression)  
- Evaluate performance using MAE and RMSE  
- Provide a prediction function for new student data  
- Apply an end-to-end machine learning pipeline  

---

## 📊 Dataset Information

**Source:**  [UCI Machine Learning Repository – Student Performance Dataset](https://example.com/url-goes-here)


Files used:
- `student-mat.csv` (Math students)
- `student-por.csv` (Portuguese students)

Both datasets were merged into a single dataset for better generalization.

### Dataset Summary

- Total Students: **1044**
- Total Features: 33 original columns
- Target Variable: `G3` (Final Grade)
- Grade Range: 0 – 20

---

## 🔍 Feature Categories

### Academic Factors
- studytime
- failures
- absences
- G1 (First Period Grade)
- G2 (Second Period Grade)

### Family & Background
- Medu (Mother’s education)
- Fedu (Father’s education)
- guardian
- famsup
- Pstatus

### Lifestyle & Behavior
- goout
- Dalc (weekday alcohol consumption)
- Walc (weekend alcohol consumption)
- health
- freetime
- romantic

---

## 🛠 Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## ⚙️ Machine Learning Workflow

1. Data Loading (`sep=";"` used for correct parsing)
2. Dataset Merging (Math + Portuguese)
3. Categorical Encoding (One-Hot Encoding)
4. Feature Scaling (StandardScaler)
5. Train-Test Split (80/20)
6. Model Training (Linear Regression)
7. Model Evaluation
8. Visualization (Actual vs Predicted)
9. Prediction Function Implementation

---

## 🧠 Model Implementation

Categorical features were converted using one-hot encoding.  
Numerical features were scaled using StandardScaler.

---

## 📈 Model Performance

### Linear Regression Results

- **MAE:** 1.02  
- **MSE:** 3.10  
- **RMSE:** 1.76  
- **R² Score:** 0.80  

---

## 📊 Performance Interpretation

- The model predicts final grades within approximately **±1 grade point** on average.
- RMSE of 1.76 indicates strong predictive precision.
- R² score of 0.80 shows that 80% of grade variance is explained by the model.
- Including G1 and G2 significantly improves performance due to strong sequential academic correlation.

---

## 📊 Visualization

An Actual vs Predicted scatter plot was generated.

Observations:
- Most points lie close to the ideal diagonal line.
- Strong linear relationship between predicted and actual grades.
- Slight overestimation for very low-performing students (G3 = 0 cases).

This confirms a good regression fit and reliable predictive behavior.

---

## 🔎 Feature Insights

Strong Predictors:
- G2
- G1
- failures (negative impact)
- studytime

Moderate Influence:
- absences
- parental education
- lifestyle behaviors

Key Insight:
Sequential academic performance is the most influential factor in predicting final grades.

---

## 👨‍💻 Author
**Debaswini-M**

---

