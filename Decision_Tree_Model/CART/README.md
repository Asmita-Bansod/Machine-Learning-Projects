# Loan Approval Prediction – CART Decision Tree

## 📌 Project Overview
This project predicts whether a loan application should be **Approved or Rejected** using applicant and loan-related information.

## 🎯 Objective
Build a **CART (Classification and Regression Trees) Decision Tree** classification model for loan approval prediction.

## 🛠️ Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## 🔄 Project Workflow
1. Data Loading
2. Data Cleaning & EDA
3. Outlier Detection
4. Categorical Encoding
5. Train-Test Split
6. Decision Tree Model Building
7. Overfitting Detection
8. Hyperparameter Tuning using GridSearchCV
9. Pre-Pruning
10. Post-Pruning using Cost Complexity Pruning (CCP)

## 🤖 Model
**Decision Tree Classifier (CART)**

- Criterion: `Gini`
- Pre-pruning:
  - `max_depth = 5`
  - `min_samples_split = 3`
- Post-pruning:
  - `ccp_alpha = 0.002449568834889938`

## 📊 Evaluation
Model performance was evaluated using:
- Training Accuracy
- Testing Accuracy
- Confusion Matrix
- Classification Report

## 💡 Conclusion
The initial Decision Tree showed signs of **overfitting**. Pre-pruning and post-pruning were applied to control tree complexity and improve model generalization.
