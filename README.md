#**Business Problem**

Customer churn poses a significant risk for financial institutions, resulting in revenue loss. This project is of utmost importance for the banking institution, as it has the potential to enhance customer retention and drive profitability. By creating a reliable churn classification model, we can help institutions proactively address customer concerns and foster lasting relationships. The model enables targeted retention strategies, boosting customer satisfaction and loyalty.


In this comprehensive analysis, the focus was on identifying the factors contributing to customer churn within financial institutions, specifically in the credit card system, using machine learning models. The process involved various stages, including exploratory data analysis, data preprocessing, classifier evaluation, feature importance selection, and hyperparameter tuning. Among the 10 classifiers evaluated, the Light GBM model emerged as the top performer, boasting the highest recall score of 0.893 and the highest F1 score of 0.888. Further optimization through a grid search enhanced its performance.

Moreover, the analysis pinpointed six key features that significantly influence customer churn in the credit card system: 'Total_Trans_Ct,' 'Total_Trans_Amt,' 'Total_Revolving_Bal,' 'Total_Ct_Chng_Q4_Q1,' 'Avg_Utilization_Ratio,' and 'Total_Relationship_Count.' By strategically monitoring and addressing these variables, financial institutions can effectively mitigate churn and improve customer retention rates. After eliminating insignificant features, the model achieved a recall score of 0.889, and the learning curve demonstrated a significant reduction in the gap between the training set (Recall: 0.96) and the test set (Recall: 1), indicating improved generalization.

This project provides valuable insights and recommendations for financial institutions to combat customer churn, ultimately leading to enhanced customer retention and profitability in the credit card system.




#**Dataset**

The credit card churn dataset consists of 10,000 customers and 18 features, including age, salary, marital_status, credit card limit, and credit card category, among others. With only 16.07% of customers having churned, the dataset presents a class imbalance challenge, making it difficult to train the model to predict churning customers effectively.


Data source: https://www.kaggle.com/datasets/sakshigoyal7/credit-card-customers?datasetId=982921&sortBy=voteCount&select=BankChurners.csv

The features in the data set are as follows:
- CLIENTNUM - Client number. Unique identifier for the customer holding the account.
- Attrition_Flag - Internal event (customer activity) variable - if the account is closed then 1 else 0.
- Customer_Age - Demographic variable - Customer's Age in Years.
- Gender - Demographic variable - M=Male, F=Female.
- Dependent_count - Demographic variable - Number of dependents.
- Education_Level - Demographic variable - Educational Qualification of the account holder (example: high school).
- Marital_Status - Demographic variable - Married, Single, Divorced, Unknown.
- Income_Category - Demographic variable - Annual Income Category of the account holder.
- Card_Category - Product Variable - Type of Card (Blue, Silver, Gold, Platinum).
- Months_on_book - Period of relationship with bank.
- Total_Relationship_Count - Total no. of products held by the customer.
- Months_Inactive_12_mon - No. of months inactive in the last 12 months.
- Contacts_Count_12_mon - No. of Contacts in the last 12 months.
- Credit_Limit - Credit Limit on the Credit Card.
- Total_Revolving_Bal - Total Revolving Balance on the Credit Card.
- Avg_Open_To_Buy - Open to Buy Credit Line (Average of last 12 months).
- Total_Amt_Chng_Q4_Q1 - Open to Buy Credit Line (Average of last 12 months).
- Total_Trans_Amt - Total Transaction Amount (Last 12 months).
- Total_Trans_Ct - Total Transaction Count (Last 12 months).
- Total_Ct_Chng_Q4_Q1 - Change in Transaction Count (Q4 over Q1).
- Avg_Utilization_Ratio - Average Card Utilization Ratio.

#**Metric Selection**
In our classification model, we deemed “Recall” as the principal evaluation metric. Recall measures the proportion of true positive predictions among all actual positive instances, as well as the proportion of true negative predictions among all actual negative instances. When using recall, we aim to accurately assess the model's performance in correctly identifying the false negatives, that is to what extent the " attrite customers" is identified as "existing customers". Additionally, when presenting the leaderboard and learning curve, F1 is introduced as supplementary references as it maintains a balance between the precision and recall.
