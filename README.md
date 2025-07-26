<img src="./customer-churn-bg-img.webp" alt="Customer Churn Prediction Cover Image" width="100%">

# Customer Churn Prediction
## Project Overview
This project focuses on analyzing customer churn in the telecom industry. Customer churn, the rate at which customers stop doing business with a company, is a critical metric. High churn rates can significantly impact revenue, especially given the high costs of acquiring new customers.

The primary goal of this project is to **build a predictive model that can identify customers who are likely to churn**. By leveraging insights from data analysis, telecom companies can develop targeted strategies to improve customer retention, enhance service quality, and ultimately foster greater customer loyalty.

This is a binary classification problem where we classify customers into two categories: **churn or not churn**.

## Dataset
The dataset used for this analysis is the "Teleco-Customer-Churn.csv" file, which contains various attributes related to customer demographics, services they have signed up for, and their account information.
### Dataset Attributes:
- `customerID`: Unique identifier for each customer.
- `gender`: Customer's gender (Male/Female).
- `SeniorCitizen`: Whether the customer is a senior citizen (1/0).
- `Partner`: Whether the customer has a partner (Yes/No).
- `Dependents`: Whether the customer has dependents (Yes/No).
- `tenure`: Number of months the customer has been with the company.
- `PhoneService`: Whether the customer has a phone service (Yes/No).
- `MultipleLines`: Whether the customer has multiple lines (Yes/No/No phone service).
- `InternetService`: Customer’s internet service provider (DSL/Fiber optic/No).
- `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`, `StreamingTV`, `StreamingMovies`: Additional services subscribed to by the customer.
- `Contract`: The customer's contract term (Month-to-month/One year/Two year).
- `PaperlessBilling`: Whether the customer has paperless billing (Yes/No).
- `PaymentMethod`: The customer’s payment method.
- `MonthlyCharges`: The amount charged to the customer monthly.
- `TotalCharges`: The total amount charged to the customer.
- `Churn`: The target variable, indicating whether the customer churned (Yes/No).

## Exploratory Data Analysis (EDA)
The EDA phase involved cleaning the data, handling missing values, and visualizing the relationships between different features and the churn rate.
### Key Findings:
- **Tenure and Total Charges**: Customers who churned have a significantly lower average tenure (around 18 months) and lower total charges compared to non-churning customers (average tenure of 37.5 months).
- **Contract Type**: Customers with month-to-month contracts are far more likely to churn than those with one- or two-year contracts.
- **Additional Services**: Customers who subscribe to services like Online Security, Online Backup, Device Protection, and Tech Support have a lower churn rate.
- **Demographics**: Senior citizens have a higher churn rate. Customers without partners or dependents are also more likely to churn.

## Modeling
Several machine learning models were implemented to predict customer churn. The dataset was split into training and testing sets, and the models were evaluated based on their performance metrics.
### Models Implemented:
- Random Forest Classifier
- XGBoost Classifier
### Performance:
The models were evaluated using metrics such as Accuracy, Precision, Recall, F1-Score, and ROC AUC. The XGBoost Classifier showed the best performance across most metrics, making it the most suitable model for this prediction task.

## Getting Started
To get started with this project, clone the repository and install the necessary dependencies.
### Prerequisites:
Make sure you have Python installed. You can install the required packages using pip:
``` bash
pip install -r requirements.txt
```
### Running the Notebook:
You can run the `customer_churn.ipynb` notebook using Jupyter Notebook or JupyterLab to see the complete analysis and modeling process.

## Next Steps
The next steps for this project include:
- **Hyperparameter Tuning**: Fine-tuning the models, especially the XGBoost Classifier, to further improve their performance.
- **Deployment**: Deploying the best-performing model as a web service or API for real-time churn prediction.