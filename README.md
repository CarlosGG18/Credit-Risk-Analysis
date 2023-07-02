# Credit Risk Analysis
![image](https://github.com/CarlosGG18/Credit-Risk-Analysis/assets/117116368/08d9363f-c398-479d-b68f-119079d38ab1)

This project focuses on analyzing credit risk in financial institutions and developing predictive models to assess the probability of default for potential borrowers. The dataset used for this analysis contains various features related to borrowers' characteristics and loan details.

## Dataset Description
The Credit Risk dataset consists of the following features:

`person_age`: Age of the borrower
 
`person_income`: Annual income of the borrower

`person_home_ownership`: Home ownership status of the borrower

`person_emp_length`: Employment length of the borrower in years

`loan_intent`: Purpose or intent of the loan

`loan_grade`: Grade assigned to the loan

`loan_amnt`: Loan amount

`loan_int_rate`: Interest rate of the loan

`loan_status`: Loan status (0 indicates non-default, 1 indicates default)

`loan_percent_income`: Percentage of income represented by the loan amount

`cb_person_default_on_file`: Historical default status of the borrower

`cb_person_cred_hist_length`: Length of the borrower's credit history

## Exploratory Data Analysis Findings
These numbers reflect the distribution of loan intents within the given dataset and provide insights into the different purposes for which borrowers are seeking loans. The variations in quantities among the categories could be influenced by factors such as market demand, economic conditions, promotional offers, or specific needs of the borrower population.

![loan_intent](https://github.com/CarlosGG18/Credit-Risk-Analysis/assets/117116368/f80a8948-9a09-4f8d-b7ab-318d88a1bd60)


| loan_grade_dist                                     | scatter_plot                                     |
|-----------------------------------------------------|--------------------------------------------------|
| ![loan_grade_dist](https://github.com/CarlosGG18/Credit-Risk-Analysis/assets/117116368/7d371fec-3f62-44d4-8878-1f4838b0645f)|![scatter_plot](https://github.com/CarlosGG18/Credit-Risk-Analysis/assets/117116368/d4d64b02-1fcf-46d5-bd55-880020b08fd5) |


There is a strong correlation between `person_age` and `cb_person_cred_hist_length`. As borrowers get older, their credit history length tends to increase as well.

The `loan_int_rate` shows a significant correlation with `loan_grade`. As the loan grade gets closer to (F), the interest rate also tends to increase.

`cb_person_default_on_file` is correlated with both `loan_grade` and `loan_int_rate`.

The target variable, `loan_status`, is correlated with `person_home_ownership`,` loan_int_rate`, `and loan_grade`.
![heatmap](https://github.com/CarlosGG18/Credit-Risk-Analysis/assets/117116368/1dc6094d-79b4-4bc3-b4d0-7324d49cc938)


## Model Results
The models trained and evaluated: Logistic Regression,Linear Regression, Random Forest, Support Vector Machine, Light GBM, Ridge Classifier, and XGBoost Classifier. Here are the performance metrics for each model:

| Model                   | Accuracy Score | Precision Score | Recall Score | F1 Score |
|-------------------------|----------------|-----------------|--------------|----------|
| Logistic Regression     | 0.784          | 0.500           | 0.778        | 0.609    |
| Ridge Classifier        |                |                 |              |          |
| - Train Set             | 0.79           | 0.52            | 0.78         | 0.61     |
| - Test Set              | 0.78           | 0.50            | 0.75         | 0.60     |
| Random Forest           |                |                 |              |          |
| - Train Set             | 0.79           | 0.51            | 0.77         | 0.61     |
| - Test Set              | 0.78           | 0.50            | 0.75         | 0.60     | 
| Ridge Classifier        |                |                 |              |          |
| - Train Set             | 0.97           | 0.99            | 0.86         | 0.92     |
| - Test Set              | 0.93           | 0.91            | 0.72         | 0.80     | 
| XGBoost                 |                |                 |              |          |
| - Train Set             | 0.98           | 0.99            | 0.91         | 0.95     |
| - Test Set              | 0.94           | 0.94            | 0.73         | 0.82     |
| LightGBM                |                |                 |              |          |
| - Train Set             | 0.94           | 0.98            | 0.74         | 0.84     |
| - Test Set              | 0.93           | 0.97            | 0.71         | 0.82     | 


**XGBoost Classifier:**
XGBoost is an advanced gradient boosting algorithm that uses an ensemble of decision trees to make predictions. It is known for its powerful performance and flexibility in handling complex datasets. The algorithm optimizes a loss function by iteratively adding decision trees to the ensemble, minimizing the errors made by the previous trees. This allows XGBoost to capture complex relationships and interactions among the features, leading to improved predictive accuracy.

The use case of XGBoost in analyzing credit risk and predicting the probability of default is well-suited. By utilizing a large number of decision trees, XGBoost can effectively capture the patterns and dependencies present in the borrower characteristics and loan details, enabling it to make accurate predictions. The high accuracy, precision, recall, and F1 scores on both the train and test sets indicate that XGBoost has good performance and generalization ability for this task.

## Conclusion
The Logistic Regression model has relatively lower performance compared to the other models across multiple metrics, indicating that it may not be the most effective choice for this specific task.

The Ridge Classifier, Random Forest, XGBoost, and LightGBM models show similar performance across various metrics. They generally achieve higher accuracy, precision, recall, and F1 scores compared to Logistic Regression. This suggests that these models might be more effective for analyzing credit risk and predicting default probability.

Properly assessing and managing credit risk is crucial for financial institutions to minimize potential losses. By utilizing credit risk analysis models such as the XGBoost and LightGBM classifiers developed in this project, lenders can make more informed decisions regarding loan approvals and minimize the risk of default.

In the context of credit risk assessment, the specific metric that is considered most important may vary depending on the priorities and requirements of the financial institution. For example, if the institution aims to minimize the risk of default, recall (identifying as many at-risk borrowers as possible) may be prioritized. Alternatively, if the institution wants to minimize the number of false positives and avoid denying credit to potentially creditworthy borrowers, precision may be more important
