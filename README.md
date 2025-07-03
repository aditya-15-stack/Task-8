
# 🛒 Sales Data Analysis – SQL & Power BI Project

## 📋 Project Overview

This project focuses on analyzing **sales performance across different markets** using **SQL for data extraction** and **Power BI for interactive dashboards and visual insights**. It uncovers key trends, market-wise performance, and customer behaviors.

---

## 📂 Repository Contents
- `db_dump.sql` — SQL database dump file
- `Readme.txt` — SQL queries used for analysis
- `sales_dashboard.pdf` — Export of Power BI dashboard visuals

---

## 🛠️ Tools & Technologies
- **SQL**: Data querying and preparation
- **Power BI**: Visual analytics and dashboard creation
- **DAX**: Quick measures, KPIs, and custom metrics in Power BI

---

## 🔍 SQL Queries Used

| Purpose | SQL Query |
|---------|-----------|
| Show all customer records | `SELECT * FROM customers;` |
| Show total number of customers | `SELECT count(*) FROM customers;` |
| Show transactions for Chennai market | `SELECT * FROM transactions WHERE market_code='Mark001';` |
| Show distinct product codes sold in Chennai | `SELECT DISTINCT product_code FROM transactions WHERE market_code='Mark001';` |
| Show transactions in USD currency | `SELECT * FROM transactions WHERE currency='USD';` |
| Show transactions in 2020 | `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date WHERE date.year=2020;` |
| Show total revenue in 2020 | `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date WHERE date.year=2020 AND (transactions.currency='INR\r' OR transactions.currency='USD\r');` |
| Show total revenue in January 2020 | `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date WHERE date.year=2020 AND date.month_name='January' AND (transactions.currency='INR\r' OR transactions.currency='USD\r');` |
| Show total revenue in Chennai in 2020 | `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date WHERE date.year=2020 AND transactions.market_code='Mark001';` |

---

## 📊 Power BI Insights
- **Revenue by Market:** Delhi NCR leads with ₹221M
- **Sales Quantity by Region:** Highest in Delhi NCR and Mumbai
- **Top 5 Products & Customers:** Electricalsara Store contributes ~65% of sales
- **Monthly Revenue Trends:** Revenue peaks between May and July 2018

---

## 🚀 Outcome
This project demonstrates:
- Strong SQL querying skills for business analysis
- Efficient dataset manipulation and data joining
- Power BI dashboard design for real-time, dynamic insights
