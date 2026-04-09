# Predicting Dog Behavioral Risk to Inform Public Safety Interventions in NYC

## Overview
Dog bite incidents pose a persistent public safety concern in urban environments such as New York City. However, direct behavioral risk signals are often unavailable at scale.

This project proposes a **data-driven proxy modeling framework** to estimate dog behavioral risk (via trainability scores) by integrating heterogeneous data sources. The goal is to support **preventive interventions**, such as targeted training programs and policy design.

Unlike traditional analyses that focus on post-incident reporting, this work shifts toward **predictive risk estimation**.

---

## Data Sources

This project integrates multiple data sources:

- **Dog Bite Incident Data (NEISS):** Provides structured records of injury-related incidents, including dog attributes and contextual factors.
- **Breed-level Behavioral Scores (AKC):** Used as a proxy signal for trainability and behavioral tendencies.

### Key Challenge
Behavioral traits are not directly observable at the individual level. This project addresses this by constructing a **proxy learning framework**, mapping breed-level priors to incident-level observations.

---

## Methodology

### 1. Feature Engineering
- Harmonized breed representations across datasets
- Encoded categorical variables (gender, spay/neuter, season)
- Removed collinearity to stabilize linear models

### 2. Modeling Strategy
Evaluated multiple regression models:
- Ridge Regression
- Lasso Regression
- Random Forest
- XGBoost
- Support Vector Regression

A key design consideration was balancing **predictive performance and interpretability**, given the downstream policy implications.

---

## Results

- **Best Model:** Ridge Regression (Test MSE = 0.029)
- **Key Predictors:**
  - Breed (dominant signal)
  - Seasonality effects
  - Spay/Neuter status

### Insight
Results suggest that **structural factors (breed priors) dominate behavioral prediction**, but environmental variables still provide meaningful signals.

---

## Implications

This work demonstrates a scalable approach to:

- Approximate behavioral risk using indirect signals
- Inform **targeted intervention strategies**
- Bridge the gap between **technical modeling and public policy**

---

## Technical Stack

- Python 3.10
- scikit-learn, XGBoost
- SHAP for interpretability

---

## Reproducibility

```bash
git clone https://github.com/penggaogu/Brown_data1030.git
cd Brown_data1030