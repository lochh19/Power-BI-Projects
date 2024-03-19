# Power-BI-Project 
## Sales Insights Analysis
As part of the Global Soft Systems Workshop, designed a Power BI dashboard using SQL to understand the sales trend by Assuming Global Soft Systems Inc. Company is a Consumer goods company. The final dashboard is effective at displaying the sales trend in Global Soft Systems, allowing users to understand the data and make informed decisions. 
This dashboard could help in increasing the revenue atleast by 7% in the next quarter.

Live Dashboard https://www.novypro.com/project/sales-insights-46

## Problem statement
In an ever-evolving computer hardware market, Assuming Global Soft Systems Inc. Company is a Consumer goods company which is facing issues in terms of tracking Sales in this dynamically growing market. To address this, the Sales Director has initiated a data analysis project aimed at developing a real-time sales insights dashboard using Power BI. The dashboard will integrate crucial data from sales_market, sales_transaction, sales_date, sales_customers, and sales_products. By leveraging this comprehensive dataset, our goal is to empower decision-makers with actionable insights into market trends, customer behavior, and product performance. Through this workshop, we will explore methodologies to extract meaningful patterns, identify opportunities, and optimize sales strategies. Ultimately, this initiative seeks to enhance our competitive edge by enabling proactive decision-making based on timely and accurate information.

## Tasks to perform on MySQL Workbench

1. Show all customer records

    `SELECT * FROM customers;`

2. Show total number of customers

    `SELECT count(*) FROM customers;`

3. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

4. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

5. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

6. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

7. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
8. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

9. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`


## Data Model 

![sales Insights DataModel](https://github.com/lochh19/Power-BI-Projects/assets/163352505/99cc9d4a-9522-4324-b550-62c7084eb1f4)


## Dashboard 

![Sales Insights](https://github.com/lochh19/Power-BI-Projects/assets/163352505/abacd6a2-157e-4a24-a763-ecc663fa1342)




