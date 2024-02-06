# Databel Churn Analysis Project

## Introduction

Welcome to the realm of Databel, a dynamic telecommunications enterprise renowned for its comprehensive array of call and data services. Our mission? To unlock the enigmatic facets concealed within our churn rate data and gain insights into the pivotal factors influencing customer retention. Examining churn extends beyond merely quantifying its rate; it entails deciphering the reasons behind customer departures and devising effective strategies to mitigate churn. Embark with me on this data-driven expedition as we navigate through the core of our operations, striving to enhance customer allegiance and diminish churn. The analytical tools employed for this exploration are Microsoft PowerBI and Python.

## Problem Statement
With a half-decade presence in the market, Databel has undergone remarkable growth. Nevertheless, mounting competition and evolving consumer preferences have cast a spotlight on our churn rate -the proportion of subscribers discontinuing their memberships monthly or yearly. I have endeavored to identify the root causes of churn and formulate strategies to preserve our most valuable clientele.
They are interested in understanding the prediction of customers that will churn with the dataset provided. A thorough EDA has been done with Microsoft Power BI to investigate the reason for customer churning behavior. However, they are still interested in profiling a potential customer that can churn to reduce the possibility of having churning customers, which was done using Python. 

## Dataset Description
The dataset comprises 29 columns and 6,687 rows. The following are the columns in the data:
- Customer ID
- Churn Label
- Account Length (in months)
- Local Calls
- Local Mins
- Intl Calls
- Intl Mins
- Intl Active
- Intl Plan
- Extra International Charges
- Customer Service Calls
- Avg Monthly GB Download
- Unlimited Data Plan
- Extra Data Charges
- State
- Phone Number
- Gender
- Age
- Under 30
- Senior
- Group
- Number of Customers in Group
- Device Protection & Online Backup
- Contract Type
- Payment Method
- Monthly Charge
- Total Charges
- Churn Category
- Churn Reason
 
## Exploratory Data Analysis with Power BI
After the EDA process, the dashboard attached below was created.

![Databel Churn Analysis IMG](https://github.com/Temitope-Omotosho/databel-analysis/assets/63404084/faf52780-74f0-4095-8c83-bd53be17857b)

## Insights

Major insights from the analysis are:
- The churn rate for the company was `26.86%`
- Competitor was the major category that led to about `44.82%` of the customers churning, while Attitude and Dissatisfaction were the next top categories for churning.
- Competitor made better offer, competitor had better devices, and Attitude of support person were the top three reasons for customers churning.
- Customers on month-to-month contracts have higher churn rate of `46.29%` than those on yearly contracts with a churn rate of `6.62%`.
- Customers in Califonia had the highest churn rate of over `63%`
- For payment methods, customers using the direct debit method were more and churned more often with a churn rate of `53.9%` however, judging using the churn rate alone seemed like paper check had a higher churn rate. The reverse is the case because most times, percentage with the totals are not necessarily representative.
- Older customers (>= 70years) have higher churn rate. It was observed that `289/357` old customers on monthly contract were on direct debit payment method, and over `82%` of them churned.
- Churn rate decreases with increasing account length.
- Churn rate increases with increasing customer age.
- Customers on unlimited data plan have higher churn rate with respect to their data usage - users with low data usage churned more often when compared to the others.
- Customers in a group had lower churn rate unlike those not subscribed in groups.
- The impact of gender was not so significant and we can conclude that gender did not play a major role in the reason why people churn.
- Lastly, customers with more customers service calls have a very high tendency of churning.

## Recommendations
- Do a market research and investigate on what their competitors are doing better to improve their services because based on the customers behavior, Databel are not competitive enough.

- Roll out promotions with juicy yearly offers in order to have more customers that are on yearly contracts who have lower churn rate.

- Investigate the direct debit payment method for older customers on monthly contracts, because it is the only distinct reason for them churning while others are generic.

- Advise customers on unlimited plan with low and medium data usage to downgrade their plan so as to use a plan that suits their data needs, this shows how much Databel cares about their customers and not just their profit.
  
- Conduct an investigation in Califonia to understand why they have a very high churn rate.
  
- Lastly, the attitude of support person was a mojor reason for customers churning, this can be easily mitigated by ensuring the customer service department adhere to all the customer relations policies to prevent customers dissatisfaction.

## Churn Prediction
Churn Prediction was done using Python.
After data cleaning and preprocessing, various models were tested using kFold cross validation, and the Gradient Boosting Classifier performed best. Hyperparameter tuning did not yield a good result as the baseline model was better. However, after several feature engineering was done the model accuracy was over 98%. The scoring metric used was the recall metric because reducing the number of false negatives is of more importance to Databel. In simple terms, this means that they are interested in knowing a customer that will churn and not otherwise.

After an accurate model was developed, custom functions were created to carry out all the important tasks carried out in the project. The model was saved using the joblib library, and it was used to make a single point prediction which can be used later for a deployed web app helping datebel to know a customer that will churn from a beautiful GUI.

The step by step workflow can be found in the Databel Churn Prediction Jupyter notebook file in the churn prediction folder.

## Conclusion
This project aim to help Databel understand the reason for their customers churning and also help them predict the potential of a customer churning or not. This was achieved with the numerous insights gotten from the dataset, and also building a model of 98% accuracy. The recommendations given will help databel improve their services to their customers and also reduce the churning rate of their customers significantly.
