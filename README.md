# credit-risk-scoring

---

## 🎯 Goal

To develop a robust machine learning pipeline that can predict a customer's credit risk and help banks make better lending decisions.

---

## 📊 Dataset Description

- **Source:** UCI Statlog (German Credit Data)
- **Instances:** 1000
- **Features:** 20 (categorical and numerical)
- **Target:** 
  - 0 = Good Credit
  - 1 = Bad Credit

---

## 🧪 Process Overview

1. **Exploratory Data Analysis (EDA):**
   - Missing value check
   - Class balance analysis
   - Visualizations for numerical and categorical features

2. **Data Preprocessing:**
   - Label Encoding for categorical features
   - Feature scaling using `StandardScaler`

3. **Modeling:**
   - Models used:
     - Logistic Regression
     - Random Forest
     - XGBoost (with and without hyperparameter tuning)
   - Evaluation metrics:
     - Confusion Matrix
     - Precision, Recall, F1-score
     - ROC-AUC

4. **Model Selection:**
   - XGBoost with hyperparameter tuning selected as final model due to strong ROC-AUC and balanced performance

5. **Feature Importance:**
   - Top features influencing credit risk identified and visualized

---

## 🏁 Results Summary

| Model              | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|-------------------|----------|-----------|--------|----------|---------|
| LogisticRegression | 0.745    | 0.55 (Bad) | 0.78   | 0.65     | 0.81    |
| Random Forest      | 0.76     | 0.71 (Bad) | 0.33   | 0.45     | 0.79    |
| XGBoost (Tuned)    | ✅ 0.75  | 0.58 (Bad) | 0.60   | 0.59     | ✅ 0.81 |

---

## ✅ Final Output

- 📁 `final_credit_risk_data.csv`: Final dataset with scaled and encoded features + human-readable `target`
- 📦 `final_credit_risk_xgb_model.pkl`: Trained XGBoost model (joblib)
- 📓 `Credit_Risk_Analysis.ipynb`: Full notebook with code, visuals, and evaluations

---

## 💡 Future Improvements

- Use SMOTE or advanced resampling for imbalanced data
- Try LightGBM or CatBoost for faster performance
- Deploy the model via Flask or FastAPI
- Schedule retraining pipelines using Airflow or Cron

---






