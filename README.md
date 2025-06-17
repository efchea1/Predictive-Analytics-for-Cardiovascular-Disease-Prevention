# Predictive Analytics for Cardiovascular Disease Prevention

## Overview
This project uses the 2021 Behavioral Risk Factor Surveillance System (BRFSS) dataset to develop machine learning models predicting cardiovascular disease (CVD) risk. By identifying individuals at high risk, this work supports targeted prevention and contributes to population health strategy.

## Objectives
- Clean and preprocess large national health survey data (BRFSS, n = 308,000+)
- Apply predictive models (Logistic Regression, Decision Tree, KNN, Random Forest)
- Evaluate models using AUC, Brier Score, and ROC curves
- Support early detection and public health intervention strategies

## Dataset
- **Source**: 2021 BRFSS (Kaggle)
- **Participants**: 308,854 adults
- **Variables Used**: 19 health behavior and chronic condition features
- **Outcome Variable**: Heart Disease (binary)

## Methods
### Preprocessing
- Column renaming, factor conversion, and scaling
- Imputed missing values (mean/mode)
- Train-test split (75/25)

### Models
- **Logistic Regression** – interpretable baseline
- **Decision Tree** – rule-based explainability
- **KNN** – local similarity insights
- **Random Forest** – ensemble learning for nonlinear patterns

### Evaluation
- **AUC Scores**: LR (0.837), RF (0.824), DT (0.768), KNN (0.674)
- **Brier Scores**: LR (0.063), RF (0.065), DT (0.074), KNN (0.097)
- ROC and calibration plots provided

## Key Findings
- Logistic Regression had best calibration and performance balance
- Random Forest excelled in modeling complex feature interactions
- Fruit and vegetable intake, BMI, exercise, depression, and smoking were top predictors

## Technologies Used
- R (tidyverse, ranger, pROC, caret)
- Data source: BRFSS 2021 survey
- GitHub for version control

## Files
- `CVD_Risk_Prediction_ML_Project.R` – full modeling script
- `Prediction_ML_Project.Rmd` – formatted project report
- `Project_Report.md` – in-depth model comparison & discussion
- `README.md` – overview documentation

## Author
**Emmanuel Fle Chea**  
[GitHub](https://github.com/efchea1) | [LinkedIn](https://linkedin.com/in/emmanuel-fle-chea-ba0669129)
