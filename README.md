# Sales-Report
This project involves the analysis of sales data for a hardware company, with the goal of deriving valuable insights to guide decision-making. The analysis focuses on understanding sales trends, identifying top-performing products, and highlighting key factors influencing sales performance. 
## Tools used in this project are "SQL" and "Power Bi


### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`
USED THE SQL TO CHECK THE RESULT OF THE VISUALIZATION IS CORRECT


Data Analysis Using Power BI
============================
1) Cleaned the data using the power query editor and changed the currency in the currency column amount to "inr" and used it for the visualization.
2) then loaded the dataset into power bi engine and created the relationship between the table.
3) Then created the charts and started to design the report in the interactive way. 

