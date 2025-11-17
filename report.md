# 📊 Customer Churn Prediction Report

## 1. Introduction
Customer churn prediction is a critical task for businesses aiming to retain customers.  
This report outlines the dataset, preprocessing steps, model training, evaluation, and interpretability analysis using SHAP.

---

## 2. Dataset
- **Source**: [Insert dataset link or description]
- **Size**: [Number of rows, columns]
- **Features**:  
  - Demographics (e.g., age, gender, location)  
  - Service usage (e.g., calls, internet, subscriptions)  
  - Contract details (e.g., tenure, payment method)

---

## 3. Data Preprocessing
- Missing value handling  
- Encoding categorical variables  
- Feature scaling  
- Train-test split (e.g., 80/20)

---

## 4. Model Training
- Algorithms used: Logistic Regression, Random Forest, XGBoost  
- Hyperparameter tuning with GridSearchCV  
- Evaluation metrics: Accuracy, Precision, Recall, F1-score, ROC-AUC

---

## 5. Results
| Model              | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|--------------------|----------|-----------|--------|----------|---------|
| Logistic Regression| 0.82     | 0.79      | 0.75   | 0.77     | 0.84    |
| Random Forest      | 0.87     | 0.85      | 0.83   | 0.84     | 0.89    |
| XGBoost            | 0.89     | 0.87      | 0.85   | 0.86     | 0.91    |

---

## 6. Interpretability (SHAP Analysis)
- SHAP values highlight the most influential features driving churn.  
- Key drivers:  
  - Contract type  
  - Monthly charges  
  - Tenure length  

---

## 7. Conclusion
- XGBoost performed best with ROC-AUC of 0.91.  
- SHAP analysis provided actionable insights for customer retention strategies.  
- Future work:  
  - Explore deep learning models  
  - Incorporate time-series data  
  - Automate retraining pipeline

---

## 8. References
- [SHAP Documentation](https://shap.readthedocs.io/en/latest/)  
- [Scikit-learn](https://scikit-learn.org/stable/)  
- [XGBoost](https://xgboost.readthedocs.io/en/stable/)  

