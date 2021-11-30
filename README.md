# Sales-insights
# problem Statemen:
AtliQ hardware is a company in India which supplies computer hardware and peripheral devices across India only. The have many stores across India such as surge stores, Nomad stores etc. The head office of the company is situated in Delhi.
# Scenario —
The sales manager of the company is facing many challenges. He is facing issues in tracking sales in dynamically growing market. He is having issues with the insights of his business.
In order to this he has some of the regional managers in North, south and central India working for the company. So, he calls them and ask about the insights he wants to know. They tell him about the sales in last quarter and the growth in that quarter.
So, the problem is that the conversations that are happening are verbal. Hence, the regional managers are sugar coating the facts and the manager of the company does not get the clear picture of the facts. Even after knowing that the sales are declining, he cannot do anything because he does not have the clear picture of the sales. Asking for the records the regional manager provides him with excel files. But by this he cannot figure out small things.
All what the manager wants is a view of the weakest area the company need to focus to increase the sales and improvise the declination. He is interested in simple, understandable and digestive insight. So, he is more interested in a dashboard which he can go and look at the real data because data speaks the truth. All he wants is a simple data visualization tool which he can access on daily basis.
Hence, by using such tools and technology one can make data driven decisions which helps to increase the sales of the company.
So, in this project we will help a company make its own sales related dashboard using PowerBI.

# AIMS Grid
![](https://github.com/yashwanth-gurram/Sales-insights/blob/main/Screenshot%20(393).png)


# Data Analysis Using SQL

Show all customer records

SELECT * FROM customers;

Show total number of customers

SELECT count(*) FROM customers;

Show transactions for Chennai market (market code for chennai is Mark001

SELECT * FROM transactions where market_code='Mark001';

Show distrinct product codes that were sold in chennai

SELECT distinct product_code FROM transactions where market_code='Mark001';

Show transactions where currency is US dollars

SELECT * from transactions where currency="USD"

Show transactions in 2020 join by date table

SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

Show total revenue in year 2020,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";

Show total revenue in year 2020, January Month,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");

Show total revenue in year 2020 in Chennai

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";
