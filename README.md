# SQL Project: **Olist E-Commerce Analysis**

## Project Overview

This SQL project analyzes the **Olist e-commerce dataset**, which contains information about customers, orders, products, payments, reviews, and sellers. The goal of the project is to explore, analyze, and generate insights based on the data from different tables. The project covers a range of SQL concepts including **JOINs**, **GROUP BY**, **subqueries**, **window functions**, and **aggregations**.
The project is divided into three levels of difficulty, starting with easy queries that retrieve basic information such as customer details, product prices, and order amounts. The medium-level queries focus on aggregating data to uncover insights like total revenue by product category, top-selling products, and average order values by customer. Finally, the hard-level queries involve advanced SQL techniques, including recursive queries, window functions, and complex aggregations to analyze sales performance by seller, identify the most frequent products ordered, and calculate the average number of products per order.

The goal of the project is to leverage SQL skills to perform real-world business analysis, uncover valuable insights, and generate reports based on the data. It helps develop expertise in JOINs, GROUP BY, subqueries, and window functions, essential for handling complex data in relational databases. This project provides a comprehensive learning experience for SQL practitioners aiming to deepen their knowledge of data analysis and reporting.

## Database Schema <a name="schema"></a>

<img width="1920" height="1080" alt="olister" src="https://github.com/user-attachments/assets/d0c606f3-1e89-4e24-9973-5e9955724ae0" />

The following tables are part of the Olist dataset:
https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

* **olist\_customers\_dataset**: Contains customer details.
* **olist\_orders\_dataset**: Contains order details including order amount and customer information.
* **olist\_order\_items\_dataset**: Contains the products purchased in each order.
* **olist\_products\_dataset**: Contains product details like name, price, and category.
* **olist\_order\_payments\_dataset**: Contains payment information for each order.
* **olist\_order\_reviews\_dataset**: Contains reviews left by customers for their orders.
* **olist\_sellers\_dataset**: Contains seller information for products.
* **product\_category\_name\_translation**: Translates product category names into different languages.

---

## SQL Queries <a name="queries"></a>

The project contains the following SQL queries and problems:

### Easy-Level Problems:

1. Retrieve all customers from the `olist_customers_dataset` table.
2. List product names and prices from the `olist_products_dataset`.
3. Find orders with a total amount greater than 500 in the `olist_orders_dataset`.
4. List products in the "Electronics" category from the `olist_products_dataset`.
5. Count the number of orders per customer.

### Medium-Level Problems:

1. .Calculate the total revenue by product category.
2. List the top 5 products based on quantity sold.
3. Identify customers who have never placed an order.
4. Calculate the average order value for each customer.
5. Identify product categories with no orders.
6. Calculate the total payments made by each payment method.
7. Count the number of orders placed by each customer in 2021.
8. List orders that have no payment information.
9. Calculate the average product rating for each seller’s products.
10. List products that were ordered more than 5 times.

### Hard-Level Problems:

1. Rank the top 3 highest paying customers.
2. Compare products with the highest and lowest average ratings.
3. Calculate the average number of products per order.
4. Create a recursive query to build the order hierarchy.
5. Identify the most common product ordered.
6. Calculate the average sales per month for each seller.
7. Calculate the average product rating for each seller’s products across all orders.
8. List customers who have ordered more than one product in any order.
9. Calculate the sales per month for each seller.
10. Identify sellers with zero sales.

---

## Objective of Queries <a name="objectives"></a>

The objectives of the queries are to:

* Analyze **customer spending** patterns and identify the most profitable customers.
* Investigate **product performance**, including which products are most popular and have the highest ratings.
* Perform detailed **order analysis**, such as average order value, the number of products per order, and sales per seller.
* Identify key **business insights**, such as product categories with no sales, the most frequent payment methods, and customers who don’t leave reviews.

