# Churn Prediction to Drive Customer Retention Through Temporal Behavioral Modeling
The goal of this project is to develop a churn prediction system for FoodCorp in order to surface insights that support smarter retention strategies through early identification of at-risk customers.
## Dataset Structure
![image](https://github.com/user-attachments/assets/07ef2ccc-3e39-42ea-a048-70a4f2fc05e7)

## Insights Summary
In order to evaluate churn prediction performance, we focused on the following key metrics:

- Churn Rate: The percentage of customers who did not make a purchase within 35 days (approx. 30%).
- ROC AUC Score: A measure of the model's ability to distinguish churners from non-churners.
- Recall at Threshold 0.3: The percentage of actual churners correctly identified by the model.
- Top Predictive Features: The features that most strongly contributed to churn prediction.

### Churn Rate
Churn was defined as 35+ days of inactivity, classifying around 30% of customers as churners.
This threshold balanced early detection with a practical intervention window, aligning with customer behavior patterns.

### ROC AUC Score
The Random Forest model achieved a strong ROC AUC of 0.8014, indicating high predictive power.
This was slightly higher than both XGBoost (0.7920) and Logistic Regression (0.7503), confirming the strength of tree-based models for this task.

### Recall at Threshold 0.3
Using a classification threshold of 0.3, the model correctly identified 74.04% of actual churners.
This threshold was selected to prioritize recall, as the cost of missing a churner outweighs the cost of a false positive.

### Top Predictive Features
The most important predictors of churn were lagged spending and product diversity over recent weeks.
Features like recency and frequency contributed little and were removed, leading to a simpler and slightly more accurate model.

### Key Takeaways
Churners show early warning signs such as declining spend, low product diversity, and irregular visit frequency. These behavioral shifts can be monitored and used to trigger timely retention efforts.

Non-churners exhibit stable, frequent shopping and increasing variety in their purchases. Encouraging product exploration and maintaining regular engagement can help reinforce loyalty.
