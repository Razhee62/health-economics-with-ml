# health-economics-with-ml
Predicting Out-of-Pocket Healthcare Expenditure using Macroeconomic Machine Learning.
# Predicting Out-of-Pocket Healthcare Expenditure using Macroeconomic Machine Learning

This repository contains a data science pipeline that combines macroeconomic indicators with global health spending metrics to predict household financial vulnerabilities during health crises.

## Project Overview
This project investigates how a nation's absolute economic development dictates out-of-pocket (OOP) healthcare expenditures. By leveraging data from the **World Bank** and the **World Health Organization (WHO)**, we developed an ensemble machine learning model to track these trends across developing nations.

## Key Findings
* **Winning Model:** The `XGBoost Regressor` outperformed Random Forest, achieving an **$R^2$ score of 0.223** and a Mean Absolute Error (MAE) of **12.09%**.
* **Feature Importance:** 
  * `GDP_Per_Capita`: **61.65%** (Dominant driver of health financing structures)
  * `Poverty_Headcount_Ratio`: **25.85%**
  * `Year` (Temporal Trends): **12.51%**
* **Public Health Insight:** The model proves that economic factors explain roughly 22.3% of health spending variances. The remaining variance is driven by institutional policy, universal health coverage, and infrastructure—highlighting the critical need for systemic public health policy interventions.

## Data Pipeline & Methodology
1. **Economic Features:** Programmatically pulled from the World Bank API via `wbgapi` (GDP per Capita and Poverty Headcount).
2. **Health Targets:** Sourced from the 2026 World Health Organization Global Health Expenditure Database (GHED).
3. **Data Cleaning:** Implemented group-wise time-series linear interpolation to handle structural missingness without introducing geographic bias.
4. **Modeling:** Evaluated competing architectures using an 80/20 train-test split optimized via gradient boosting.

## How to Run
1. Clone this repository.
2. Install dependencies: `pip install -r requirements.txt`
3. Open and execute the notebook inside the `notebooks/` directory.

## Author
* AL Razee
* Assistant Organizing Secratary, SUST Data Science Club
