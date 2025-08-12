# Student Outflow Prediction Project

## Project Overview
This project focuses on analyzing and predicting student outflow (dropout) from master's programs at the National Research University Higher School of Economics (HSE). The goal is to develop a machine learning model that identifies students at risk of expulsion based on academic performance, attendance, and demographic data. The model aims to enable early intervention and improve student retention rates.

## Key Features
- **Data Sources**: The dataset includes academic records (grades, retakes, attendance), demographic information (gender, region, socioeconomic status), and program-specific details (faculty, specialty).
- **Target Variable**: Binary classification (`IncCategory`), where `1` indicates expulsion and `0` indicates continuation.

## Methods
- **Data Preprocessing**: Handling missing values, feature selection, and aggregation (e.g., min/max/mean grades, attendance metrics).
- **Models Tested**:
  - Logistic Regression
  - Decision Trees
  - Random Forest
  - k-Nearest Neighbors (k-NN)
  - Support Vector Machines (SVM)
  - Gradient Boosting (XGBoost, CatBoost)
- **Evaluation Metric**: ROC AUC (to address class imbalance).
- **Best Model**: **XGBoost** achieved the highest ROC AUC (0.895 on training, 0.854 on test data).

## Results
- **Top Predictors**:
  1. Maximum absences (`Missed_max`)
  2. Number of retakes (`RepassCount`)
  3. Modal grade (`StrResult_mode`)
  4. Faculty/Specialty (e.g., Urban Development, Political Science)
  5. Admission year (`AdmissionYear`)

## Practical Applications
- The model can be integrated into HSE’s academic support systems to flag at-risk students.
- Recommendations include targeted interventions for students with poor attendance or frequent retakes.

## Repository Contents
- `EDA/`: Exploratory data analysis (Jupyter notebooks).
- `Model_Training/`: Code for preprocessing, model training, and evaluation.
- `Data/`: Placeholder for dataset (not included due to privacy).

## Future Work
- Incorporate additional features (e.g., psychological/social factors).
- Test real-time monitoring systems for early alerts.
