# Interpretable-churn-prediction
Interpretable Machine Learning project on Customer Churn Prediction using SHAP analysis for global and local interpretability.  
# 📉 Customer Churn Prediction with SHAP Interpretability

This project builds a machine learning model to predict customer churn using a telecommunications dataset. It emphasizes **model interpretability** using SHAP (SHapley Additive exPlanations), providing both global and local insights into why customers are predicted to churn.

---

## 🧠 Objectives

- Predict customer churn using XGBoost
- Evaluate model performance using AUC and F1-score
- Apply SHAP to explain global feature importance
- Generate SHAP force plots for individual customer predictions
- Identify counter-intuitive feature interactions
```
interpretable-churn-prediction-project/
│
├── project.ipynb
├── report.md
├── requirements.txt
├── readme.md
│
└── plots/
    |--shap summary plot.png
    ├── customer1.png
    ├── customer2.png
    ├── customer3.png
    ├── customer4.png
    └── customer5.png
```

## 📊 Models Used
- **XGBoost Classifier**


### Evaluation Metrics
- **AUC Score**
- **F1 Score**

---

## 🔍 Interpretability
This project uses **SHAP** for:
🔍 SHAP Interpretation
** Global Interpretability  **
** Local Interpretability  **



---

## 📂 Dataset

### Source
- [Telco Customer Churn Dataset](https://www.kaggle.com/blastchar/telco-customer-churn)

### Features
| Column Name               | Description                                                  |
|---------------------------|--------------------------------------------------------------|

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

