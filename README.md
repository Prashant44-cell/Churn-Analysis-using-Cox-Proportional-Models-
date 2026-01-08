# 📊 Churn Analysis using Cox Proportional Hazards Model

This project demonstrates how to apply **survival analysis** techniques, specifically the **Cox Proportional Hazards (Cox-PH) model**, to analyze and predict **customer churn over time**. The Cox-PH model is widely used in medical research and reliability engineering, but here it is adapted to business analytics to understand customer retention. 

## 🚀 Project Overview Customer 
churn is a critical metric for subscription-based businesses. Instead of simply predicting *whether* a customer will churn, survival analysis allows us to estimate **when** churn is likely to occur. The Cox-PH model helps us: - Estimate the **hazard function** (instantaneous risk of churn). - Quantify the effect of customer features (covariates) on churn risk. - Predict **survival probabilities** (likelihood of staying subscribed) over time. 

## 🛠️ Procedure
### 1. Setup & Data Generation - Define **duration**: how long each customer has been observed. - Define **event indicator**: whether the customer churned (1) or is still active (0). - Collect **covariates**: customer features such as age, tenure, usage frequency, or engagement metrics.
### 2. Model Fitting - Fit the **Cox-PH model** using duration, event indicator, and covariates. - The model estimates: - **Baseline hazard function** (risk of churn over time without covariates). **Log-hazard coefficients** for each covariate.
### 3. Interpretation - Convert coefficients into **Hazard Ratios (HRs)**: - HR > 1 → Feature increases churn risk. - HR < 1 → Feature decreases churn risk. - Example: If HR for "low engagement" = 2.0, customers with low engagement are twice as likely to churn at any given time. ### 4. Prediction - Use the fitted model to predict **survival probabilities**: - Probability that a customer remains subscribed at different time points. - Apply predictions to: - Individual customers. - Cohorts (e.g., new vs. long-term customers).
