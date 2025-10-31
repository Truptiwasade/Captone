
# 🛒 E-Commerce Database Analysis – SQL Project

## 📘 Overview

This project focuses on **data analysis and cleaning using SQL** for an e-commerce business.
The database contains information about **customers, orders, products, order items, and returns**, enabling insights into **sales performance, customer behavior, and operational efficiency**.

The project is divided into **14 well-structured sections**, starting from database setup to advanced analytical queries.

---

## 🧩 Database Structure

### **Tables**

1. **customers** – Stores customer details (ID, name, email, signup date, region)
2. **orders** – Contains order information (order ID, customer ID, date, total amount)
3. **order_items** – Includes each product item in an order (order item ID, order ID, product ID, price, quantity)
4. **products** – Product catalog (product ID, name, category, price)
5. **returns** – Return and refund details (return ID, order ID, return date, reason)

---

## ⚙️ SECTION 1: Database Setup

* Creates and selects the `ecommercedb` database.
* Displays all tables to confirm structure and connectivity.

---

## 🔍 SECTION 2: Data Preview & Exploration

* Previews the first 5 rows of each table using `LIMIT 5`.
* Helps verify data import and column structure.

---

## 🧹 SECTION 3: Data Quality – Nulls & Missing Values

* Checks for missing or `NULL` values in every table.
* Calculates **percentage of NULLs** for customer columns.
* Ensures completeness and identifies areas requiring data cleaning.

---

## 📊 SECTION 4: Basic Statistics & Summary

* Computes **min, max, avg, and sum** for order amounts and item prices.
* Provides initial understanding of sales distributions and value ranges.

---

## 🧭 SECTION 5: Duplicate Data Handling

* Detects duplicate entries in:

  * Customer emails
  * Orders per customer-date
  * Repeated products within same order
* Removes duplicates using **CTE (Common Table Expressions)** and **window functions**.

---

## 🧼 SECTION 6: Data Validation & Cleaning

* Identifies invalid or blank email addresses using regex patterns.
* Replaces missing regions with `"Unknown"` using `COALESCE()`.
* Filters out orders with missing `total_amount`.

---

## 🔗 SECTION 7: Referential Integrity Checks

* Ensures **foreign key consistency**:

  * Orders link to existing customers.
  * Order items link to valid products.
  * Returns reference valid orders.

---

## 💰 SECTION 8: Sales & Revenue Analysis

* Calculates:

  * **Revenue by category**
  * **Top 5 products by revenue**
  * **Orders per customer**
  * **Average Order Value (AOV)**
  * **Customer-level total revenue**
* Core section for **business revenue insights**.

---

## ⏱️ SECTION 9: Time-Based Analysis

* Evaluates sales trends over time:

  * **Monthly revenue trends**
  * **Daily order counts**
* Useful for seasonality and performance tracking.

---

## 🧾 SECTION 10: Product & Category Analysis

* Tracks **category performance per month**.
* Finds **first order date** per customer (for retention analysis).

---

## 👥 SECTION 11: Customer Behavior & Cohorts

* Groups customers by **signup month**.
* Calculates **early activation** (orders within 30 days of signup).
* Helps understand customer engagement patterns.

---

## 🧮 SECTION 12: Window Functions & Analytics

* Uses `DENSE_RANK()` to **rank customers by total revenue**.
* Demonstrates advanced SQL analytics capabilities.

---

## 🔄 SECTION 13: Returns & Refund Analysis

* Calculates:

  * **Return rate (% of total orders)**
  * **Most common return reasons**
  * **Total refund value (revenue loss)**

---

## 🌍 SECTION 14: Geographical Insights

* Analyzes customers and revenue by **region**.
* Identifies top-performing geographical areas.

---

## 🧠 Key Learnings

* Data cleaning & validation using SQL.
* Applying window functions and CTEs.
* Performing business-oriented analytical queries.
* Building end-to-end database analytics workflow.

---

## 🛠️ Tools Used

* **Database:** MySQL / SQL Workbench
* **Language:** Structured Query Language (SQL)
* **Concepts Used:**

  * Aggregations (`SUM`, `AVG`, `COUNT`)
  * Joins (INNER, LEFT JOIN)
  * Window Functions (`ROW_NUMBER`, `DENSE_RANK`)
  * CTEs for de-duplication
  * Data validation using regex

---

## 📈 Conclusion

This project demonstrates how **SQL can be used to clean, validate, and analyze e-commerce data** effectively.
It provides valuable insights into **sales, customers, products, and returns**, supporting data-driven decision-making for business growth.

---

## 📂 File Information

* **Filename:** `ecommerce_analysis.sql`
* **Database:** `ecommercedb`
* **Author:** *[Your Name]*
* **Version:** 1.0

