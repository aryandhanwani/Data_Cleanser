# 🧠 Healthcare Data Cleaning Project

## 📌 Overview
This project focuses on cleaning a healthcare dataset by handling missing values and outliers to make the data suitable for machine learning models.

---

## 📊 Dataset Information
The dataset contains 300 patient records with the following features:

- patient_id
- age
- gender
- region
- bmi
- blood_pressure
- cholesterol
- glucose
- disease_risk

The dataset was intentionally created with:
- Missing values
- Outliers

---

## 🧹 Data Cleaning Steps

### 1. Missing Value Analysis
- Identified missing values using `.isna().sum()`
- Calculated percentage of missing values

---

### 2. Missing Value Imputation

#### a. Simple Imputer
- BMI → Mean
- Region → Most frequent value

#### b. Missing Indicator + Random Imputation
- Created binary indicator columns
- Filled missing values using random sampling

#### c. KNN Imputer
- Used similarity between rows
- Applied on numerical features

#### d. MICE (Iterative Imputer)
- Predicted missing values using other columns
- Most advanced and accurate method

---

## 📉 Outlier Detection

### Methods Used:
- Z-score
- IQR (Interquartile Range)
- Percentile Method

---

## ⚙️ Outlier Treatment

### Techniques:
- Percentile Capping (1%–99%)
- Winsorization

These methods reduced extreme values without removing data.

---

## 📊 Before vs After Comparison

### Before Cleaning:
- Missing values present
- Extreme outliers affected distribution

### After Cleaning:
- No missing values
- Outliers reduced
- Data more stable and consistent

---

## ✅ Results & Conclusion

- MICE was the most effective imputation method
- Winsorization preserved data quality best
- Dataset became clean, reliable, and ready for machine learning

---

## 🚀 Final Outcome

A fully cleaned dataset with:
- No missing values
- Handled outliers
- Improved usability for predictive modeling
