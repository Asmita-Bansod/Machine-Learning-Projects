# 🌆 City Lifestyle & Happiness Analysis using Hierarchical Clustering

## 📌 Project Overview

This project analyzes different **city lifestyle factors** such as average income, rent, population density, internet penetration, air quality, public transport, and green spaces to understand how cities differ in terms of their lifestyle and happiness.

The main objective is to identify **similar groups of cities using Hierarchical Clustering** and understand the characteristics of each cluster.

---

## 🎯 Problem Statement

Analyze city lifestyle factors such as:

* Average income
* Average rent
* Population density
* Internet penetration
* Air quality
* Public transport
* Green space

The project aims to:

1. Identify the factors associated with differences in `happiness_score`.
2. Understand whether income and living costs influence residents' happiness.
3. Group cities with similar lifestyle characteristics using hierarchical clustering.

---

## 📊 Dataset

The dataset contains **300 records and 10 columns**.

### Dataset Features

| Feature                  | Description                        |
| ------------------------ | ---------------------------------- |
| `city_name`              | Name of the city                   |
| `country`                | Country/region information         |
| `population_density`     | Population density of the city     |
| `avg_income`             | Average income                     |
| `internet_penetration`   | Percentage of internet penetration |
| `avg_rent`               | Average rent                       |
| `air_quality_index`      | Air quality index                  |
| `public_transport_score` | Public transport score             |
| `happiness_score`        | Happiness score                    |
| `green_space_ratio`      | Percentage/ratio of green space    |

The dataset contains 300 non-null observations for each column.

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* SciPy
* Jupyter Notebook

### Machine Learning Technique

**Hierarchical Agglomerative Clustering**

---

## 🔄 Project Workflow

```text
Dataset
   ↓
Data Understanding
   ↓
Data Cleaning
   ↓
Duplicate & Missing Value Check
   ↓
Outlier Detection
   ↓
Categorical Encoding
   ↓
Feature Selection
   ↓
Feature Scaling
   ↓
Dendrogram
   ↓
Hierarchical Clustering
   ↓
Cluster Evaluation
   ↓
Cluster Profiling
   ↓
Business Insights
```

---

## 🧹 Data Cleaning

The following data-cleaning steps were performed:

### Missing Value Check

```python
df.isna().sum()
```

The dataset did not contain missing values.

### Handling Invalid Values

Potential invalid values such as:

```text
?
empty
space
#
-
```

were replaced with `NaN`.

### Duplicate Check

```python
df.duplicated().sum()
```

No duplicate records were identified.

---

## 🔎 Exploratory Data Analysis

`describe()` was used to understand the statistical distribution of the numerical variables.

Some important dataset averages were:

| Feature                |    Mean |
| ---------------------- | ------: |
| Population Density     | 3944.84 |
| Average Income         | 2827.20 |
| Internet Penetration   |   74.31 |
| Average Rent           | 1002.77 |
| Air Quality Index      |   71.25 |
| Public Transport Score |   55.72 |
| Happiness Score        |    6.64 |
| Green Space Ratio      |   33.99 |

---

## ⚙️ Data Preprocessing

### 1. Removing City Name

`city_name` was removed because it is an identifier and does not provide a numerical distance that can directly be used by the clustering algorithm.

```python
x.drop(columns=['city_name'], inplace=True)
```

### 2. Encoding

The categorical `country` feature was converted into numerical form before clustering.

### 3. Feature Scaling

Standardization was performed using `StandardScaler`.

```python
from sklearn.preprocessing import StandardScaler

sc = StandardScaler()
x = sc.fit_transform(x)
```

Scaling is particularly important for clustering because clustering algorithms use distance calculations. Variables with larger numerical ranges could otherwise dominate the distance calculation.

---

## 🌳 Hierarchical Clustering

Hierarchical clustering was performed using the **agglomerative approach**.

A linkage matrix was created using the **complete linkage** method:

```python
from scipy.cluster import hierarchy

lk = hierarchy.linkage(x, method='complete')
```

