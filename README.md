# Pulse of Prevention: Analyzing Heart Health for Better Outcomes

## 📌 Project Overview

This project performs an exploratory data analysis (EDA) of heart health data to identify demographic, clinical, and medical factors associated with heart disease.

The analysis aims to help healthcare stakeholders understand important patterns, identify characteristics associated with heart disease, and support data-driven preventive healthcare strategies.

---

## 🎯 Business Objective

The primary objective is to analyze patient health information and:

- Identify key factors associated with heart disease.
- Develop a profile of patients exhibiting higher-risk characteristics.
- Explore relationships between demographic, clinical, and medical-history variables.
- Provide preventive and lifestyle recommendations based on observed patterns.
- Identify potential areas for further medical research.
- Build a machine learning model to evaluate the predictive potential of the available features.

---

## 📊 Dataset

The dataset contains **302 unique patient records** after duplicate removal and includes 14 variables.

### Key Features

| Feature | Description |
|---|---|
| age | Age of the patient |
| sex | Gender |
| cp | Chest pain type |
| trestbps | Resting blood pressure |
| chol | Serum cholesterol |
| fbs | Fasting blood sugar >120 mg/dl |
| restecg | Resting ECG result |
| thalach | Maximum heart rate achieved |
| exang | Exercise-induced angina |
| oldpeak | ST depression induced by exercise |
| slope | Slope of peak exercise ST segment |
| ca | Number of major vessels |
| thal | Thalassemia |
| target | Heart disease diagnosis |

---

## 🧹 Data Cleaning & Preprocessing

The following preprocessing steps were performed:

- Checked dataset dimensions and data types.
- Checked for missing values.
- Identified and removed duplicate records.
- Validated categorical variables and their unique values.
- Investigated values outside the ranges specified in the data dictionary.
- Detected potential outliers using boxplots.
- Applied standardization to selected clinical measurements using `StandardScaler`.

### Data Quality Observation

Two values were identified outside the ranges specified in the supplied data dictionary:

- `ca = 4`
- `thal = 0`

These observations were retained rather than being arbitrarily removed or recoded and were considered during the analysis.

---

## 🔎 Exploratory Data Analysis

The project answers basic, medium, and advanced analytical questions covering:

### Basic Analysis

- Average patient age
- Gender distribution
- Average resting blood pressure
- Fasting blood sugar levels
- Chest pain types
- Maximum heart rate
- Exercise-induced angina
- Average cholesterol
- Resting ECG results
- Major vessel distribution

### Intermediate Analysis

- Age and cholesterol correlation
- Chest pain distribution across age groups
- Maximum heart rate and exercise-induced angina
- Resting blood pressure by gender
- Fasting blood sugar and heart disease
- Major vessels and heart disease
- Oldpeak across chest pain types
- Thalassemia and heart disease
- Common feature combinations among heart disease cases
- Clinical measurement comparison between target groups

### Advanced Analysis

- Combined analysis of age, cholesterol, and blood pressure
- Correlation analysis of features with heart disease
- Logistic regression classification
- Slope distribution across chest pain types
- Relationship between age, thalassemia, and heart disease

---

## 📈 Key Findings

- The average patient age is approximately **54.42 years**.
- Approximately **68.2%** of the records are male and **31.8%** are female.
- Average resting blood pressure is approximately **131.60 mm Hg**.
- Average cholesterol is approximately **246.5 mg/dl**.
- Approximately **32.8%** of patients have exercise-induced angina.
- Chest pain type, exercise-induced angina, oldpeak, maximum heart rate, number of major vessels, and thalassemia show notable associations with heart disease status.
- Patients with heart disease have a higher average maximum heart rate than patients without heart disease.
- Oldpeak also shows a substantial difference between the two target groups.
- Several clinical and demographic variables overlap considerably between patients with and without heart disease, indicating that heart disease cannot be explained reliably by a single factor.

---

## 🤖 Machine Learning

A **Logistic Regression** model was developed using the available features.

### Model Performance

| Metric | Result |
|---|---:|
| Accuracy | **80.33%** |
| Recall – Heart Disease | **85%** |
| Precision – Heart Disease | **80%** |
| F1 Score – Heart Disease | **82%** |

The model demonstrated reasonable predictive performance on the evaluated test set, particularly in identifying patients with heart disease.

> **Note:** This model is intended for analytical and educational purposes and should not be considered a clinical diagnostic system.

---

## 💡 Preventive Insights

Based on the observed patterns, potential preventive strategies include:

- Regular cardiovascular health screening.
- Monitoring blood pressure and cholesterol.
- Maintaining a heart-healthy diet and active lifestyle.
- Monitoring exercise-related symptoms.
- Identifying patients with multiple risk indicators for further assessment.
- Using a combination of demographic, clinical, and medical-history factors rather than relying on a single indicator.

---

## 🔬 Areas for Further Research

Future analysis could investigate:

- The relationship between exercise-induced angina and cardiovascular outcomes.
- The role of ST depression in heart disease risk.
- Relationships between different chest pain types and clinical measurements.
- The combined effect of major vessels and thalassemia.
- Interactions between multiple risk factors.
- Larger and longitudinal datasets containing patient follow-up information.

---

## 🛠️ Tools & Technologies

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Scikit-learn**
- **Jupyter Notebook**

---

## 📁 Project Structure

```text
Pulse-of-Prevention-Heart-Health-Analysis/
│
├── Heart_Health_Analysis.ipynb
├── heart.csv
├── README.md
└── .gitignore
