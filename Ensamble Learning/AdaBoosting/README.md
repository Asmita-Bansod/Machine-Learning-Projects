# AdaBoost Classification – Play Tennis Prediction

## 📌 Project Overview

This project uses **AdaBoost Classification** to predict whether a person should **Play Tennis (Yes/No)** based on weather conditions.

### Problem Statement

Predict the target variable using:

* Outlook
* Temperature
* Humidity
* Wind

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

## 🔄 Project Workflow

1. Data loading and understanding
2. Exploratory Data Analysis (EDA)
3. Missing value treatment using **SimpleImputer**
4. Categorical data encoding
5. Feature and target selection
6. Train-test split
7. AdaBoost model training
8. Hyperparameter tuning using **GridSearchCV**
9. Model evaluation

## 🤖 Model

**AdaBoost Classifier** with a **Decision Tree** as the base estimator.

Best parameters:

* `n_estimators = 50`
* `learning_rate = 0.1`
* `max_depth = 3`
* Cross-validation = 5-fold

## 📊 Results

The final tuned model achieved:

* **Training Accuracy:** 91.25%
* **Testing Accuracy:** 97.5%
* **Macro F1-Score:** 0.97

### Classification Performance

| Class | Precision | Recall | F1-Score |
| ----- | --------: | -----: | -------: |
| 0     |      1.00 |   0.94 |     0.97 |
| 1     |      0.96 |   1.00 |     0.98 |

## ✅ Conclusion

AdaBoost provided strong performance for predicting whether tennis should be played based on weather conditions. Hyperparameter tuning with GridSearchCV improved the observed test accuracy from **95% to 97.5%**.

## 📁 Project Structure

```text
├── Adaboost.ipynb
├── playtennis.csv
└── README.md
```

## 👩‍💻 Author

**Asmita Bansod**
