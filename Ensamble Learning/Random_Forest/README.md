# Air Quality Ventilation Prediction

## 📌 Project Overview

A Machine Learning project that analyzes classroom occupancy and environmental conditions to predict the **ventilation decision** for maintaining healthy indoor air quality.

## 🎯 Problem Statement

Develop a machine learning-based ventilation decision system using classroom occupancy and environmental conditions to predict whether ventilation is required.

## 🔍 Project Workflow

* Data Loading & Understanding
* Exploratory Data Analysis (EDA)
* Missing Value & Duplicate Check
* Feature Selection
* Categorical Encoding
* Train-Test Split
* Random Forest Model Training
* Model Evaluation

## 📊 Dataset

* **Rows:** 500
* **Columns:** 10
* **Target:** `ventilation_decision`
* **Classes:** IDLE, MONITOR
* Key features include CO₂, PM2.5, temperature, humidity, student count and school period.

## 🤖 Model Used

**Random Forest Classifier**

Selected features include CO₂, PM2.5, humidity, student count, temperature and selected school-period features.

## 📈 Results

* Training Accuracy: **100%**
* Testing Accuracy: **100%**
* Precision: **100%**
* Recall: **100%**
* F1-Score: **100%**
* Confusion Matrix: **67 TN, 33 TP, 0 errors**

## 🛠️ Technologies

Python • Pandas • NumPy • Matplotlib • Seaborn • Scikit-learn • Jupyter Notebook

## ✅ Conclusion

The Random Forest model achieved **100% test accuracy** with no false positives or false negatives on this dataset.
