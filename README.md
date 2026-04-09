# Predicting Dog Trainability to Mitigate Bite Incidents in New York City

## Overview
This project aims to predict dog trainability as a means to mitigate dog bite incidents in urban areas like New York City. Using data from the National Electronic Injury Surveillance System (NEISS) and the American Kennel Club (AKC), we evaluate factors influencing trainability, such as breed, age, and spay/neuter status. The goal is to provide actionable insights for public safety measures and targeted training programs.

## Dataset
The dataset combines:
- **Dog Bite Incidents:** NEISS records detailing dog characteristics, incident contexts, and victim demographics.
- **Trainability Scores:** Evaluations provided by AKC based on breed-based criteria.

### Key Features:
- **Breed, Gender, Spay/Neuter Status, and Season** were among the variables used to predict the target variable, `trainability value`, a continuous score ranging from 0 to 1.
- Exploratory data analysis revealed key insights such as breed distribution and seasonal trends in bite incidents.

## Methodology
1. **Data Preprocessing:**
   - Missing values were imputed.
   - Features were encoded (ordinal and one-hot encoding).
   - Highly collinear variables were removed.
2. **Model Training:**
   - Models evaluated include Ridge Regression, Lasso Regression, Random Forest, XGBoost, and Support Vector Regression.
   - **Ridge Regression** emerged as the best-performing model with an MSE of 0.02905 on the test set.
3. **Evaluation:**
   - Mean Squared Error (MSE) was used as the primary metric.
   - Feature importance was analyzed using SHAP values and Ridge coefficients.

## Results
- **Top Features Influencing Trainability:**
  - **Breed:** The strongest predictor of trainability.
  - **Season:** Seasonal trends align with behavioral changes.
  - **Spay/Neuter Status:** Unneutered dogs were associated with lower trainability.
- **Best Model:** Ridge Regression was selected due to its strong performance and interpretability.

## Prerequisites
- **Python Version:** 3.10
- **Dependencies:** See `requirements.yaml` for a full list of libraries and package versions.

## Setup Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/penggaogu/Brown_data1030.git
   cd Brown_data1030
