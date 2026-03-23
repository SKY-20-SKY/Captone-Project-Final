# Telecomm Customer Churn Prediction

## Project Overview
Customer churn poses a significant threat to revenue and growth in the telecommunications sector. This project identifies high-risk customers and uncovers the underlying drivers of churn to develop data-driven retention strategies. Using machine learning, we built a predictive model to forecast churn and provide actionable business insights for proactive engagement.

## Data Analysis: Key Findings
Our Exploratory Data Analysis revealed several critical factors that correlate strongly with customer loss:

* **Contract Type:** Customers on month-to-month contracts exhibit the highest risk, indicating a lack of long-term commitment.
* **Internet Service:** Fiber optic users show a significantly high churn rate of 41.89%, suggesting potential dissatisfaction with service quality or pricing.
* **Payment Method:** Users paying via Electronic Check have a considerably higher churn rate compared to other payment methods.
* **Ancillary Services:** Lack of "Online Security" or "Tech Support" significantly increases churn probability (both over 41%).
* **Tenure and Charges:** Shorter-tenure customers and those with higher monthly charges are primary churn risks.
* **Demographics:** While gender has little impact, customers without partners or dependents tend to churn more frequently.
* **Outliers:** Outliers in Senior Citizens were retained as their inclusion slightly improved model accuracy, capturing essential behavioral signals.

## Model Performance & Selection
I evaluated several tuned models, including Logistic Regression, KNN, Decision Trees, and SVM. 

### **The Tuned Logistic Regression Model**
This was selected as it achieved a test accuracy of **0.82** with a balanced **Precision (0.70)** and **F1-score (0.63)**. While the SVM model showed similar performance, Logistic Regression offers significantly faster training times, which is important for frequent model updates.

### **The Impact of SMOTE**
I implemented SMOTE (Synthetic Minority Over-sampling Technique) to address class imbalance. While it successfully increased recall (identifying more total churners), it led to a decrease in overall accuracy and precision by misclassifying stable customers as churners. For a balanced business view, the original tuned Logistic Regression remains the preferred model.

## Actionable Business Recommendations
To reduce churn effectively, the following strategies are recommended:

1. **Targeted Retention Programs:** Focus on deploying loyalty offers to customers with month-to-month contracts and Fiber Optic service to incentivize long-term commitments.
2. **Payment Method Incentives:** Provide small discounts or incentives to move customers from Electronic Checks to automated electronic payments, improving payment reliability.
3. **Value-Add Service Promotion:** Educate customers on the advantages of "Online Security" and "Tech Support" during onboarding.
4. **Service Quality Audit:** Conduct a deep dive into Fiber Optic service disruptions to address the high churn rate in this premium segment.

## Deployment and Next Steps
* **Model Integration:** Implement the Logistic Regression model to score existing customers in real-time and trigger proactive retention alerts for those at high risk.
* **Continuous Monitoring:** Regularly monitor model performance metrics (Accuracy, Precision, Recall) to account for shifts in customer behavior due to economic or market changes.
* **Cost-Benefit Analysis:** Conduct a "Save Rate" analysis to ensure that the financial cost of retention efforts is justified by the lifetime value of the customers saved.
