# Loan Approval Prediction

This project involves analyzing loan application data and building a machine learning model to predict whether a loan will be approved or rejected.

---

## 📌 Objective

To automate the loan approval process using machine learning by analyzing applicant and asset information.

---

## 🧾 Dataset Overview

- **Source:** `loan_approval_dataset.csv`
- **Total Records:** 4269
- **Features:** 13
  - Includes categorical and numerical fields like:
    - Education, Self Employment, Income, CIBIL Score, Asset Values
    - Loan Amount, Loan Term, Number of Dependents, etc.

---

## 🧹 Data Preprocessing

- Cleaned column names and string values
- Converted categorical fields to numeric:
  - `education`: Graduate (1), Not Graduate (0)
  - `self_employed`: Yes (1), No (0)
  - `loan_status`: Approved (1), Rejected (0)
- Created `total_assets` by summing:
  - Residential, Commercial, Luxury, Bank asset values
- Removed redundant columns like `loan_id`

---

## 📊 Exploratory Data Analysis (EDA)

### 📌 Univariate Analysis
- KDE plots for numerical features
- Count plots for categorical features

### 📌 Bivariate & Multivariate Analysis
- Boxplots for feature vs. loan status
- Count plots for categorical features vs. loan status
- Correlation heatmap for numerical features

---

## 🛠️ Feature Engineering

- Created new feature: `total_assets`
- Dropped asset columns after combination
- Removed non-predictive fields like `loan_id`

---

## 🤖 Model Building

### Model Used:
- **Logistic Regression**

### Steps:
1. Train-Test Split (80/20 stratified)
2. Scaled features using `StandardScaler`
3. Trained model using `LogisticRegression(max_iter=1000)`

---

## 📈 Evaluation

- **Accuracy:** 0.9110070257611241
- **Classification Report:** Includes Precision, Recall, F1-score
- **Confusion Matrix:** Visualized using seaborn

---

## 📌 Results

- The model performed well on binary classification
- Key predictors: Income, CIBIL score, Loan amount, Total assets

---

## 🚀 Future Work

- Try advanced models (e.g., Random Forest, XGBoost)
- Handle class imbalance (SMOTE, resampling)
- Feature selection for optimization
- Deploy using Flask or Streamlit

---

