# Wine Customer Segment Prediction using Gradient Boosting

## 📌 Project Overview

This project uses **Machine Learning and Gradient Boosting Classification** to predict the customer/wine segment based on the chemical properties of wine.

## 🎯 Problem Statement

Build a multiclass classification model that can accurately classify wine samples into **Customer Segment 1, 2, or 3** using their chemical characteristics.

## 📊 Dataset

* Rows: **178**
* Columns: **14**
* Input Features: **13 numerical chemical properties**
* Target: `Customer_Segment`
* Classes: **1, 2, 3**

## 🔧 Project Workflow

1. Data Loading & Understanding
2. Exploratory Data Analysis (EDA)
3. Data Quality Checks
4. Train-Test Split
5. Gradient Boosting Model
6. Hyperparameter Tuning using **GridSearchCV**
7. Model Evaluation
8. Feature Importance Analysis

**Encoding:** Not required because all input features are numerical.

## 🤖 Model

**Gradient Boosting Classifier**

Hyperparameter tuning was performed using GridSearchCV to identify the best model configuration.

## 📈 Results

* **Test Accuracy:** 94.44%
* **Macro F1-Score:** ~0.94
* Only **2 out of 36** test samples were misclassified.

## ✅ Conclusion

The Gradient Boosting model performed well in predicting the three wine/customer segments. The results show that the chemical properties contain useful information for distinguishing between the segments.

Since the dataset is relatively small, **cross-validation and multiple train-test splits** are recommended for more reliable performance estimation.

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook
