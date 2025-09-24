###Olist E-Commerce Analysis: SQL & Power BI Insights

This project analyzes the Olist Brazilian E-Commerce dataset (2016–2018) using SQL to uncover customer behavior, sales trends, and product performance insights, visualized with Power BI dashboards. Key findings include São Paulo driving 40% of sales and high-photo products boosting reviews by 15%. Results are presented as screenshots to protect originality.
View the full presentation: Olist_E-Commerce_Analysis.pptx (PDF format, watermarked).
🎯 Project Overview
This SQL-driven project explores the Olist dataset, focusing on:

Customer Behavior: Urban vs. rural purchasing patterns.
Sales Trends: Regional and seasonal revenue patterns (total ~R$16M).
Product Performance: Category and seller analysis via reviews and sales.
Visualizations: Power BI dashboards for interactive insights.

Key Insights:

São Paulo and Rio account for 70% of orders; rural areas offer growth potential (10% orders).
Products with >3 photos have 15% higher reviews and sales.

Tools: SQL (MySQL/PostgreSQL), Power BI.

🚀 Getting Started

Prerequisites
SQL engine (e.g., MySQL, PostgreSQL).
Power BI Desktop (optional, for dashboard replication).
Olist dataset CSVs from Kaggle.

Setup
Clone the repository:git clone https://github.com/Vandana177/Olist-E-Commerce-Analysis.git
cd Olist-E-Commerce-Analysis


Create the database (from olist.sql):CREATE DATABASE olist_project;
USE olist_project;


Import CSVs into tables using MySQL Workbench, pgAdmin, or LOAD DATA INFILE.
Run queries from queries.sql in your SQL client.
View Power BI dashboards (screenshots in PPT or .pbix file in releases).

Note: Query results are shown as images in the presentation to prevent direct copying.
📊 Dataset Schema
The dataset includes 8 tables with ~100K orders:



Table
Key Columns
Description



olist_customers_dataset
customer_id, customer_unique_id, customer_state
Customer demographics

olist_orders_dataset
order_id, order_status, order_purchase_timestamp
Order lifecycle

olist_order_items_dataset
order_id, product_id, price, quantity
Item details

olist_products_dataset
product_id, product_category_name, product_photos_qty
Product attributes

olist_order_reviews_dataset
order_id, review_score
Customer feedback

olist_sellers_dataset
seller_id, seller_state
Seller locations

olist_order_payments_dataset
order_id, payment_type, payment_value
Payment details

product_category_name_translation
product_category_name, product_category_name_english
Category translations

 
🔍 SQL Analysis
The project includes 10 SQL queries (easy and medium levels) to extract insights. Results are shown as screenshots in the presentation to protect originality.
Easy Level Queries

Retrieve All Customers  
SELECT * FROM olist_customers_dataset;

Insight: 99,441 unique customers; 70% from São Paulo/Rio. 

Count Orders by Status  
SELECT order_status, COUNT(*) AS order_count
FROM olist_orders_dataset
GROUP BY order_status;

Insight: 95% orders delivered, 2% canceled. 

Distinct Product Categories  
SELECT DISTINCT product_category_name
FROM olist_products_dataset;

Insight: 71 categories; home goods lead. 

Payment Types Usage  
SELECT payment_type, COUNT(*) AS usage_count
FROM olist_order_payments_dataset
GROUP BY payment_type;

Insight: Credit card dominates (70%). 

10 Most Recent Orders  
SELECT order_id, order_purchase_timestamp
FROM olist_orders_dataset
ORDER BY order_purchase_timestamp DESC
LIMIT 10;

Insight: Q4 2018 peaks show seasonal trends. 


Medium Level Queries

Sellers per State  
SELECT seller_state, COUNT(*) AS seller_count
FROM olist_sellers_dataset
GROUP BY seller_state;

Insight: São Paulo hosts 50% of sellers. 

Average Review Score  
SELECT AVG(review_score) AS avg_score
FROM olist_order_reviews_dataset;

Insight: 4.1/5 average; low scores need attention. 

Items in Specific Order  
SELECT oi.*
FROM olist_order_items_dataset oi
WHERE oi.order_id = '00010242fe8c5a6d1ba2dd792cb16214';

Insight: Single-item orders suggest upselling focus. 

Top 5 Cities by Customers  
SELECT customer_city, COUNT(*) AS customer_count
FROM olist_customers_dataset
GROUP BY customer_city
ORDER BY customer_count DESC
LIMIT 5;

Insight: São Paulo/Rio drive 70% of customers. 

Average Product Weight by Category  
SELECT p.product_category_name, AVG(p.product_weight_g) AS avg_weight
FROM olist_products_dataset p
GROUP BY p.product_category_name;

Insight: Heavy categories (e.g., furniture) increase shipping costs. 


📈 Power BI Dashboard
The presentation includes Power BI dashboard screenshots for interactive insights:

Customer Map: Shows São Paulo’s dominance (40% sales).
Sales Trend Line: Highlights Q4 peaks (~R$6.4M).
Top Categories Bar: Ranks bed_bath_table, health_beauty.
Review Heatmap: Correlates high reviews with sales.

Insights: Filters enable dynamic analysis; high-photo products boost engagement by 15%. 
💡 Key Findings

Customer Behavior: Urban areas (70% orders); rural growth potential (10% orders, 8% revenue).
Sales Trends: R$16M total; Q4 peaks for promotions.
Product Performance: >3 photos increase reviews/sales by 15%.
Recommendations: Optimize delivery (12-day avg.), prioritize top categories, launch loyalty programs.

🛠️ Challenges & Future Work

Challenges: Handling missing timestamps, scaling queries.
Future Work: Add Python ETL, ML for churn prediction, real-time API integration.

🤝 Contributing

Fork the repo.
Create a branch (git checkout -b feature/new-analysis).
Commit changes (git commit -m 'Add new query').
Push and open a PR.

See CONTRIBUTING.md for details.
📄 License
MIT License. See LICENSE.
🙏 Acknowledgments

Olist and Kaggle for the dataset.
SQL and Power BI communities for inspiration.

Star this repo if it helped! 🚀Contact: Vandana Bharti | vandana.1771.bharti@gmail.com | LinkedInPresentation: Olist_E-Commerce_Analysis.pptx
Built with SQL, Power BI



