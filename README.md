# 🩺 SugarSense – Diabetes Risk Prediction System
SugarSense – An AI-powered diabetes risk screening system that uses machine learning to predict diabetes risk from clinical health measurements. Built with Python, Scikit-learn, and Streamlit, featuring data preprocessing, exploratory data analysis, feature engineering, model comparison, and an interactive prediction interface.


SugarSense is a machine learning-based diabetes risk prediction project developed using Python and Scikit-learn. The project analyzes clinical health measurements and uses supervised machine learning to predict whether a patient is likely to have diabetes.

The project also includes an interactive Streamlit web application where users can enter patient measurements and receive a diabetes prediction, probability information, risk factors, and basic health recommendations.

> ⚠️ **Disclaimer:** This project is created for educational purposes only. It is not a medical diagnostic system and should not replace professional medical advice.

---

## 📌 Project Overview

Diabetes is a common chronic disease, and early identification of people who may be at higher risk can help encourage further medical screening.

The main objective of this project is to explore patient health data, perform data analysis and feature engineering, train machine learning classification models, compare their performance, and create an interactive prediction application.

### Main Objectives

- Analyze diabetes-related clinical data
- Identify problematic values in the dataset
- Perform exploratory data analysis (EDA)
- Create additional features using domain-based logic
- Train different machine learning classification models
- Compare model performance
- Build a diabetes prediction system
- Deploy the prediction interface using Streamlit

---

## 📊 Dataset

The project uses the **Pima Indians Diabetes Database**.

The dataset contains:

- **768 patient records**
- **8 original input features**
- **1 target variable**

### Original Features

| Feature | Description |
|---|---|
| Pregnancies | Number of times pregnant |
| Glucose | Plasma glucose concentration |
| BloodPressure | Diastolic blood pressure |
| SkinThickness | Triceps skin-fold thickness |
| Insulin | 2-hour serum insulin |
| BMI | Body Mass Index |
| DiabetesPedigreeFunction | Diabetes family-history related score |
| Age | Age of the patient |
| Outcome | Target variable: 0 = Non-Diabetic, 1 = Diabetic |

---

## 🔍 Data Cleaning and Analysis

The dataset contains some values represented as `0` that can be problematic for certain medical measurements.

The project investigates these values during the data audit instead of treating every zero as a valid measurement.

Problematic zero values were investigated in:

- Glucose
- BloodPressure
- SkinThickness
- Insulin
- BMI

The notebook also performs:

- Dataset shape inspection
- Data type checking
- Statistical description
- Duplicate checking
- Class distribution analysis
- Problematic-value analysis

---

## 📈 Exploratory Data Analysis

Exploratory Data Analysis was performed to understand the relationship between patient measurements and diabetes outcome.

The project includes analysis such as:

- Feature distributions
- Comparison between diabetic and non-diabetic groups
- Correlation analysis
- Correlation heatmap
- Class distribution visualization
- Analysis of important and weaker features

One important observation from the analysis is that **Glucose shows a strong relationship with diabetes outcome compared with several other features**.

---

## 🛠️ Feature Engineering

Additional features were created using information from the same patient record.

### Engineered Features

#### 1. Obesity

A binary feature based on BMI:

```python
obesity = (BMI >= 30)
