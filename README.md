# Retail Sales Data Analysis using SQL

This project demonstrates a foundational approach to retail sales data analysis using SQL. It involves creating a mock dataset, populating it with sample data, and then performing various analytical queries to extract meaningful business insights. The dataset simulates common retail entities such as products, customers, employees, stores, and transactions.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset Schema](#dataset-schema)
- [Key Analyses & Insights](#key-analyses--insights)

## Project Overview

The goal of this project is to simulate a retail environment and derive actionable insights from its transactional data. By creating a normalized schema (dimension and fact tables) and populating it with mock data, we can then perform various aggregations and analyses to understand sales performance, customer behavior, and product trends.

## Dataset Schema

The dataset is designed with a star schema-like structure, consisting of the following tables:

**Dimension Tables:**

* `products`: Stores details about individual products (ID, name, category, price).
* `customers`: Contains information about customers (ID, name, email, city).
* `employees`: Holds details about employees (ID, name, position, assigned store).
* `stores`: Provides information about retail store locations (ID, name, location).

**Fact Table:**

* `transactions`: Records each sales transaction, linking to the dimension tables via foreign keys. It includes `transaction_date`, `quantity`, and `total_amount`.

**View:**

* `sales`: A virtual table created to simplify complex queries by joining the `transactions` fact table with all dimension tables, making it easier to access combined information like `customer_name`, `product_name`, `store_name`, etc.

## Key Analyses & Insights

The analytical queries in this project aim to provide a comprehensive understanding of the retail operations:

* **Top Spender:** Identifies the customer with the highest total expenditure (e.g., Alice).
* **Overall Sales Volume:** Calculates the total number of items sold across all transactions.
* **Average Selling Price:** Determines the average price of products sold.
* **Employee Performance:** Ranks employees based on the total revenue they generated (e.g., Emily as the top performer).
* **Product Performance:** Identifies the top 3 and bottom 3 best-selling products by total sales.
* **Store Revenue:** Determines which store generates the most revenue (e.g., Downtown Store).
* **Category Revenue:** Calculates total revenue generated by each product category (e.g., Electronics as the highest).
* **Order Date Range:** Finds the earliest and latest transaction dates in the dataset.
* **Transaction Segmentation:** Categorizes individual transactions into 'regular', 'privilege', and 'VIP' segments based on `total_amount`, and provides a count for each segment.
