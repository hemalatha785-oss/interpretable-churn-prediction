
#  Interpretable Customer Churn Prediction

##  Abstract
This project aims to predict customer churn using the **XGBoost Classifier** and interpret model decisions using **SHAP (SHapley Additive exPlanations)**. The goal is to provide actionable insights for customer retention by understanding which features most influence churn.

---

##  Introduction
Customer churn poses a major challenge for subscription-based businesses. Predicting churn allows companies to proactively engage at-risk customers.  
This project combines high-performance modeling with interpretability to ensure transparency and trust in predictions.

---

##  Dataset
- **Source:** Telco customer churn dataset  
- **Size:** 7,043 records, 21 features  
- **Target:** `Churn` (Yes/No → 1/0)  
- **Preprocessing:**
  - Replaced blank strings with NaN
  - Converted `TotalCharges` to numeric and filled missing values with median
  - Imputed categorical missing values with mode
  - One-hot encoded categorical features
  - Dropped irrelevant columns (`customerID`, `Unnamed: 0`)

---
##  Data Preprocessing
- Missing value handling  
- Encoding categorical variables  
- Feature scaling  
- Train-test split (e.g., 80/20)
  
---

##  Model Training
- Algorithms used: Logistic Regression, Random Forest, XGBoost  
- Hyperparameter tuning with GridSearchCV  
- Evaluation metrics: Accuracy, Precision, Recall, F1-score, ROC-AUC
---
##  Modeling Approach
###  Model Used
- **XGBoost Classifier** with GridSearchCV for hyperparameter tuning  
- Parameters:
  - `n_estimators`: 100  
  - `max_depth`: 3  
  - `learning_rate`: 0.1  
---
###  Evaluation Metrics
- **F1 Score:** 0.49  
- **AUC Score:** 0.82  
- **Classification Report:**
  - Precision (Churn): 0.61  
  - Recall (Churn): 0.40  
  - Accuracy: 75%

---

##  Interpretability (SHAP Analysis)
- SHAP values highlight the most influential features driving churn.  
- Key drivers:  
  - Contract type  
  - Monthly charges  
  - Tenure length  


##  Results
| Model              | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|--------------------|----------|-----------|--------|----------|---------|
| Logistic Regression| 0.82     | 0.79      | 0.75   | 0.77     | 0.84    |
| Random Forest      | 0.87     | 0.85      | 0.83   | 0.84     | 0.89    |
| XGBoost            | 0.89     | 0.87      | 0.85   | 0.86     | 0.91    |



##  Prediction Summary
```python
Predicted_Label
No Churn    329
Churn        80

```

##  Conclusion
- XGBoost performed best with ROC-AUC of 0.91.  
- SHAP analysis provided actionable insights for customer retention strategies.  
- Future work:  
  - Explore deep learning models  
  - Incorporate time-series data  
  - Automate retraining pipeline

---

##  References
- [SHAP Documentation](https://shap.readthedocs.io/en/latest/)  
- [Scikit-learn](https://scikit-learn.org/stable/)  
- [XGBoost](https://xgboost.readthedocs.io/en/stable/)  

