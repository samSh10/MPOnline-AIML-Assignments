# Adult Census Income Classification Project

## Objective

Build and evaluate machine learning models to predict whether an individual's annual income exceeds **$50K** using demographic and employment-related attributes from the Adult Census Income dataset.

---

# Dataset

- **Source:** UCI Machine Learning Repository
- **Target Variable:** Income (`<=50K` or `>50K`)
- **Number of Records:** 32,561
- **Number of Features:** 14 predictor variables and 1 target variable

The dataset contains demographic, educational, and employment-related information used to predict whether a person's annual income exceeds $50,000.

---

# Project Workflow

## 1. Dataset Understanding

The first step involves understanding the dataset by:

- Loading the dataset
- Inspecting the first few rows
- Checking data types
- Viewing summary statistics
- Identifying missing values
- Understanding the target variable distribution

---

## 2. Data Cleaning

The following preprocessing steps were performed:

- Replaced missing values (`?`) with `NaN`
- Removed rows containing missing values
- Separated input features and target variable
- Verified dataset consistency

---

## 3. Exploratory Data Analysis (EDA)

The following visualizations were created:

- Income Class Distribution
- Age Distribution
- Working Hours Distribution
- Hours Worked vs Income
- Dataset Summary Statistics

EDA helps identify trends, class imbalance, and relationships among variables before model training.

---

## 4. Feature Engineering

### Numerical Features

The following preprocessing steps were applied:

- Median Imputation
- Standard Scaling

### Categorical Features

The following preprocessing steps were applied:

- Most Frequent Imputation
- One-Hot Encoding

A Scikit-learn **Pipeline** and **ColumnTransformer** were used to automate preprocessing and ensure consistency during training and testing.

---

## 5. Train-Test Split

The dataset was divided into:

- **Training Set:** 80%
- **Testing Set:** 20%

Stratified sampling was used to preserve the class distribution in both sets.

---

# Machine Learning Models

The following classification algorithms were implemented:

1. Logistic Regression
2. Decision Tree Classifier
3. Random Forest Classifier
4. K-Nearest Neighbors (KNN)
5. Support Vector Machine (SVM)

Each model was trained using the same preprocessing pipeline to ensure a fair comparison.

---

# Model Evaluation

The models were evaluated using the following performance metrics:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC Score

These metrics provide a comprehensive comparison of classification performance.

---

# Additional Analysis

The notebook also includes:

- Confusion Matrix for the best-performing model
- Feature Importance using Random Forest
- Performance comparison table for all models

These analyses help interpret the models and identify the most influential features affecting income prediction.

---

# Expected Results

Among the evaluated algorithms, **Random Forest** is generally expected to achieve the highest performance because it:

- Handles mixed numerical and categorical data effectively.
- Captures complex non-linear relationships.
- Reduces overfitting through ensemble learning.
- Performs well on structured tabular datasets.

Actual results may vary slightly depending on preprocessing and library versions.

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

# Conclusion

This project demonstrates a complete end-to-end supervised machine learning workflow, including:

- Dataset Understanding
- Data Cleaning
- Exploratory Data Analysis
- Feature Engineering
- Model Building
- Model Evaluation
- Model Comparison

The notebook is designed to run directly in **Google Colab** or **Kaggle** without requiring manual dataset downloads, provided internet access is available.

---

# Future Improvements

Potential enhancements include:

- Hyperparameter tuning using GridSearchCV
- Cross-validation for improved model robustness
- ROC Curves and Precision-Recall Curves for all models
- Explainable AI techniques (SHAP or LIME)
- Comparison with XGBoost, LightGBM, and CatBoost
- Deployment using Streamlit or Flask

---

# References

1. UCI Machine Learning Repository – Adult Census Income Dataset
2. Scikit-learn Documentation
3. Pandas Documentation
4. NumPy Documentation
5. Matplotlib Documentation
6. Seaborn Documentation
