# 📊 Bank Marketing Data Analysis

This project analyzes the `bankmarketing.csv` dataset to understand customer behavior in relation to a bank's marketing campaign. The primary goal is to explore the data, identify meaningful patterns, and set the foundation for predictive modeling — specifically, whether a customer subscribes to a term deposit.

---

## 📁 Dataset Overview

* **File**: `bankmarketing.csv`
* **Size**: 41,188 entries × 21 features
* **Target Variable**: `y` (whether the client subscribed to a term deposit: `yes`/`no`)

### 🔍 Key Features

* `age`, `job`, `marital`, `education`: Customer demographics
* `default`, `housing`, `loan`: Financial indicators
* `contact`, `month`, `day_of_week`: Contact details
* `duration`, `campaign`, `pdays`, `previous`: Marketing information
* `emp.var.rate`, `cons.price.idx`, `euribor3m`: Economic indicators

---

## 🧹 Data Inspection

* **No missing values** detected across any columns.
* **Descriptive statistics** calculated for numerical variables.
* **Data types** identified (categorical vs numerical).

---

## 📈 Data Visualization

### 🔦 Univariate and Bivariate Analysis

* **Line Plot**: `euribor3m` trend across the dataset index.
* **Box Plot**: Age distribution grouped by subscription outcome (`y`).
* **Histogram**: Age distribution with KDE overlay.
* **Bar Plot**: Distribution of job titles among clients.
* **Pair Plot**: Multivariate relationships between selected numerical features.
* **Heatmap**: Correlation matrix of numerical variables for pattern detection.

---

## ⚠️ Observations

* The dataset is **imbalanced**, with significantly more `no` responses than `yes`.
* `euribor3m` and `nr.employed` show strong correlations with other variables.
* `duration` is a key variable but should be handled carefully in modeling as it is campaign-specific.

---

## ✅ Next Steps

* Encode categorical variables for ML models.
* Handle class imbalance using techniques like **SMOTE**, **class weights**, or **undersampling**.
* Apply **Logistic Regression**, **Random Forest**, or **XGBoost** for prediction.
* Evaluate using metrics beyond accuracy (like **F1-score**, **ROC AUC**).

---

## 📌 Dependencies

```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
```

Ensure the environment includes:

* Python 3.8+
* Jupyter Notebook or JupyterLab
* `seaborn`, `matplotlib`, `scikit-learn`, `pandas`
