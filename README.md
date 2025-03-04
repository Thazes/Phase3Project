# Phase 3 data Science Project



## Project Overview 

Reducing customer churn is crucial for sustaining revenue and profitability. Identifying at-risk customers allows for proactive retention strategies, such as tailored offers and service improvements. A data-driven approach enhances customer satisfaction, strengthens loyalty, and supports long-term business growth.

### Business Understanding

In the highly competitive telecom industry, customer retention is crucial for sustained business growth. A significant challenge faced by telecom providers is customer churn, where users discontinue their services. Understanding the factors influencing churn can help companies take proactive measures to enhance customer satisfaction and reduce revenue loss.

This dataset contains various attributes related to customer usage patterns, service plans, and interactions with customer support. By analyzing this data, we aim to build a predictive model that can identify customers at high risk of churning.

#### Business Objectives
 1. Predict churn probability: Develop a model to classify customers as likely to churn or likely to stay based on their usage behavior.

 2. Identify key churn indicators: Determine which factors (e.g., high call charges, frequent customer service calls, etc.) contribute the most to churn.



### Data Understanding

The data set had 3,333 rows and 21 columns with different data types

![alt text](https://github.com/Thazes/Phase3Project/blob/main/photos/datatypes.png)


### Data Cleaning

Upon further analysis the dataset didn't have any null or duplicated values therefore minimal cleaning of data was needed.

Next I looked at the Outliers. The Box plot below shows how they were distributed:

![alt text](https://github.com/Thazes/Phase3Project/blob/main/photos/box%20plot%20showing%20outliers.png)

I dropped all rows with outliers

### EDA and data analysis
I plotted a histogram showing how the numerical values are distributed

![alt text](https://github.com/Thazes/Phase3Project/blob/main/photos/Histogram%20Numerical%20Columns.png)

From the above Histograms The following columns seem to be having a unifirm distribution:

accountlength,total day minutes,total day calls,total day charge,total eve minutes,total eve calls,total eve charge,total night minutes,total night calls,total night charge,total intl minutes,total intl charge

Next I plotted a correlation matrix of numeric the variables 
![alt text](https://github.com/Thazes/Phase3Project/blob/main/photos/correlationmatricnumeric.png)

Total day minutes and total day charge have a perfect correlation (1.00), indicating a direct linear relationship (likely because total day charge is derived from total day minutes). Similarly, total eve minutes and total eve charge, total night minutes and total night charge, total intl minutes and total intl charge also show a perfect correlation (1.00).

Since total day charge is derived from total day minutes,total eve minutes and total eve charge and finally total night minutes and total night charge one of them from the pairs should be dropped to avoid multicollinearity in modeling.





