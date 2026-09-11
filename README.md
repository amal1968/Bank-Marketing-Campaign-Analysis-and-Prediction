# Bank Marketing Campaign Analysis and Prediction

## Project Overview

This project analyzes the Bank Marketing dataset and develops machine learning models to predict whether a client will subscribe to a term deposit.

The project also applies customer segmentation using KMeans clustering to identify potential customer groups.

## Dataset

- **Source:** UCI Machine Learning Repository
- **Instances:** 41,188
- **Features:** 20
- **Target:** `y` — Term deposit subscription (`yes` / `no`)

## Project Workflow

### 1. Data Acquisition
- Retrieved the dataset using the `ucimlrepo` Python package.

### 2. Data Preprocessing
- Handled missing values.
- Removed the `poutcome` feature due to a high percentage of missing values.
- Removed duplicate records.
- Treated outliers using the IQR method.

### 3. Exploratory Data Analysis
- Analyzed numerical and categorical features.
- Used histograms, boxplots, count plots, area plots, pie charts, and correlation analysis.
- Investigated relationships between customer characteristics and campaign outcomes.

### 4. Feature Engineering
- Created `no_previous_contact` and `total_contacts`.
- Applied transformations to skewed features.
- Encoded categorical variables.
- Standardized numerical features using `StandardScaler`.

### 5. Machine Learning

Three classification algorithms were implemented:

- Logistic Regression
- Random Forest
- Support Vector Machine (SVM)

**GridSearchCV** was used for hyperparameter tuning.

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC AUC

The effect of **Scaling, Normalization, and PCA** on model performance was also investigated.

### 6. Customer Segmentation

KMeans clustering was applied to identify potential customer segments.

- PCA was used for dimensionality reduction and visualization.
- Clustering performance was evaluated using the Adjusted Rand Index (ARI).

## Key Results

- **Random Forest** achieved the highest accuracy among the tested classification models.
- Features such as `duration`, `pdays`, and `previous` were important predictors of subscription likelihood.
- Scaling had limited impact on model performance.
- Normalization and PCA slightly reduced model accuracy.
- KMeans clustering identified distinct customer segments that could support targeted marketing strategies.

## Technologies

Python · Pandas · NumPy · Scikit-learn · Matplotlib · Seaborn · UCI ML Repository

## Project Structure

```text
Bank-Marketing-Campaign-Analysis-and-Prediction/
│
├── notebook.ipynb
├── README.md
└── dataset/
```

## Conclusion

This project demonstrates an end-to-end data science workflow, from data preprocessing and exploratory analysis to machine learning, model evaluation, and customer segmentation.

The results can help banking institutions better understand customer behavior and improve the targeting of marketing campaigns.