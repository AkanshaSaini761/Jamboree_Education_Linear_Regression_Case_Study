# 🎓 Jamboree Graduate Admission Prediction - Linear Regression Case Study

## 🏫 About Jamboree

**Jamboree** is a leading test prep and admissions counseling organization that helps students excel in exams like GMAT, GRE, and SAT. Recently, Jamboree introduced a feature to help students estimate their chances of getting into Ivy League graduate programs, especially from an Indian applicant's perspective.

## 🎯 Objective

This project analyzes historical applicant data to:

- Identify significant predictors of graduate admission chances.
- Understand interdependencies among factors like test scores, GPA, and research.
- Build a robust linear regression model to predict the **Chance of Admit**.
- Test assumptions and evaluate model performance for actionable insights.

## 📁 Dataset Overview

📄 **File:** [Jamboree_Admission.csv](https://github.com/AkanshaSaini761/Jamboree_Education_Linear_Regression_Case_Study/blob/main/Jamboree_Admission.csv) 

📊 **Records:** 500 rows, 9 columns

| Column Name         | Description                                           |
|---------------------|-------------------------------------------------------|
| `Serial No.`        | Unique row identifier (dropped in analysis)           |
| `GRE Score`         | GRE score (out of 340)                                |
| `TOEFL Score`       | TOEFL score (out of 120)                              |
| `University Rating` | Rating of the applied university (1 to 5)             |
| `SOP`               | Strength of Statement of Purpose (1 to 5)             |
| `LOR`               | Strength of Letter of Recommendation (1 to 5)         |
| `CGPA`              | Undergraduate GPA (out of 10)                         |
| `Research`          | Research experience (0: No, 1: Yes)                   |
| `Chance of Admit`   | Probability of admission (0 to 1)                     |

## 📊 Exploratory Goals

- **Data Cleaning & Preprocessing**  
  Drop ID columns, normalize values, rename mislabeled fields.

- **EDA (Univariate & Bivariate)**  
  Visualize distributions, analyze correlation via pairplots & heatmaps.

- **Model Building**  
  - Create base and reduced **linear regression** models using `statsmodels`.
  - Identify insignificant features using **p-values**.
  - Validate model assumptions: **multicollinearity, normality, homoscedasticity**.

- **Model Evaluation Metrics**  
  - Mean Absolute Error (MAE)  
  - Root Mean Square Error (RMSE)  
  - R-squared & Adjusted R-squared

## 📈 Key Insights

- **Strong Predictors**:  
  `GRE`, `TOEFL`, and `CGPA` significantly impact the **Chance of Admit**.

- **Moderate Predictors**:  
  `LOR` and `Research` show positive but smaller influence.

- **Insignificant Predictors**:  
  `SOP` and `University Rating` were found **statistically insignificant**.

- **Multicollinearity Issue**:  
  High VIF for `GRE` and `TOEFL`, suggesting **redundancy**.

- **Residual Analysis**:  
  - Mean residual ≈ 0 → **unbiased predictions**  
  - Homoscedasticity validated via **Goldfeld-Quandt test** (p > 0.05)  
  - Residuals nearly **normally distributed** (checked via histogram and Q-Q plot)

- **Model Fit**:
  - R² = **0.82**, Adjusted R² = **0.818**
  - MAE = **0.043**, RMSE = **0.059**

## ✅ Recommendations

1. **Focus on Test Prep**  
   Enhance coaching for GRE & TOEFL, as they are major contributors to admission success.

2. **Support Academic Performance**  
   Offer GPA improvement plans via tutoring and study workshops.

3. **Encourage Research Participation**  
   Facilitate student research via university tie-ups to strengthen applicant profiles.

4. **Improve Application Materials**  
   Help students write compelling SOPs and secure strong LORs through structured guidance.

5. **Enhance the Model**  
   Introduce new variables like work experience, extracurriculars, and internships to improve prediction accuracy.

## 🛠️ Tools & Libraries Used

- **Python**: `pandas`, `numpy`, `matplotlib`, `seaborn`
- **Statistical Analysis**: `scipy`, `statsmodels`
- **Feature Scaling**: `sklearn.preprocessing` (`MinMaxScaler`)
- **Model Evaluation**: `sklearn.metrics`
- **Notebook Environment**: Jupyter Notebook

## 📄 Report

📎 [Download Full Report (PDF)](https://github.com/AkanshaSaini761/Jamboree_Education_Linear_Regression_Case_Study/blob/main/Jamboree_education_case_study_akansha_saini.pdf)

Contains detailed data exploration, statistical modeling, assumption validation, visualizations, and interpretation.
