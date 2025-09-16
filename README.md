# 🚀 Telco Customer Churn Prediction System

## 📌 Project Overview

This project is part of Future Interns – Machine Learning Task 2.
The goal is to build a Churn Prediction System that identifies which telecom customers are likely to stop using the service.

Customer churn is a critical business problem since retaining an existing customer is cheaper than acquiring a new one.
We trained multiple ML models and integrated the results into an interactive Power BI dashboard for business storytelling.

We used Decision Tree, Random Forest, and XGBoost for training and evaluation.
The final results and churn insights are visualized through Power BI.

---

## 🔑 Key Features

- ✔ Data cleaning and preprocessing of telecom churn dataset
- ✔ Balanced dataset using SMOTE
- ✔ Trained 3 ML models → Decision Tree, Random Forest, XGBoost
- ✔ Cross-validation accuracy comparison across models
- ✔ Saved trained model and encoders as .pkl for reuse
- ✔ Feature importance analysis (Top 10 churn drivers)
- ✔ Interactive Power BI dashboard with KPIs, churn insights, and prediction interface

---

## 🛠️ Tools & Libraries

- Python → Data preprocessing, ML model training, saving models
- Pandas, NumPy, Scikit-learn → Data wrangling, encoding, evaluation
- XGBoost → Gradient boosting classifier
- Imbalanced-learn (SMOTE) → Handling class imbalance
- Seaborn & Matplotlib → EDA and feature visualization
- Power BI → Dashboard for visualization, KPIs, and prediction interface

---

## 📊 Dataset

We used the Telco Customer Churn dataset from Kaggle.

Key Columns:

- customerID → Unique identifier
- gender → Male / Female
- SeniorCitizen → 1 (Yes), 0 (No)
- Partner, Dependents → Family-related attributes
- tenure → Number of months as customer
- PhoneService, InternetService, OnlineSecurity, etc. → Service usage
- Contract → Month-to-month / One year / Two year
- PaymentMethod → Billing type
- MonthlyCharges, TotalCharges → Billing amounts
- Churn → Target variable (Yes = churned, No = retained)

📂 Dataset on Kaggle

---

## 🤖 Models & Performance

We trained and evaluated multiple classifiers with 5-fold cross-validation after balancing classes using SMOTE.

Model CV Accuracy:

- Decision Tree 0.787
- Random Forest 0.840
- XGBoost 0.835

Final model chosen: Random Forest

Accuracy: ~84%

Balanced performance on churn and non-churn classes

Saved as customer_churn_model.pkl for deployment

We also saved encoders.pkl for consistent categorical encoding during new predictions.

---

## 📈 Power BI Dashboard

The dashboard highlights:

- KPI Cards → Total Customers, Churned Customers, Churn Rate

- Pie Chart → Churn distribution

- Bar Charts → Churn by Contract, Churn by Internet Service, Churn by Payment Method

- Feature Importance → Top drivers of churn (e.g., Contract type, Tenure, MonthlyCharges)

- Model Results Table → Accuracy comparison of Decision Tree, Random Forest, and XGBoost

📂 Dashboard file: PowerBI Dashboard/Churn_Prediction_System.pbix

---

## 📂 Project Structure

### 📦 Telco Churn Prediction

```bash
FUTURE_ML_02
│
├── 📁 Dataset
│ └── Telco-Customer-Churn.csv
│
├── 📁 Output_Files
│ ├── cleaned_telco_churn.csv
│ ├── customer_churn_model.pkl
│ ├── encoders.pkl
│ ├── feature_importance.csv
│ ├── model_results.csv
│ └── test_predictions.csv
│
├── 📁 PowerBI Dashboard
│ └── Churn_Prediction_System.pbix
│
├── churn_prediction_system image.png # Screenshot of dashboard
├── churn-prediction-system.ipynb # Notebook with ML pipeline
└── README.md # Documentation
```

---

## 📌 How to Run

1. Model Training (Python)

   - Run churn-prediction-system.ipynb to:

   - Clean & preprocess data

   - Train models

   - Save outputs:

     - customer_churn_model.pkl (trained Random Forest)

     - encoders.pkl (label encoders)

     - model_results.csv (comparison of models)

     - feature_importance.csv (displays important features in the dataset)

     - test_predictions.csv (actual & predicted values for each record)

     - cleaned_telco_churn.csv (preprocessed & encoded data)

2. Power BI Dashboard

   - Open PowerBI Dashboard/Churn_Prediction_System.pbix in Power BI Desktop

   - Refresh data connections to point to saved CSVs

---

## 📜 Conclusion

This project demonstrates how Machine Learning + Business Dashboards can work together to:

Predict customer churn dynamically

Identify key churn drivers ( Gender, Contract type, Tenure, Monthly Charges)

Compare model performance

Provide actionable insights for decision-makers to reduce churn and increase customer retention
