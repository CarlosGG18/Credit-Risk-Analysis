# Credit Risk Analysis
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
There is a strong correlation between `person_age` and `cb_person_cred_hist_lengt`h. As borrowers get older, their credit history length tends to increase as well.

The `loan_int_rate` shows a significant correlation with `loan_grade`. As the loan grade gets closer to (F), the interest rate also tends to increase.

`cb_person_default_on_file` is correlated with both `loan_grade` and `loan_int_rate`.

The target variable, `loan_status`, is correlated with `person_home_ownership`,` loan_int_rate`, `and loan_grade`.

## Model Results
Three models were trained and evaluated: Logistic Regression,Linear Regression, Random Forest, Support Vector Machine, Light GBM, Ridge Classifier, and XGBoost Classifier. Here are the performance metrics for each model:

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
| - Train Set             | N/A            | N/A            | N/A         | N/A     |
| - Test Set              | N/A            | N/A            | N/A         | N/A     | 


**LightGBM Classifier:**
In addition to the previous models, a LightGBM classifier was trained and evaluated. Light Gradient Boosting uses a leaf-wise tree growth strategy, which can lead to faster convergence and potentially better accuracy compared to other gradient boosting algorithms. Noteworthy features of LightGBM include its ability to handle categorical variables without one-hot encoding, customizable loss functions, and quickness.

## Conclusion
Properly assessing and managing credit risk is crucial for financial institutions to minimize potential losses. By utilizing credit risk analysis models such as the XGBoost and LightGBM classifiers developed in this project, lenders can make more informed decisions regarding loan approvals and minimize the risk of default.

For detailed code implementation and further analysis, please refer to the Jupyter Notebook folder.
