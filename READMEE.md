# 🛒 Grocery Store Management: SQL Project

A complete MySQL project that builds a grocery store database from scratch and answers real business questions with SQL: customer behaviour, product performance, sales trends, supplier contribution and employee performance.

## 📌 Project Overview

The script `Grocery_Store_Management_2026.sql` does everything in one run:

1. **Creates the database** (`grocery_store`)
2. **Builds 7 related tables** with primary and foreign keys
3. **Loads sample data** (about 1,170 rows)
4. **Runs 25 analysis queries** plus 5 bonus advanced queries

## 🗂️ Database Schema

| Table | Description | Rows |
|---|---|---|
| `supplier` | Supplier names and addresses | 5 |
| `categories` | Product categories (e.g. Grains & Cereals, Dairy Products) | 5 |
| `employees` | Staff who process orders | 10 |
| `customers` | Customer names and addresses | 200 |
| `products` | Products with price, supplier and category | 50 |
| `orders` | Order header: customer, employee, date | 300 |
| `order_details` | Line items: product, quantity, price | 600 |

**Relationships**

```
supplier ──┐
           ├──< products >──┐
categories ┘                │
                            ├──< order_details >── orders >──┬── customers
                            │                                └── employees
```

## 🔍 Analysis Covered

| Part | Topic | Questions |
|---|---|---|
| A | Customer Insights | Unique customers, top customers by orders and spend, average purchase value |
| B | Product Performance | Products per category, average price, top sellers, revenue per product |
| C | Sales & Order Trends | Total/average orders, busiest dates, monthly trends, weekday vs weekend |
| D | Supplier Contribution | Supplier counts, products per supplier, revenue by supplier |
| E | Employee Performance | Orders handled, sales value and average order value per employee |
| F | Order Details Deep Dive | Quantity vs price, average quantity, unit price variation |
| Bonus | Advanced Queries | Revenue summary, category revenue share (%), customers with no orders, best seller per category, year-over-year revenue |

## 🧠 SQL Concepts Used

- `JOIN`s across multiple tables
- Aggregate functions: `SUM`, `AVG`, `COUNT`, `MAX`
- `GROUP BY`, `HAVING`, `ORDER BY`, `LIMIT`
- Subqueries and window functions (`RANK() OVER (PARTITION BY ...)`)
- Date functions (`STR_TO_DATE`, `YEAR`, `MONTH`, `DAYOFWEEK`)
- Foreign keys with `ON UPDATE CASCADE` / `ON DELETE CASCADE`

## 🚀 How to Run

**Requirements:** MySQL 8.0 or later (window functions need 8.0+) and MySQL Workbench, or any MySQL client.

1. Clone this repository:
   ```bash
   git clone https://github.com/Varaddahale/Grocery-Store-Management-SQL.git
   ```
2. Open `Grocery_Store_Management_2026.sql` in MySQL Workbench.
3. Run the whole script with `Ctrl + Shift + Enter` (`Cmd + Shift + Return` on Mac).
4. The script creates the `grocery_store` database, tables and data, then runs the queries.

> ⚠️ The script runs `DROP TABLE IF EXISTS` on its own tables, so re-running it resets the data. Don't run it on a database that holds anything you want to keep.

## 📸 Sample Output

_Add screenshots of a few query results here, for example "Best selling product per category" and "Monthly trends"._

```
![Best selling product per category](images/bonus4.png)
```

## 🛠️ Tools

- MySQL 8.x
- MySQL Workbench

## 👤 Author

**Your Name**
GitHub: [@Varaddahale](https://github.com/Varaddahale)
