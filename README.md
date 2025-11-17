# Interpretable-churn-prediction
Interpretable Machine Learning project on Customer Churn Prediction using SHAP analysis for global and local interpretability.  
#  Customer Churn Prediction with SHAP Interpretability

This project builds a machine learning model to predict customer churn using a telecommunications dataset. It emphasizes **model interpretability** using SHAP (SHapley Additive exPlanations), providing both global and local insights into why customers are predicted to churn.

---

##  Objectives

- Predict customer churn using XGBoost
- Evaluate model performance using AUC and F1-score
- Apply SHAP to explain global feature importance
- Generate SHAP force plots for individual customer predictions
- Identify counter-intuitive feature interactions
```
# Customer Churn Prediction with SHAP Interpretability

This project builds a high-performing machine learning model to predict customer churn using a telecommunications dataset. Beyond predictive accuracy, it emphasizes **model interpretability** using SHAP (SHapley Additive exPlanations) to explain both global and individual predictions.

---

##  Dataset Overview

- **Source**: Anonymized telco customer dataset
- **Target Variable**: `Churn` (binary: Yes = 1, No = 0)
- **Features**: Demographics, service usage, contract details, billing information

---

## 🧹 Data Preprocessing

- Removed irrelevant columns (`customerID`, `Unnamed: 0`)
- Handled missing values:
  - Converted blank strings to NaN
  - Imputed `TotalCharges` with median
  - Filled categorical NaNs with mode
- Encoded categorical variables using one-hot encoding
- Binary encoded target column: `'Yes' → 1`, `'No' → 0`

---

## Model Training

- **Algorithm**: XGBoost Classifier
- **Hyperparameter Tuning**: GridSearchCV with 3-fold cross-validation
- **Parameters Tuned**:
  - `n_estimators = 100`
  - `max_depth = 3`
  - `learning_rate = 0.1`
- **Train/Test Split**: 80/20

---

## 📈 Model Evaluation

```python
Classification Report:
              precision    recall  f1-score   support
       0.0        0.78      0.89      0.83       288
       1.0        0.61      0.40      0.49       121

    accuracy                            0.75       409
   macro avg        0.70      0.65      0.66       409
weighted avg        0.73      0.75      0.73       409

AUC Score: 0.82
F1 Score: 0.49


**Repository Structure**

interpretable-churn-prediction-project/
│
├── project.ipynb
├── report.md
├── requirements.txt
├── readme.md
|__ summary.md
-
└── plots/
    |--shap summary plot.png
    ├── customer1.png
    ├── customer2.png
    ├── customer3.png
    ├── customer4.png
    └── customer5.png
```

## Models Used
- **XGBoost Classifier**


### Evaluation Metrics
- **AUC Score**
- **F1 Score**

---

## Interpretability
This project uses **SHAP** for:
 SHAP Interpretation
** Global Interpretability  **
** Local Interpretability  **
#  Model Interpretability with SHAP

Interpretability is critical in customer churn prediction, as it allows us to understand **why** the model makes certain decisions. SHAP (SHapley Additive exPlanations) provides two complementary perspectives:

---

##  Global Interpretability

Global interpretability explains the **overall behavior of the model** across the entire dataset.

- **Definition**: Identifies which features are most important in driving churn predictions for the population as a whole.
- **Method**: SHAP summary plots aggregate feature contributions across all customers.
- **Insights**:
  - Short **tenure** strongly increases churn risk.
  - **Month-to-month contracts** are highly associated with churn, while long-term contracts reduce risk.
  - Lack of **OnlineSecurity** and **TechSupport** services consistently push predictions toward churn.
  - **High monthly charges** combined with low total charges (new customers) are linked to churn.
- **Use Case**: Helps businesses understand the main drivers of churn and design global retention strategies.

---

##  Local Interpretability

Local interpretability explains the **prediction for an individual customer**.

- **Definition**: Breaks down how each feature contributed to a single customer’s churn prediction.
- **Method**: SHAP force plots and dependence plots show feature-level impacts for one customer at a time.
- **Insights**:
  - For a churner with **low tenure** and **no security services**, SHAP highlights these as strong positive contributors to churn.
  - For a loyal customer with a **two-year contract** and multiple add-on services, SHAP shows negative contributions that reduce churn probability.
- **Use Case**: Enables personalized retention actions, such as offering discounts or service upgrades to at-risk customers.

---

>  **Summary**:  
Global interpretability answers *“What drives churn overall?”*  
Local interpretability answers *“Why did this specific customer churn (or stay)?
---


## 🛠 How to Run the Project

### Option 1 — Google Colab (Recommended)
1. Upload the dataset and notebook  
2. Install packages using `requirements.txt`  
3. Run cells from top to bottom  

### Option 2 — Local Machine
```
pip install -r requirements.txt
jupyter notebook project.ipynb
```

---

### Key Insights
- Customers with **Month-to-Month contracts** show higher churn rates.
- **High MonthlyCharges** are positively correlated with churn.
- **Longer Tenure** reduces churn likelihood.

### Visualizations
- SHAP Summary Plot
- SHAP Force Plot

