# 🏠 House Price Prediction using Random Forest & XGBoost

## 📌 Project Overview

This project builds an end-to-end supervised machine learning regression model to predict residential house prices using the Ames Housing dataset from Kaggle.

The goal is to accurately predict **SalePrice** based on 79 structured features such as construction quality, living area, basement size, garage capacity, and neighborhood.

This project demonstrates:

- Structured preprocessing pipeline  
- Feature relevance analysis using Mutual Information  
- Cross-model feature importance comparison  
- Dimensionality reduction using zero-importance filtering  
- Hyperparameter optimization with GridSearchCV  

---

## 📊 Dataset

- Source: Ames Housing Dataset (Kaggle)
- Target Variable: `SalePrice`
- 79 explanatory features

---

## 🔍 Machine Learning Pipeline

### 1️⃣ Data Preprocessing
- Removed ID column
- Separated numerical and categorical features
- Missing value treatment:
  - Numerical → Mean Imputation
  - Categorical → Most Frequent Imputation
- Applied OneHotEncoding using ColumnTransformer

---

### 2️⃣ Feature Selection

- Applied Mutual Information Regression
- Extracted feature importance from Random Forest & XGBoost
- Removed zero-importance features
- Reduced dimensionality while maintaining performance

---

### 3️⃣ Model Comparison

#### Random Forest Regressor
- n_estimators = 200
- RMSE ≈ 33,107

#### XGBoost Regressor
- Initial RMSE ≈ 32,003
- Observed overfitting before tuning

---

### 4️⃣ Hyperparameter Tuning

Used GridSearchCV (3-fold cross-validation)

Parameters tuned:
- n_estimators
- max_depth
- learning_rate

---

## 📈 Final Performance

Final Optimized XGBoost Model:

**RMSE ≈ 27,839**

Improvement achieved through:
- Feature elimination
- Model complexity control
- Cross-validated optimization

---

## 🛠 Tech Stack

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- XGBoost  

---

## 📂 Project File

House_Price_Prediction_XG.ipynb

---

## 📌 Author

Yadukrishnan  
Aspiring Data Scientist | ML & AI Enthusiast

