# Factors-Affecting-Contraceptive-Utilisation-in-India
This project analyzes data from the **National Family Health Survey (NFHS-5)** to identify the key socio-economic, demographic, and health-related drivers of contraceptive usage in India. 

Using a dataset of over 130 indicators across all Indian states and union territories, this analysis employs machine learning techniques—specifically **Lasso Regression** and **Random Forest**—to handle high-dimensionality and isolate the most robust predictors of family planning adoption.

**Key Objective:** To move beyond simple correlation and identify actionable policy levers (such as child mortality rates and female literacy) that significantly influence contraceptive uptake.

# Methodology & Technical Approach
The analysis addresses the challenge of "High Dimensionality" (130+ features vs. limited observations) through a rigorous preprocessing pipeline:

1.  **Data Cleaning:**
    * Handling NFHS-specific error codes (negative values).
    * Dynamic imputation of missing values using median strategies to prevent data leakage.
    * Removal of aggregate rows (e.g., "India" total) to ensure granular state-level analysis.
2.  **Dimensionality Reduction:**
    * **Null Value Filtering:** Dropping features with >40% missing data.
    * **Correlation Filtering:** Automatically removing features with >95% collinearity (e.g., duplicate literacy metrics) to reduce redundancy.
3.  **Modeling:**
    * **Lasso Regression (L1 Regularization):** Used for strict feature selection, shrinking coefficients of irrelevant features to zero.
    * **Random Forest Regressor:** Used to capture non-linear relationships and complex interactions between variables.

## Key Findings
* **Primary Predictor:** The analysis consistently identifies **Under-Five Mortality Rate** as a top predictor, suggesting a strong link between child survival confidence and family planning.
* **Secondary Factors:** Female literacy, access to media, and economic indicators (like bank account ownership) show significant importance.
