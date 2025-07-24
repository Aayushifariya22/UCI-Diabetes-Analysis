# 🏥 Predicting Diabetes Patient Readmission within 30 Days

> A data-driven machine learning project aimed at predicting hospital readmissions of diabetes patients based on 10 years of hospital data using models like Logistic Regression, Random Forest, and XGBoost.

---

## 📊 Overview

This project addresses a healthcare problem — predicting whether a diabetic patient will be readmitted within 30 days of discharge. Using a dataset containing over 10 years of hospital records (1999–2008), we performed an end-to-end analysis from data cleaning and imputation to model building and evaluation.

---

## 👩‍💻 Team Hackverse – Hack-A-Stat 25

- **Aayushi Fariya**  
- **Sayali Mahurkar**  
- **Sneha Maheshwari**

---

## 🧩 Problem Statement

Given patient records with lab results, medication details, and hospital stay information, the objective is to predict **30-day readmission** using classification models.

---

## 🗂️ Dataset Description

- Records: ~130 hospitals
- Duration: 10 years (1999–2008)
- Features: Demographics, medical specialties, lab results, medications, diagnoses
- Target: `readmitted` (`<30`, `>30`, `NO`)

---

## 📌 Project Objectives

1. Perform Exploratory Data Analysis (EDA)
2. Impute missing values using predictive models (KNN, Random Forest)
3. Analyze the impact of **HbA1c** (blood glucose) levels
4. Study changes in **diabetes medications** over time
5. Test for **multicollinearity** and reduce dimensionality
6. Build machine learning models and evaluate performance

---

## 🔬 EDA Highlights

- Majority patients are **Caucasian**, likely due to the dataset’s US origin.
- High skewness in `num_medications` and `num_lab_procedures`.
- **Circulatory diseases** dominate diagnoses across all levels.
- **Insulin** dosage changes showed strong influence on readmissions.

---

## 🛠️ Methodology

- **Missing Value Treatment**: 
  - Predictive imputation using Random Forest
  - Dropping columns with >90% missing (e.g., `Weight`)
- **Feature Engineering**:
  - New variable `DM` for drug effect encoding
  - VIF used to handle multicollinearity
- **Feature Selection**: Chi-square test, PCA

---

## 🤖 Models Used

| Model                    | Accuracy | Notes                                  |
|-------------------------|----------|----------------------------------------|
| Logistic Regression     | 95%      | High accuracy, poor recall             |
| Random Forest Classifier| 93%      | Imbalanced classes affect recall       |
| XGBoost                 | 95%      | High precision, very poor recall       |
| **Balanced Random Forest** | **84% (F1)** | Best trade-off in class imbalance |

---

## ✅ Key Insights

- Higher **HbA1c** levels do not always lead to medication changes.
- **Balanced Random Forest** gave the most stable results in imbalanced classification.
- Feature `max_glu_serum` and `A1Cresult` had highest predictive importance.

---

## 🔚 Conclusion

By identifying key factors such as HbA1c levels and medication patterns, we can aid healthcare professionals in reducing **avoidable readmissions** and improving **post-discharge care**.

---

## 🧭 Limitations & Future Work

- Highly imbalanced data; future work can involve advanced imbalance handling (e.g., SMOTE, ADASYN).
- Patient segmentation and deeper causal analysis can improve interpretability.
- Real-time dashboard or deployment as an API for hospital systems.

---

## 📁 Files in this Repository

- `JnJ_Final.ipynb` – Jupyter notebook with all analysis and models
- `UCIdiabetes.csv` – Cleaned dataset
- `README.md` – Project overview
- `JnJ REPORT.pdf` – Final project report with full documentation

---
