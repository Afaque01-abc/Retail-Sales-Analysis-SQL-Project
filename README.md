

# **Retail Sales Analysis SQL Project**

## **Project Overview**

**Level:** Beginner
**Database:** `p1_retail_db`

This project demonstrates SQL skills and techniques typically used by data analysts to **explore, clean, and analyze retail sales data**.
It involves setting up a retail sales database, performing exploratory data analysis (EDA), and answering business questions through SQL queries.


---

## **Objectives**

* **Database Setup:** Create and populate a retail sales database.
* **Data Cleaning:** Identify and remove records with missing/null values.
* **Exploratory Data Analysis (EDA):** Understand the dataset.
* **Business Analysis:** Use SQL to answer business questions & extract insights.

---

## **Project Structure**

### **1. Database Setup**

```sql
CREATE DATABASE p1_retail_db;

CREATE TABLE retail_sales (
    transactions_id INT PRIMARY KEY,
    sale_date DATE,	
    sale_time TIME,
    customer_id INT,	
    gender VARCHAR(10),
    age INT,
    category VARCHAR(35),
    quantity INT,
    price_per_unit FLOAT,	
    cogs FLOAT,
    total_sale FLOAT
);
```

---

### **2. Data Exploration & Cleaning**

```sql
-- Record count
SELECT COUNT(*) FROM retail_sales;

-- Unique customers
SELECT COUNT(DISTINCT customer_id) FROM retail_sales;

-- Unique categories
SELECT DISTINCT category FROM retail_sales;

-- Check for NULL values
SELECT * FROM retail_sales
WHERE sale_date IS NULL OR sale_time IS NULL OR customer_id IS NULL 
  OR gender IS NULL OR age IS NULL OR category IS NULL 
  OR quantity IS NULL OR price_per_unit IS NULL OR cogs IS NULL;

-- Delete rows with NULL values
DELETE FROM retail_sales
WHERE sale_date IS NULL OR sale_time IS NULL OR customer_id IS NULL 
  OR gender IS NULL OR age IS NULL OR category IS NULL 
  OR quantity IS NULL OR price_per_unit IS NULL OR cogs IS NULL;
```

---

### **3. Business Analysis SQL Queries**

* Sales on a specific date
* Clothing category sales > 4 units in Nov 2022
* Total sales per category
* Average age of Beauty category customers
* High-value transactions (> 1000)
* Sales by gender & category
* Best-selling month per year
* Top 5 customers by total sales
* Unique customers per category
* Orders by shift (Morning, Afternoon, Evening)

Full query list is included in [`analysis_queries.sql`](sql_query_p1.sql
).

---

## **Findings**

* **Customer Demographics:** Wide range of ages & categories.
* **High-Value Transactions:** Many sales over 1000.
* **Seasonality:** Peaks in certain months.
* **Top Customers:** Clear high spenders by category.

---

## **Reports**

* **Sales Summary** – Overall performance & demographics
* **Trend Analysis** – Seasonal & time-based patterns
* **Customer Insights** – Loyalty & top spenders

---

## **Conclusion**

This project serves as a **complete SQL case study** for beginner analysts.
It covers **database creation, cleaning, analysis, and insights extraction**—skills crucial for real-world analytics work.

---




