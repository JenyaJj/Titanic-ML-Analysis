# Titanic-ML-Analysis


This project focuses on predicting the survival chances of passengers aboard the RMS Titanic using machine learning techniques. It involves exploratory data analysis (EDA), feature engineering, and model development with various machine learning algorithms.

## Project Overview

The sinking of the Titanic in 1912 was a tragedy that revealed disparities in survival based on class, gender, and other factors. Using the Titanic dataset provided by Kaggle, this project builds a machine learning model to predict survival probabilities.

## Features

- **EDA**: Identification of key factors influencing survival.
- **Data Preparation**: Cleaning and preprocessing, handling missing values, feature engineering.
- **Modeling**: Evaluation of several ML algorithms, including:
  - Decision Trees
  - Random Forest
  - Logistic Regression
  - Support Vector Machines (SVM)
- **Documentation**: Detailed Jupyter Notebook with visualizations and results.

## Project Structure

```plaintext
Titanic-Survival-Prediction/
│
├── data/                     # Datasets
├── TitanicML.ipynd           # Main Jupyter Notebook
├── README.md                 # Project documentation
├── requirements.txt          # Python dependencies
```

## Results
This project applied various machine learning models to predict Titanic survival probabilities. Below are the key results and insights:

## Exploratory Data Analysis (EDA) Findings
- Missing Data:
-- The Cabin column had ~77% missing values and was excluded.
-- The Age column, missing 177 values, was imputed as it is a critical factor.
-- The Embarked column had only two missing values, which were excluded.
- Feature Engineering:
-- FamilySize: Derived by summing SibSp, Parch, and adding 1. Moderate-sized families (2-4 members) showed higher survival rates.
-- FamilyID: Created to group passengers with the same surname and family size.
-- Titles: Extracted from names and grouped into categories (e.g., Mr., Miss., Mrs.), showing strong correlations with survival.
-- Ticket Prefix: Analysed but found redundant due to correlation with FamilySize.
## Survival Patterns:
- Class: Survival rates were stratified by ticket class:
  - First class: 62%
  - Second class: 47%
  - Third class: 24%
-  Gender: Women had a significantly higher survival rate (74%) than men (19%).
- Embarkation Port: Passengers from port C had the highest survival rate (55%), compared to port S (33%).
- Children: Passengers with the title "Master" had the highest survival rates among all groups.
## Model Performance
Four machine learning models were evaluated: Random Forest, Logistic Regression, Decision Tree, and Support Vector Machines (SVM). Performance metrics included accuracy, precision, recall, and F1-score.

- Best Model: SVM achieved the highest test accuracy of 93.78%, with balanced precision and recall for both survivors and non-survivors.
- Other Model Performances:
  - Logistic Regression: 92.58%
  - Decision Tree: 90.19%
  - Random Forest: 89.47%
## Key Observations:
- Feature engineering (e.g., adding Title, FamilySize, FamilyID) significantly improved model accuracy.
- Random Forest initially achieved high accuracy but showed signs of overfitting on the training data, with limited improvement on the test set.
- SVM and Decision Tree were more effective at capturing nuanced patterns in the data, particularly gender and class biases.
- Logistic Regression was stable and robust but sensitive to feature redundancy.
## Conclusion:
This project highlights the importance of feature engineering and the ability of machine learning models to uncover meaningful patterns in data. SVM emerged as the best-performing model, demonstrating excellent generalization and balanced performance metrics. These results emphasize the potential of machine learning to analyse complex historical datasets, though ethical considerations like biases in gender and class remain crucial for ensuring fairness.
