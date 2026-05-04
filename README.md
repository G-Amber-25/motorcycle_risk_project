# 🏍️ Modeling Motorcycle Injury Severity with Southern California Crash Data

A machine learning analysis identifying factors associated with severe and fatal motorcycle crash outcomes across four Southern California counties, using police-reported crash records from 2021–2023.

> **M.S. Data Science Capstone Thesis** | National University | ANA 699 | March 2026

---

## 📋 Project Overview

Motorcycles account for roughly 3% of registered vehicles in California but represent a disproportionate share of severe and fatal traffic injuries statewide. This study models motorcycle crash injury severity as a function of observable crash conditions across behavioral, environmental, roadway, spatial, and temporal domains.

Three machine learning models were applied and compared:
- **Logistic Regression** (multinomial)
- **Random Forest**
- **XGBoost**

SHAP (SHapley Additive exPlanations) values were used to interpret model predictions and rank feature importance across injury severity classes.

---

## 🔍 Research Questions

- Which observable behavioral, environmental, and roadway characteristics are associated with increased odds of severe or fatal motorcycle injury in Southern California?
- Are injury severity associations consistent across temporal and roadway contexts, or do risk patterns differ by time of day, day of week, and roadway type?

---

## 📊 Dataset

| Detail | Info |
|---|---|
| **Source** | Transportation Injury Mapping System (TIMS) / SWITRS |
| **Coverage** | Los Angeles, Riverside, San Bernardino, San Diego, Orange counties |
| **Years** | 2021–2023 |
| **Records** | ~19,700 motorcycle crash events |
| **Unit** | Individual crash (event-level) |

**Severity Classification:** California's KABCO scale
- **K** — Fatal injury
- **A** — Incapacitating injury
- **B** — Visible injury
- **C** — Complaint of pain
- *(Property-damage-only crashes excluded from modeling)*

> 🔗 Data is publicly available through [TIMS](https://tims.berkeley.edu/) — free account registration required to download.

---

## 🛠️ Methods

| Step | Detail |
|---|---|
| Data cleaning & preprocessing | Standardization, missing data treatment, feature engineering |
| Exploratory data analysis | Descriptive statistics, distribution analysis |
| Modeling | Multinomial Logistic Regression, Random Forest, XGBoost |
| Validation | Train/test/validation split + k-fold cross-validation |
| Interpretability | SHAP global and local feature importance |
| Imbalance handling | SMOTE (Synthetic Minority Oversampling Technique) |

**Tools:** Python (pandas, scikit-learn, XGBoost, SHAP, geopandas, matplotlib)

---

## 📈 Key Findings

- **Broadside collision geometry**, **nighttime exposure**, and **alcohol involvement** were the strongest predictors of severe and fatal outcomes across all three models
- **Tow-away status** emerged as one of the top predictors of injury severity
- Random Forest and XGBoost performed comparably (macro ROC-AUC ~0.69); no single model was declared a clear winner
- Logistic Regression provided interpretable baseline comparisons but had lower discriminative performance
- Younger riders (18–30) showed elevated fatality odds across crash configurations
- Geographic variation across counties suggested localized risk patterns worth further investigation

---

## 📁 Repository Structure

```
├── README.md                        # Project overview 
├── SoCal_Motorcycle_Crashes.csv     # Combined crash dataset (4 counties)
├── notebooks/                       # Python analysis notebooks
└── thesis/                          # Full written thesis (PDF)
```

---

## 👥 Team

This project was completed as a collaborative M.S. capstone thesis:

- Jeremiah Snipes
- Amber Garcia
- Ed Baek
- Ryan Neighbor

**Thesis Advisors:** Dr. Mario Missakian, National University & Dr. Wen Cheng, P.E., Cal Poly Pomona  
**Industry Advisor:** Mr. Brian Huynh, Chief Traffic Records Officer, California Office of Traffic Safety

🔗 Original repository: [jeremiahsnipes/motorcycle_risk_project]
(https://github.com/jeremiahsnipes/motorcycle_risk_project)

---

## 🎓 Academic Context

**Program:** M.S. in Data Science, National University School of Engineering & Computing  
**Course:** ANA 699 – Analytic Capstone Project  
**Submitted:** March 2026
