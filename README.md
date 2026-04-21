# Place Matters: Regional Risks in Breast Cancer Mortality
The Influence of Clinical and Structural Factors on In-Hospital Breast Cancer Mortality Among Black Women
# Executive Summary

### Problem
Black women in the United States experience disproportionately high breast cancer mortality, yet the specific drivers of in-hospital death, particularly the role of structural inequities beyond clinical severity, remain underexamined.

## Methodology
This study analyzes 5,933 hospitalizations from the 2021 National Inpatient Sample using a machine learning framework. Data Preparation Extraction of breast cancer hospitalizations using ICD-10 code C50. Cleaning and recoding of clinical and structural variables. Application of discharge weights to produce nationally representative estimates. Handling of categorical variables through encoding and normalization.
Exploratory Data Analysis Descriptive statistics of demographic, clinical, and structural variables. Comparative analysis across geographic regions and socioeconomic strata.
Statistical & Machine Learning Models Six predictive models were trained and compared: Model Purpose Logistic Regression (L1/L2) Baseline statistical inference Elastic Net (Best Model) Handles multicollinearity and feature selection Random Forest Captures nonlinear relationships Gradient Boosting (GBM) Enhances predictive performance XGBoost Optimized ensemble learning Training/Validation Split: 70% / 30% Evaluation Metric: Area Under the ROC Curve (AUC) Best Performance: Elastic Net (AUC ≈ 0.69) Feature Importance: Assessed using permutation importance.


### Key Features

Race-Specific Analysis: Focus exclusively on non-Hispanic Black women. Nationally Representative Estimates: Use of NIS discharge weights. Integration of Clinical and Structural Determinants. Machine Learning–Driven Risk Prediction. Structural Inequity Gap: Quantifies mortality differences attributable to systemic factors. Regional Analysis: Highlights disparities across U.S. Census divisions.

## Key Findings

In-Hospital Mortality Rate: 5.3% among Black women. Strongest Clinical Predictor: Metastatic disease (OR ≈ 2.18). Key Structural Predictors: Geographic Region: Highest risk in the Deep South (Division 6) and lowest in Division 8. Insurance Status: Self-pay and Medicaid associated with higher mortality. Socioeconomic Status: Lower ZIP income quartiles linked to increased risk. Admission Type: Non-elective admissions significantly increase mortality. Structural Inequity Gap: Up to a 37-percentage-point difference in predicted mortality between high- and low-risk regions and a model based dashboard was created for user exploration of the inequity gap.
