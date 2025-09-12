# 📊 Telecom Customer Churn Prediction

---

## 🚀 Project Overview

This project builds a predictive model to identify telecom customers likely to churn. Predicting churn enables proactive engagement with high-risk customers, reducing attrition and improving business outcomes.

---

## 📂 Dataset

- **File:** `telecom_churn_synthetic.csv`  
- **Description:** Contains demographic data, service details, contract information, charges, and churn status for customers.

---

## 🧑‍💻 Methodology

The project follows a structured machine learning pipeline:

### 1. Data Loading and Description
- Load the dataset and explore its structure, data types, and summary statistics.

### 2. Exploratory Data Analysis (EDA)
- Visualize distributions of key features.
- **Univariate Analysis:** For numerical and categorical features.
- **Bivariate Analysis:** Explore relationships between features and churn.
- **Correlation Analysis:** For numerical features.

### 3. Feature Engineering & Preprocessing
- Encode categorical variables (One-hot and Label Encoding).
- Scale numerical features (StandardScaler).
- Create new interaction features based on EDA insights.

### 4. Model Building
- Train and evaluate various classification models:
  - Logistic Regression
  - Random Forest Classifier
  - XGBoost Classifier

### 5. Class Imbalance Handling
- Address imbalanced target (`Churn`) using:
  - `scale_pos_weight` (XGBoost)
  - SMOTE (Synthetic Minority Over-sampling Technique)

### 6. Cross-validation & Hyperparameter Tuning
- Use `GridSearchCV` with `StratifiedKFold` cross-validation.
- Focus on metrics relevant to imbalanced classification (e.g., recall).

### 7. Feature Importance & Interpretation
- Identify crucial features from the best-performing model.

### 8. Conclusion & Recommendations
- Summarize findings, evaluate model performance, and provide actionable business recommendations.

---

## 🔑 Key Findings

- **Imbalanced Dataset:** More non-churned than churned customers.
- **Major Churn Drivers:**
  - Month-to-month contracts & lower tenure.
  - Higher monthly charges.
  - Fiber optic internet service.
  - Electronic check payment method.
  - Interaction between tenure & contract type.

---

## 📈 Model Performance

- Multiple models evaluated using precision, recall, and F1-score.
- Handling class imbalance (SMOTE, scale_pos_weight) improved performance.
- Best models achieved strong recall for identifying churned customers.

---

## 💡 Recommendations

- Target retention programs for new and month-to-month customers.
- Offer incentives for longer-term contracts.
- Review pricing and high-charge/fiber plans.
- Investigate issues with electronic check payments.
- Promote value-added services (e.g., online security, streaming).
- Deploy churn prediction model for proactive retention.
- Continuously monitor and refine model & strategies.

---

## 🛠️ How to Run the Project

1. **Clone the repository:**  
   `git clone <repository_url>`

2. **Navigate to project directory:**  
   `cd telecom-churn-prediction`

3. **Install required libraries:**  
   - Create `requirements.txt` listing:  
     `pandas, numpy, matplotlib, seaborn, scikit-learn, xgboost, imbalanced-learn`
   - Install:  
     `pip install -r requirements.txt`

4. **Run the Jupyter Notebook or Python script** containing the analysis and code.

---

## 📁 Files in the Repository

- **`telecom_churn_synthetic.csv`**: The dataset.
- **`your_notebook_name.ipynb`**: Jupyter Notebook with code & analysis.
- **`README.md`**: Project overview (this file).

---

## ⚖️ License

*Specify your project's license here (e.g., MIT, Apache 2.0).*
