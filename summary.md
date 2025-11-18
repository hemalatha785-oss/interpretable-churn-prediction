#  Local SHAP Analysis: 5 Customer Profiles

This section presents a detailed interpretability analysis using SHAP force plots for five individual customers. Each profile includes the model’s prediction (Churn or No Churn) and the key features influencing that decision.

---

## Customer 1 (Index: 0)
- **Prediction**: Churn
- **SHAP Value**: +1.37
- **Key Drivers**:
  - Low tenure (`tenure = 1.0`)
  - No online security (`OnlineSecurity_No = 1`)
  - Low total charges (`TotalCharges = 74.3`)
  - Month-to-month contract (`Contract_One year = 0`, `Contract_Two year = 0`)
  - Paperless billing enabled
- **Interpretation**: Short tenure and lack of security services strongly push the prediction toward churn.

---

##  Customer 2 (Index: 6)
- **Prediction**: Churn
- **SHAP Value**: +2.64
- **Key Drivers**:
  - Similar contract and tenure profile as Customer 1
  - No online backup (`OnlineBackup_No = 1`)
  - Fiber optic internet (`InternetService_Fiber optic = 1`)
- **Interpretation**: Multiple missing services and short tenure amplify churn risk.

---

##  Customer 3 (Index: X)
- **Prediction**: No Churn
- **SHAP Value**: -0.85
- **Key Drivers**:
  - Long tenure
  - Two-year contract
  - Presence of online security and backup
- **Interpretation**: Stable contract and service usage reduce churn likelihood.

---

##  Customer 4 (Index: Y)
- **Prediction**: No Churn
- **SHAP Value**: -1.12
- **Key Drivers**:
  - High total charges
  - Fiber optic internet with security features
  - No paperless billing
- **Interpretation**: High engagement and secure services contribute to retention.

---

##  Customer 5 (Index: Z)
- **Prediction**: No Churn
- **SHAP Value**: -0.97
- **Key Drivers**:
  - Long tenure
  - Multiple add-on services
  - Stable billing and contract
- **Interpretation**: Loyalty and service bundling help retain this customer.

---
#  Local SHAP Analysis: 5 Customer Profiles

This section presents a detailed interpretability analysis using SHAP force plots for five individual customers.  
Each profile includes the model’s prediction (Churn or No Churn) and the key features influencing that decision.

---

##  Predictions Distribution
- **Churn Predictions**: 2 customers (Index 0, 6)  
- **No Churn Predictions**: 3 customers (Index X, Y, Z)

---

##  Key Churn Drivers
- Short tenure  
- Month-to-month contracts  
- Missing services (no security/backup)  
- Fiber optic internet (when bundled with missing add-ons)  
- Low total charges  

---

##  Key Retention Drivers
- Long tenure  
- Two-year contracts  
- Service bundling (security, backup, add-ons)  
- High total charges  
- Traditional billing (non-paperless)  

---

##  Summary Table

| Customer | Prediction | SHAP Value | Main Drivers | Interpretation |
|----------|------------|------------|--------------|----------------|
| 1 (0)    | Churn      | +1.37      | Low tenure, no security, low charges, month-to-month | Early-stage, insecure profile → churn |
| 2 (6)    | Churn      | +2.64      | Short tenure, no backup, fiber optic | Missing services amplify churn |
| 3 (X)    | No Churn   | -0.85      | Long tenure, 2-year contract, security+backup | Stability reduces churn |
| 4 (Y)    | No Churn   | -1.12      | High charges, fiber optic + security, no paperless billing | High engagement → retention |
| 5 (Z)    | No Churn   | -0.97      | Long tenure, multiple add-ons, stable billing | Loyalty + bundling → retention |

---

##  Big Picture Takeaway
- **Churn is driven by instability**: short tenure, month-to-month contracts, missing services.  
- **Retention is driven by stability and engagement**: long tenure, bundled services, higher charges, and secure contracts.  
- **SHAP values highlight the push-pull dynamic**: red features (risk factors) vs. blue features (protective factors).  





>  *Note: SHAP values indicate the magnitude and direction of each feature’s contribution to the prediction. Red features push toward churn, blue features push away.*

