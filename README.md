# Task 1: Data Cleaning & Preprocessing (Titanic Dataset)

This repository contains my solution for Task 1, focusing on cleaning and preparing the Titanic dataset for machine learning.

### What did I do?

The goal was to transform the raw data by following standard ML preprocessing steps:

### Data Loading & Exploration

I loaded the Titanic dataset and checked the initial data types and missing values using .isna().sum().

### Missing Value Imputation

- Dropped 2 rows that were missing Embarked data.
- Imputed missing Age values using the median after observing a slight positive skew.
- Dropped the Cabin column due to excessive missing data (around 77%).

### Categorical Encoding

- One-hot encoded the Embarked column manually into S and C binary features.
- Used label encoding for Sex to create a Gender feature (Male=1, Female=0).

### Feature Scaling & Outlier Handling

- Applied log transformation to Fare to handle skewness, which I confirmed with a boxplot.
- Normalized Age and the transformed Fare using StandardScaler.
- Detected and removed outliers from Age and Fare using the IQR method (1.5*IQR rule).

### Tools Used

Python
Pandas
NumPy
Scikit-learn
Matplotlib & Seaborn
