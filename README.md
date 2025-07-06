# Customer Churn Analysis Project (SQL + Excel)

This project is a complete Customer Churn Analysis case study using SQL for data analysis and Excel for visual storytelling. It aims to solve a real business problem:  
Why are customers leaving, and what can we do about it?



## Project Objective

- Identify churn patterns using real-world customer data
- Discover why customers are leaving
- Present clear, data-driven recommendations to reduce churn
- Build charts that are easy to understand for business stakeholders

## Tools Used

| Tool               | Purpose                                |
|--------------------|----------------------------------------|
| SQL (MySQL Workbench) | Data cleaning, filtering, and analysis |
| Excel              | Chart building and visual dashboards   |
| GitHub             | Version control and project showcase   |

## Dataset Overview

Each row = 1 customer  
Each column = customer details

| Column Name       | Description                                |
|-------------------|--------------------------------------------|
| `customerID`      | Unique customer ID                         |
| `gender`          | Male / Female                              |
| `SeniorCitizen`   | 1 = Yes, 0 = No                             |
| `Partner`         | Has a partner (Yes/No)                     |
| `Dependents`      | Has dependents (Yes/No)                    |
| `tenure`          | Number of months the customer has stayed   |
| `PhoneService`    | Has phone service (Yes/No)                 |
| `MultipleLines`   | Has multiple phone lines                   |
| `InternetService` | DSL / Fiber Optic / None                   |
| `OnlineSecurity`, `TechSupport`, etc. | Service usage flags    |
| `Contract`        | Month-to-month / One year / Two year       |
| `PaperlessBilling`| Is billing paperless?                      |
| `PaymentMethod`   | Type of payment method used                |
| `MonthlyCharges`  | Amount paid per month                      |
| `TotalCharges`    | Total charges since joining                |
| `Churn`           | Yes = Left the company / No = Still active |



## Key Questions Answered Using SQL

### 1. How many customers churned overall?

- Query: Count customers where `Churn = 'Yes'`
- Insight: Helps us understand how big the churn problem is

| Churn | Total_Customers |
|-------|------------------|
| No    | 5174             |
| Yes   | 1869             |


### 2. Which contract types have the highest churn?

- Grouped customers by contract (Monthly / 1 Year / 2 Year)
- Calculated churn percentage in each group
- Insight: Month-to-month plans have highest churn — these customers are less committed
  
| Contract        | Total_Customers | Churned_Customers | Churn_Rate (%) |
|----------------|------------------|-------------------|----------------|
| Month-to-month | 3875             | 1655              | 42.71%         |
| One year       | 1473             | 166               | 11.27%         |
| Two year       | 1695             | 48                | 2.83%          |


### 3. Does payment method affect churn?

- Grouped by payment type (e.g., Electronic Check, Credit Card)
- Compared churn rates
- Insight: Customers using electronic checks tend to leave more

| Payment Method              | Total_Customers | Churned_Customers | Churn_Rate (%) |
|----------------------------|------------------|-------------------|----------------|
| Electronic check           | 2365             | 1071              | 45.29%         |
| Mailed check               | 1612             | 308               | 19.11%         |
| Bank transfer (automatic)  | 1544             | 258               | 16.71%         |
| Credit card (automatic)    | 1522             | 232               | 15.24%         |


### 4. Does customer tenure affect churn?

- Segmented users based on how long they stayed
- Found that newer customers churn more
- Insight: First few months are critical — onboarding should be improved

| Tenure Group   | Total_Customers | Churned_Customers | Churn_Rate (%) |
|----------------|------------------|-------------------|----------------|
| 0–12 Months    | 2186             | 1037              | 47.44%         |
| 13–24 Months   | 1024             | 294               | 28.71%         |
| 25–48 Months   | 1594             | 325               | 20.39%         |
| 49+ Months     | 2239             | 213               | 9.51%          |




## Excel Charts

SQL results were converted to `.csv` files and visualized in Excel for clarity:

| Chart Name              | What It Shows                         |
|-------------------------|----------------------------------------|
| `contract_churn.csv`    | Churn percentage by contract type      |
| `payment_churn.csv`     | Churn percentage by payment method     |
| `tenure_churn.csv`      | Churn percentage by customer tenure    |

Each chart helps business teams visually identify problems and take action.


## Business Insights

| Finding                          | Business Suggestion                            |
|----------------------------------|-------------------------------------------------|
| High churn in month-to-month plans | Offer discounts for 1-year contracts           |
| High churn in first 6 months       | Improve onboarding experience                  |
| High churn with electronic checks | Promote card/auto-debit options                |
| Low churn in long-tenure users    | Reward loyal customers with retention offers   |



## Project Files

| File Name                        | Description                            |
|----------------------------------|----------------------------------------|
| `churn_analysis_queries.sql`    | SQL queries used for analysis          |
| `contract_churn.csv`            | Contract type vs churn data            |
| `payment_churn.csv`             | Payment method vs churn data           |
| `tenure_churn.csv`              | Tenure group vs churn data             |
| `Customer_Churn_Dashboard.xlsx` | Excel dashboard with visuals           |
| `README.md`                     | Project explanation file               |


## What This Project Proves

- Ability to use SQL to solve real business problems  
- Skill in presenting data insights clearly in Excel  
- Understanding of how data supports business decisions  
- Capable of working independently from raw data to final output  
- Strong communication and storytelling with data


## Resources I Used to Build This Project

These learning resources helped me build and understand this project:

- [IBM Telco Customer Churn Dataset (Kaggle)](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)  
- [W3Schools SQL Tutorial](https://www.w3schools.com/sql/)  
- [Learn SQL by Sumit Mittal (Hindi)](https://www.youtube.com/watch?v=zAOUpVM6R6I&list=PLtgiThe4j67rAoPmnCQmcgLS4iIc5ungg)  
  



