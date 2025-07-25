# 🚑 Predicting Hospital Readmission Risk for Chronic Patients

## 🔍 Overview

Hospital readmissions among patients with chronic illnesses (such as diabetes, heart disease, and hypertension) place a heavy burden on healthcare systems. This project aims to develop a data-driven model to **predict the likelihood of a patient being readmitted** using healthcare data. By identifying high-risk patients early, hospitals can implement proactive care strategies to reduce readmission rates and improve patient outcomes.

---

## 🧠 Objectives

- Analyze patient data to uncover patterns related to readmission.
- Develop a risk scoring system based on key clinical and demographic features.
- Build a machine learning model to predict hospital readmission.
- Visualize insights to assist healthcare professionals in decision-making.

---

## 📁 Dataset

The dataset used (`healthcare_dataset.csv`) contains anonymized patient records with the following relevant fields:

- **Demographics**: Age, Gender
- **Clinical Details**: Medical Condition, Test Results
- **Admission Info**: Admission Type, Date of Admission & Discharge
- **Financial Info**: Billing Amount
- **Other Info**: Hospital, Doctor, Room Number

---

## ⚙️ Key Features & Implementation

### ✅ Data Preprocessing
- Handled missing values
- Dropped irrelevant or identifier columns (e.g., Name, Room Number)
- Removed outliers using Interquartile Range (IQR) on `Billing Amount`

### 🔐 Readmission Scoring Logic
Patients were assigned a risk score based on:
1. High-risk chronic conditions
2. Emergency or urgent admission type
3. Abnormal or inconclusive test results
4. Billing amount above 75th percentile
5. Age ≥ 65

A custom logic converts the score to a binary target:
- `1` → Readmitted
- `0` → Not Readmitted

### 📊 Data Visualization
- Readmission distribution
- Readmission by medical condition
- Age vs. Readmission (histogram)
- Billing amount by readmission status (box plot)
- Admission type vs. readmission (bar chart)

### 🤖 Machine Learning Pipeline
- Used `sklearn` for modeling
- Encoded categorical features using `OrdinalEncoder` and `OneHotEncoder`
- Applied `StandardScaler` for numeric features
- Train-test split for model evaluation

*Model training and evaluation steps are performed to assess prediction accuracy and generalizability.*

---

## 📉 Tools & Technologies

- **Python 3.x**
- **Pandas, NumPy** – Data manipulation
- **Matplotlib, Seaborn** – Visualization
- **scikit-learn** – ML modeling & preprocessing
- **Jupyter Notebook** – Development environment

---

## 📷 Sample Visualizations

> ![Readmission Distribution Chart](assets/readmission_distribution.png)  
> ![Readmission by Medical Condition](assets/readmission_medical_condition.png)

---

## 👥 Team Members

| Name               | Role                        |
|--------------------|-----------------------------|
| **Raut Sipun Gopal**  | Data Analysis & Visualization |
| **Binayak Naudia**    | Backend Logic & Model Development |
| **Subham Satyajit**   | Preprocessing & Evaluation |
| **Avantika Panda**    | Documentation & Testing     |

---

## 🆔 Team Info

**Team Name:** `Team (SC2) - 06`

---

## 🚀 Future Scope

- Integrate with a hospital web dashboard for real-time predictions.
- Include more features like medication history and diagnosis codes.
- Use advanced ML models (XGBoost, Random Forest) for better performance.
- Implement patient-specific intervention recommendations.

---

## 📜 License

This project is developed for academic and educational purposes under Smart India Hackathon guidelines.

---

