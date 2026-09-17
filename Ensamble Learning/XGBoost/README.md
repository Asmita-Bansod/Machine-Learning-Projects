# 📱 Mobile Price Range Prediction using XGBoost

## 📌 Project Overview

This project uses **Machine Learning and XGBoost** to predict the **price range of a mobile phone** based on its technical specifications.

## 🎯 Problem Statement

To build a classification model that predicts the appropriate **mobile price range** based on features such as RAM, battery power, internal memory, camera specifications, screen resolution, and other mobile characteristics.

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost
* Jupyter Notebook

## 🔄 Project Workflow

1. Data Collection
2. Data Cleaning
3. Exploratory Data Analysis (EDA)
4. Feature Selection
5. Train-Test Split
6. Feature Scaling (where required)
7. XGBoost Model Building
8. Hyperparameter Tuning using `RandomizedSearchCV`
9. Model Evaluation
10. Final Prediction

## 🤖 Machine Learning Algorithm

**XGBoost Classifier**

XGBoost is a gradient boosting algorithm that builds decision trees sequentially, where each new tree attempts to improve the errors made by previous trees.

### Hyperparameter Tuning

The following parameters were tuned:

* `n_estimators`
* `max_depth`
* `learning_rate`
* `subsample`
* `colsample_bytree`
* `min_child_weight`
* `gamma`

## 📊 Model Performance

* **Training Accuracy:** 100%
* **Testing Accuracy:** 92.5%

The model performs well on unseen test data, although the difference between training and testing accuracy indicates that overfitting should be monitored.

## 📁 Project Structure

```text
Mobile-Price-Range-XGBoost/
│
├── Mobile_price_range.csv
├── Mobile_Price_Range_XGBoost.ipynb
├── README.md
└── requirements.txt
```

## 🚀 Future Improvements

* Perform more extensive hyperparameter tuning
* Evaluate Precision, Recall, F1-score and ROC-AUC
* Perform cross-validation
* Deploy the model using Streamlit

## 👩‍💻 Author

**Asmita Bansod**
