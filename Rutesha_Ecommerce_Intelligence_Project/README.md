# End-to-End E-commerce Intelligence System
## Building a Customer 360 Analytics Framework

---

## Project Overview

This project simulates a real-world data analytics scenario using a
multi-table Brazilian e-commerce dataset. The goal is to integrate
multiple data sources, build a unified Customer 360 view, perform
exploratory data analysis, and generate actionable business
recommendations.

---

## Business Problem

In modern e-commerce ecosystems, data is generated across multiple
independent systems such as customer management, order processing,
payments, product catalogs, seller networks, and customer feedback
platforms. These datasets are fragmented and stored in separate tables,
making it difficult to extract unified insights.

This project addresses that problem by:

- Integrating multiple data sources into one master dataset
- Constructing a Customer 360 View
- Analyzing customer behavior, revenue patterns, and operational performance
- Identifying key drivers of business growth and customer satisfaction
- Generating actionable, data-driven business recommendations

---

## Dataset

The project uses 8 relational CSV files from a e-commerce platform.
Tables:
1.	customers.csv
Contains customer demographic and location information 
2.	orders.csv
Central table containing order lifecycle details (purchase, delivery, timestamps) 
3.	order_items.csv
Contains product-level details for each order 
4.	payments.csv
Payment information including type and value 
5.	reviews.csv
Customer feedback and review scores
6.	products.csv
Product details and categories 
7.	sellers.csv
Seller-level information 
8.	geolocation.csv
Geographic information (optional for advanced analysis) 
9.	category_translation.csv
Mapping of product categories to English names 

The orders table acts as the central fact table connecting all other datasets.

---

## Steps Followed

### Step 1: Data Loading and Exploration
- Loaded all 8 datasets using Pandas
- Inspected structure using head(), info(), describe()
- Identified primary and foreign keys
- Understood relationships between tables

### Step 2: Data Cleaning and Preprocessing
- Handled missing values based on count
  - Below 1000 missing: filled with median or placeholder text
  - Above 1000 missing: rows dropped
- Removed duplicate records from all tables
- Converted date columns from object to datetime format
- Validated data ranges for price, payment value, and review scores
- Standardized all column names to lowercase with underscores

### Step 3: Data Integration
- Merged all 8 tables into one Master Dataset
- Used GroupBy and aggregation for one-to-many relationships
- Final Master Dataset contains 42 columns

### Step 4: Feature Engineering
Created new features out of all the tables.


### Step 5: Exploratory Data Analysis
Performed structured analysis across 5 dimensions:
- Customer Analysis (new vs repeat, segments, geography)
- Revenue and Order Analysis (monthly trends, peak periods)
- Product Analysis (top categories, revenue contribution)
- Seller Analysis (top performers, distribution)
- Review and Satisfaction Analysis (scores, delivery impact)

### Step 6: Data Visualization
Created the following visualizations using Matplotlib and Seaborn:
- Time series plots for monthly revenue and order volume trends
- Bar charts for top categories, states, and customer segments
- Histograms for order value, delivery time, and CLV distribution
- Box plots for order value by segment and delivery time by rating
- Heatmaps for correlation analysis, revenue by month, and orders by day and hour

---

## Technologies Used

- Python 3
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---
