nternet Usage Clustering Analysis

Project Overview

This project analyzes Internet usage across countries from 2000 to 2023 and applies unsupervised machine learning to identify groups of countries with similar Internet-usage patterns.

The project focuses on data preprocessing, exploratory analysis, feature scaling, DBSCAN clustering, selection of the eps parameter using a k-distance approach, and evaluation using the Silhouette Score.

Note: The notebook's original problem statement mentions predicting future Internet usage, but the implemented machine-learning workflow is primarily a clustering problem using DBSCAN. No supervised prediction model is implemented in the notebook.

Problem Statement

Analyze the growth and adoption of Internet usage across different countries from 2000 to 2023, identify countries with similar Internet-usage patterns, and use clustering techniques to discover meaningful groups based on historical Internet penetration.

Dataset

The dataset contains country-level Internet usage information.

Dataset dimensions

Rows: 217

Columns: 26

Country columns: Country Name, Country Code

Year columns: 2000–2023

Technologies Used

Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn

StandardScaler

DBSCAN

NearestNeighbors

silhouette_score

Project Workflow

Raw Dataset
     |
     v
Data Understanding
     |
     v
Missing Value Identification
     |
     v
Missing Value Handling
     |
     v
Remove Unnecessary Columns
     |
     v
Convert Numeric Columns
     |
     v
Create Feature Matrix
     |
     v
StandardScaler
     |
     v
Initial DBSCAN
     |
     v
Silhouette Evaluation
     |
     v
K-Distance Analysis
     |
     v
DBSCAN Hyperparameter Tuning
     |
     v
Final DBSCAN Model
     |
     v
Final Silhouette Evaluation

Key Findings

The dataset contains 217 countries and 26 columns.

Internet-usage observations are available for years 2000–2023.

The dataset contains missing values represented by values such as ...

The 2023 column has a particularly large amount of missing data and was removed from the clustering analysis.

Historical numeric features from 2000–2022 were used for clustering.

StandardScaler was applied before DBSCAN.

Default DBSCAN produced a Silhouette Score of approximately -0.038.

DBSCAN hyperparameters were tuned using k-distance analysis.

The selected parameters were:

eps = 2.5

min_samples = 24

The tuned model achieved a Silhouette Score of approximately 0.399.

The tuned model provides a substantial improvement over the initial DBSCAN configuration.

Conclusion

This project demonstrates an end-to-end unsupervised machine learning workflow for grouping countries based on historical Internet-usage patterns.

The initial DBSCAN configuration produced a negative Silhouette Score of approximately -0.038, indicating poor clustering. After analyzing neighborhood distances and tuning DBSCAN's eps and min_samples parameters, the Silhouette Score improved to approximately 0.399.

Therefore, the tuned DBSCAN model provides a meaningful improvement over the initial model, although the resulting clustering should still be validated using noise percentage, cluster sizes, visualization, and domain interpretation before considering it a final production-quality clustering solution.

Author

Asmita Bansod

Data Science / Machine Learning Project