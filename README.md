Diabetes Readmission Prediction
Overview

This project aims to predict the risk of hospital readmission for diabetes patients using machine learning. The goal is to help healthcare facilities identify high-risk patients, optimize resource allocation, and reduce costs associated with preventable readmissions.

The project uses the UCI Diabetes Readmission Dataset and implements advanced modeling techniques to tackle class imbalance, threshold selection, and probability-based risk ranking.

Problem Statement

Hospital readmissions are costly and often preventable. Traditional approaches rely on manual tracking and human judgment, which can lead to inefficiencies.

This project addresses the problem by:

Predicting readmission likelihood within 30 days

Providing actionable risk scores for patient prioritization

Leveraging machine learning to identify patterns not apparent from raw data

Dataset

Source: UCI Machine Learning Repository – Diabetes Readmission Dataset

Key Features:

Demographics: race, gender, age

Hospital stay info: time_in_hospital, admission_type_id, discharge_disposition_id, admission_source_id

Clinical metrics: num_lab_procedures, num_medications, num_diagnoses, diag_1, max_glu_serum, a1cresult

Medication info: insulin, change, diabetesmed

Target: readmitted_binary (0 = no readmission, 1 = readmitted within 30 days)

Methodology

Data Cleaning & Preprocessing

Removed irrelevant columns (Unnamed: 0, encounter_id, etc.)

Handled categorical and numerical features with ColumnTransformer

Addressed class imbalance using model parameters (scale_pos_weight) and threshold optimization

Model Selection

Compared Logistic Regression, Random Forest, XGBoost, LightGBM, and CatBoost

Evaluated models using ROC-AUC, PR-AUC, F1-score, and threshold tuning

XGBoost outperformed other models (ROC-AUC: 0.899, PR-AUC: 0.595)

Threshold Optimization

Explored multiple probability thresholds to maximize F1-score

Selected operational threshold = 0.35 for best balance of recall and precision

Business-Relevant Evaluation

Identified top 10% high-risk patients

Precision in top 10% = 0.60 → captures the majority of true readmissions while targeting a manageable patient group

Demonstrates practical, cost-saving utility for healthcare operations

Key Outcomes

Developed a robust XGBoost model capable of predicting readmission risk

Applied data-driven threshold selection for real-world deployment

Provided actionable insights for hospitals to reduce readmission costs

Showcased analytical problem-solving, handling class imbalance, feature preprocessing, and risk prioritization
