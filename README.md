# Telco Customer Churn Analysis

## Problem Statement
In the telecom industry, customers are able to choose from multiple service providers and actively switch from one operator to another. In this highly competitive market, the telecommunications industry experiences an average of 15-25% annual churn rate. Given the fact that it costs 5-10 times more to acquire a new customer than to retain an existing one, customer retention has now become even more important than customer acquisition.

For many incumbent operators, retaining high profitable customers is the number one business goal.

To reduce customer churn, telecom companies need to predict which customers are at high risk of churn.

In this project, we will analyse customer-level data of a leading telecom firm, build predictive models to identify customers at high risk of churn and identify the main indicators of churn.

## Overview and Dataset Description
The Telco Customer Churn dataset includes data points related to customer demographics, account details, services subscribed, and contract type. The primary goal is to identify patterns that predict customer churn (whether a customer will leave the service).

### Key Columns:
- **CustomerID**: Unique identifier for each customer.
- **Demographics**: Age, gender, etc.
- **Services**: Type of services such as internet, phone, streaming services.
- **Account Information**: Contract type (month-to-month, one year, two years), payment method, tenure, total charges, and monthly charges.
- **Churn**: Whether or not the customer has churned (binary outcome).

## Technologies Used
- **Python**: Programming language.
- **Pandas**: Data manipulation and analysis.
- **NumPy**: Numerical computing.
- **Matplotlib**: Data visualization.
- **Seaborn**: Statistical data visualization.
- **Scikit-Learn**: Machine learning.

## Initial Insights from Exploratory Data Analysis (EDA)
### Distribution Analysis:
- The **TotalCharges** column showed cases with missing or zero values, which were addressed by imputing or recalculating them based on the customer's tenure and monthly charges.
- Histograms of tenure and monthly charges revealed varied distribution, indicating different user behavior profiles.

### Demographic Patterns:
- Certain age groups and genders showed higher churn rates. For example, younger customers might churn more frequently compared to older, long-term users.

## Key Correlations and Factors Influencing Churn
### High Correlation with Contract Type:
- Customers on a month-to-month contract exhibited higher churn compared to those on longer-term contracts.

### Payment Method:
- Payment methods like automatic bank payments were linked to lower churn rates, while manual payment methods correlated with higher churn.

### Internet Service:
- Specific internet service types (e.g., Fiber Optic) showed a higher association with churn due to potential service reliability issues or competitive alternatives.

### Tenure and Charges:
- Higher tenure was inversely related to churn, while high monthly charges without proportional tenure (newer customers with high bills) often indicated higher churn rates.

## Visual Analysis
### Churn vs. Non-Churn Comparison:
- Box plots and violin plots showed that customers with higher monthly charges tended to churn more.
- Heatmaps helped identify correlations between numerical features, confirming stronger relationships between variables such as tenure and TotalCharges with Churn.

### Categorical Analysis:
- Bar charts depicting churn by service type (e.g., tech support availability, online security) suggested that customers lacking these services were more prone to churn.

## Model Insights (If Predictive Modeling Was Conducted)
### Feature Importance:
- Random Forest or Logistic Regression models often highlight contract type, monthly charges, and tenure as top predictive features.

### Model Performance:
- Confusion matrices and ROC curves from these models may show strong precision and recall values, aiding in targeted churn mitigation strategies.

## Recommendations for Reducing Churn
1. **Incentivize Long-Term Contracts**:
   - Provide attractive offers for customers to switch from month-to-month plans to annual plans.
2. **Improve Service Reliability**:
   - Address issues related to internet service reliability, especially for high-churn services like Fiber Optic.
3. **Customized Offers**:
   - Identify high-risk customers (e.g., high monthly bills, low tenure) and offer personalized retention packages.
4. **Enhanced Payment Flexibility**:
   - Streamline and promote automatic payment options to reduce churn associated with manual payment methods.

## Conclusion
The Telco Customer Churn analysis highlights actionable insights to understand customer behavior and reduce churn rates. By focusing on key factors such as contract type, payment methods, and service quality, the company can implement targeted strategies to improve retention.
