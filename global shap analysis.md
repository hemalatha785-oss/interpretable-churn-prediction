#  Global SHAP Analysis Summary

To understand the overall drivers of customer churn, we applied SHAP (SHapley Additive exPlanations) to the trained classification model. The SHAP summary plot provides a ranked visualization of feature importance and the direction of their impact on the model’s predictions.

##  Top Features Influencing Churn

- **tenure**  
  Customers with shorter tenure are more likely to churn.  
  SHAP values show a strong negative correlation: lower tenure pushes predictions toward churn.

- **Contract type**  
  Month-to-month contracts significantly increase churn risk.  
  Longer-term contracts (one or two years) reduce churn likelihood.

- **OnlineSecurity and TechSupport**  
  Absence of these services contributes positively to churn predictions.  
  Their presence acts as a retention factor.

- **InternetService**  
  Customers using fiber optic internet show higher churn tendencies compared to DSL or no internet.

- **MonthlyCharges and TotalCharges**  
  High monthly charges combined with low total charges (indicating short tenure) are associated with churn.  
  Customers with high total charges and long tenure are less likely to churn.

##  SHAP Summary Plot Interpretation

- The **horizontal axis** represents SHAP values (impact on model output).
- Each **dot** represents a customer; color indicates feature value (red = high, blue = low).
- Features are sorted by importance from top to bottom.
- **Red dots on the right** (positive SHAP values) indicate high feature values pushing toward churn.
- **Blue dots on the left** (negative SHAP values) indicate low feature values pulling away from churn.

##  Insights

- SHAP reveals **non-linear effects**: for example, tenure has a steep drop-off in churn risk after a certain threshold.
- It also highlights **interactions**: customers with fiber optic internet and no security services are at higher risk.
- These patterns would be missed by traditional feature importance metrics like Gini or permutation importance.

> *Note: SHAP summary plots provide global interpretability by aggregating feature contributions across all predictions.*
