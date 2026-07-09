# Vaccine Uptake Prediction

## Overview

This project predicts whether individuals are likely to receive the **H1N1** and **Seasonal Influenza** vaccines using demographic, behavioral, and healthcare-related survey data.

The objective is to develop a predictive model that can identify individuals with a lower likelihood of vaccination, enabling targeted public health interventions and improved vaccination outreach.

---

## Problem Statement

Vaccination campaigns often face challenges in identifying populations that are less likely to receive vaccines. By leveraging machine learning, this project predicts vaccine uptake based on individual characteristics and health-related behaviors.

---

## Dataset

The dataset consists of survey responses collected from individuals, including:

- Demographic information
- Employment and socioeconomic status
- Medical history
- Chronic health conditions
- Preventive healthcare practices
- Healthcare access
- Behavioral and risk perception variables
- Vaccination labels for:
  - H1N1 Vaccine
  - Seasonal Influenza Vaccine

---

## Workflow

### Data Preprocessing

- Removed non-predictive identifiers
- Handled missing values using median and most-frequent imputation
- Encoded categorical variables
- Built preprocessing pipelines using ColumnTransformer and Pipeline

### Exploratory Data Analysis

- Examined missing values
- Studied feature distributions
- Explored vaccine uptake patterns
- Investigated relationships between demographic and behavioral variables

### Model Development

Implemented a **MultiOutput Logistic Regression** model to simultaneously predict:

- H1N1 vaccine uptake
- Seasonal influenza vaccine uptake

---

## Model Evaluation

The model was evaluated using **ROC-AUC**.

| Metric | Score |
|---------|-------|
| H1N1 ROC-AUC | **0.835** |
| Seasonal Vaccine ROC-AUC | **0.856** |
| Mean ROC-AUC | **0.845** |
| 5-Fold Cross Validation ROC-AUC | **0.844** |

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

---

## Key Findings

- Successfully developed a machine learning pipeline for predicting vaccine uptake.
- Achieved strong discrimination performance with a mean ROC-AUC of **0.845**.
- Demonstrated the effectiveness of demographic, behavioral, and healthcare variables in predicting vaccination behavior.
- Built a reusable preprocessing pipeline suitable for future healthcare prediction tasks.

---

## Future Improvements

- Compare Logistic Regression with Random Forest, XGBoost, and LightGBM.
- Perform hyperparameter tuning using GridSearchCV.
- Apply SHAP for model interpretability.
- Deploy the model using Streamlit or FastAPI.
