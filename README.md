🛒 Olist E-Commerce Data Analysis

This project is an exploratory analysis of the [Olist E-Commerce Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce), which contains over 100,000 real orders made by customers across Brazil.

The goal was to understand customer behavior, sales distribution, delivery performance, and seller activity using real marketplace data.



🧭 Project Overview

Olist is a Brazilian e-commerce platform that connects small businesses to major online marketplaces.
I wanted to explore this dataset to answer a few key questions:

-Which states generate the most sales?
-How well does Olist perform in terms of on-time delivery?
-Who are the top-performing sellers?
-Does the sales distribution follow the 80/20 rule?


🧹 Data Cleaning & Preparation

I worked with multiple CSV files from Kaggle, including orders, order items, customers, products, and sellers.
Here’s what I did during the data prep phase:

-Merged all relevant tables into a single dataset using common keys (`order_id`, `customer_id`, etc.)
-Removed missing or inconsistent values
-Converted timestamps to datetime objects
-Calculated delivery delays and created an on-time/delayed delivery indicator

The final cleaned dataset was then exported for analysis.


📊 Main Insights

Here are a few highlights from the analysis:

-Top States: Most orders come from São Paulo (SP), followed by Rio de Janeiro (RJ) and Minas Gerais (MG).
-Delivery Performance: Around 93% of orders were delivered on time — a strong operational metric.
-Seller Revenue: A small group of sellers generate a large portion of total sales, showing a clear revenue concentration.
-Pareto Effect: The 80/20 rule applies — a minority of sellers drive the majority of revenue.


📈 Visualizations

Some of the charts created during this analysis include:

-Total sales by customer state
-On-time vs delayed deliveries
-Top 10 sellers by total revenue
-Monthly sales trends

All visuals were made using **Matplotlib** and **Seaborn**.


⚙️ Tools & Libraries

-Python
-Pandas & NumPy for data cleaning and manipulation
-Matplotlib & Seaborn for data visualization
-Google Colab as the main development environment


📂 Repository Structure
File                                Description
E-Commerce Analysis.ipynb           Colab notebook with full analysis
cleaned_olist_sales_data.csv        Exported cleaned dataset used for analysis
README.md                           Project overview and documentation


🧠 Reflections

This project was a great opportunity to practice real-world data wrangling and exploratory analysis.
The Olist dataset is messy and diverse, which made it perfect for learning how to handle joins, timestamps, and feature creation.

If I extend this project, I’d like to:

-Explore customer lifetime value (CLV)
-Analyze product categories and pricing patterns
-Build simple predictive models for delivery delays


👤 About Me

VIDHYA DHARI YELURI
📧 vidhyay458@gmail.com
🔗 in/vidhya-yeluri-88432a254


💬 Final Note
This was a fun and insightful project — it helped me strengthen my data analysis workflow and understand how real e-commerce businesses operate behind the scenes.