A dendrogram was then used to visually analyze the hierarchical structure of the observations.

---

## 📌 Cluster Formation

Different numbers of clusters were explored.

For example:

```python
hc = AgglomerativeClustering(n_clusters=4)

labels = hc.fit_predict(x)
```

The resulting cluster labels were added back to the original dataframe:

```python
df['4 Clusters'] = labels
```

---

## 📈 Cluster Evaluation

The **Silhouette Score** was used to evaluate clustering quality.

```python
from sklearn.metrics import silhouette_score

silhouette_score(x, labels)
```

The notebook obtained a silhouette score of approximately:

```text
0.2686
```

A score around `0.27` indicates that the clusters have **some separation but are not strongly separated**.

---

## 📊 Cluster Profiles

The four-cluster analysis produced the following average profiles:

| Cluster   | Avg Income | Avg Rent | Happiness | Public Transport | Green Space |
| --------- | ---------: | -------: | --------: | ---------------: | ----------: |
| Cluster 0 |    2406.05 |   868.07 |      6.37 |            51.47 |       34.17 |
| Cluster 1 |    4117.20 |  1460.80 |  **8.43** |            62.78 |       36.80 |
| Cluster 2 |     882.22 |   301.94 |  **4.08** |            35.80 |       39.15 |
| Cluster 3 |    2607.80 |   898.40 |      5.54 |        **65.60** |       24.27 |

The notebook's cluster profiling shows that Cluster 1 has the highest average income and happiness score, while Cluster 2 has the lowest average income and happiness score.

---

## 💡 Key Insights

### Cluster 1 — Higher-Income / Higher-Happiness Cities

* Highest average income among the four clusters.
* Highest average happiness score.
* Higher internet penetration.
* Higher average rent.
* Relatively good public transport.

### Cluster 2 — Lower-Income / Lower-Happiness Cities

* Lowest average income.
* Lowest average rent.
* Lowest happiness score.
* Lower internet penetration.
* Lower public transport score.

### Cluster 3 — High-Density Cities

* Highest population density.
* Moderate income.
* Moderate happiness.
* Highest air quality index among the four clusters.
* Lowest green-space ratio.

### Cluster 0 — Moderate Lifestyle Cities

* Moderate income and rent.
* Moderate happiness.
* Moderate green-space availability.
* Average public transport score.

---

## 📉 Model Limitation

The silhouette score of approximately **0.2686** suggests that the identified clusters are not highly distinct.

Possible reasons include:

* Overlap between city lifestyle characteristics.
* Similar values across multiple features.
* Limited dataset size.
* Country information being represented numerically.
* Different lifestyle factors may not naturally form strongly separated groups.

Therefore, the clustering results should be considered **exploratory rather than definitive**.

---


## 📁 Project Structure

```text
City-Lifestyle-Happiness/
│
├── city_lifestyle_dataset.csv
├── City_Lifestyle_Hierarchical_Clustering.ipynb
├── README.md
│
└── images/
    ├── dendrogram.png
    └── cluster_visualization.png
```

---

## 🧠 Skills Demonstrated

* Python Programming
* Pandas Data Analysis
* NumPy
* Exploratory Data Analysis
* Data Cleaning
* Categorical Encoding
* Feature Scaling
* Hierarchical Clustering
* Dendrogram Analysis
* Agglomerative Clustering
* Silhouette Score
* Cluster Profiling
* Data Visualization
* Business Interpretation

---

## 📌 Conclusion

This project demonstrates how **unsupervised machine learning** can be used to group cities according to their lifestyle characteristics.

The hierarchical clustering approach identified groups with noticeably different profiles in terms of **income, rent, population density, internet penetration, transportation, air quality, green space, and happiness**.

However, the silhouette score of approximately **0.27** indicates that the clusters are only moderately separated. Further experimentation with clustering algorithms, preprocessing techniques, feature selection, and dimensionality reduction could improve the quality and interpretability of the segmentation.

---

## 👩‍💻 Author

**Asmita Bansod**
