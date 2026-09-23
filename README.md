# 🛒 Flipkart Sales Analysis — SQL Data Analytics Project

<p align="center">
  <img src="https://img.shields.io/badge/SQL-MySQL%208.0%2B-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL">
  <img src="https://img.shields.io/badge/Data%20Analysis-SQL-00A98F?style=for-the-badge&logo=databricks&logoColor=white" alt="Data Analysis">
  <img src="https://img.shields.io/badge/Project-Flipkart%20Sales-2874F0?style=for-the-badge" alt="Flipkart Sales">
  <img src="https://img.shields.io/badge/Author-Abhishek%20Verma-111827?style=for-the-badge&logo=github&logoColor=white" alt="Author">
</p>

<p align="center">
  <strong>📊 A beginner-friendly SQL Data Analytics project focused on analyzing sales, customers, products, payments, geography, and delivery performance.</strong>
</p>

---


------------------------------------------------------------------------

# 📌 Table of Contents

-   [📖 Project Overview](#-project-overview)
-   [🎯 Project Objectives](#-project-objectives)
-   [🗂️ Database Structure](#️-database-structure)
-   [📊 Dataset Tables](#-dataset-tables)
-   [🧠 SQL Concepts Used](#-sql-concepts-used)
-   [🔍 Analysis Covered](#-analysis-covered)
-   [💼 Business Questions](#-business-questions)
-   [📈 Business Insights](#-business-insights)
-   [💡 Key Findings](#-key-findings)
-   [🛠️ Tools & Technologies](#️-tools--technologies)
-   [🚀 How to Run the Project](#-how-to-run-the-project)
-   [📁 Project Structure](#-project-structure)
-   [📌 Conclusion](#-conclusion)
-   [👨‍💻 Author](#-author)

------------------------------------------------------------------------

# 📖 Project Overview

**Flipkart Sales Analysis** is a SQL-based data analytics project
designed to analyze an e-commerce sales database and extract useful
business information.

The project works with three main tables:

-   👥 `customers`
-   📦 `products`
-   🛍️ `sales`

The analysis starts with basic data exploration and gradually moves into
aggregation, filtering, `GROUP BY`, `HAVING`, `CASE`, joins, subqueries
and business-oriented analysis.

The main purpose is to convert raw sales data into meaningful
information about:

> **Revenue • Customers • Products • Categories • Brands • Payments •
> Geography • Orders • Discounts • Ratings • Delivery**

------------------------------------------------------------------------

# 🎯 Project Objectives

### The project aims to answer questions such as:

  Area            Business Question
  --------------- --------------------------------------------------------
  💰 Revenue      How much revenue is generated?
  🛒 Sales        How many products and orders are sold?
  👥 Customers    Who are the most valuable and repeat customers?
  📦 Products     Which products generate the most revenue?
  🏷️ Categories   Which categories contribute most to sales?
  ⭐ Ratings      How are products rated by customers?
  💳 Payments     Which payment methods are most frequently used?
  🌍 Geography    Which states and cities generate the most revenue?
  🎁 Discounts    How are discounts distributed across products?
  🚚 Delivery     What is the average delivery time and success rate?
  📈 Trends       How does revenue change monthly, quarterly and yearly?

------------------------------------------------------------------------

# 🗂️ Database Structure

The project uses a simple relational database containing three major
tables.

``` text
                    ┌────────────────────┐
                    │     CUSTOMERS      │
                    ├────────────────────┤
                    │ Customer_ID        │
                    │ Customer_Name      │
                    │ Customer_Tier      │
                    │ Total_Spent        │
                    │ Gender             │
                    └─────────┬──────────┘
                              │
                              │ Customer_ID
                              │
                    ┌─────────▼──────────┐
                    │       SALES        │
                    ├────────────────────┤
                    │ Order_ID           │
                    │ Order_Date         │
                    │ Customer_ID       │
                    │ Product_ID        │
                    │ Total_Amount      │
                    │ Quantity          │
                    │ City              │
                    │ State             │
                    │ Payment_Mode      │
                    │ Order_Status      │
                    │ Delivery_Date     │
                    │ Rating            │
                    └─────────┬──────────┘
                              │
                              │ Product_ID
                              │
                    ┌─────────▼──────────┐
                    │      PRODUCTS      │
                    ├────────────────────┤
                    │ Product_ID         │
                    │ Product_Name       │
                    │ Category           │
                    │ Brand              │
                    │ Discount_Percent   │
                    │ Original_Price     │
                    │ Selling_Price      │
                    │ Avg_Rating         │
                    │ Total_Reviews      │
                    │ Stock_Quantity     │
                    └────────────────────┘
```

------------------------------------------------------------------------

# 📊 Dataset Tables

## 👥 `customers`

Contains customer-level information.

**Important columns:**

-   `Customer_ID`
-   `Customer_Name`
-   `Customer_Tier`
-   `Total_Spent`
-   `Gender`

------------------------------------------------------------------------

## 📦 `products`

Contains product information, pricing, ratings and inventory details.

**Important columns:**

-   `Product_ID`
-   `Product_Name`
-   `Category`
-   `Brand`
-   `Discount_Percent`
-   `Original_Price`
-   `Selling_Price`
-   `Avg_Rating`
-   `Total_Reviews`
-   `Stock_Quantity`

------------------------------------------------------------------------

## 🛍️ `sales`

Contains individual order/sales records.

**Important columns:**

-   `Order_ID`
-   `Order_Date`
-   `Customer_ID`
-   `Product_ID`
-   `Total_Amount`
-   `Quantity`
-   `City`
-   `State`
-   `Payment_Mode`
-   `Order_Status`
-   `Customer_Age_Group`
-   `Delivery_Date`
-   `Rating`

------------------------------------------------------------------------

# 🧠 SQL Concepts Used

This project focuses on practical SQL concepts that are useful for a
beginner-to-intermediate Data Analyst.

### 🔹 Basic SQL

-   `SELECT`
-   `FROM`
-   `WHERE`
-   `DISTINCT`
-   `ORDER BY`
-   `LIMIT`

### 🔹 Aggregation

-   `COUNT()`
-   `SUM()`
-   `AVG()`
-   `MIN()`
-   `MAX()`
-   `ROUND()`

### 🔹 Grouping

-   `GROUP BY`
-   `HAVING`

### 🔹 Conditional Analysis

-   `CASE`
-   `WHEN`
-   `THEN`
-   `ELSE`

### 🔹 Table Relationships

-   `INNER JOIN`
-   `LEFT JOIN`

### 🔹 Subqueries

Used for comparisons against:

-   Average order value
-   Average product rating
-   Average state revenue
-   Repeat customers
-   Customer spending

### 🔹 Date Analysis

-   `YEAR()`
-   `MONTH()`
-   `MONTHNAME()`
-   `QUARTER()`
-   `DATEDIFF()`

### 🔹 Data Handling

-   `COALESCE()`
-   `NULL` checks
-   `TRIM()`

------------------------------------------------------------------------

# 🔍 Analysis Covered

The project explores the following areas:

``` text
📊 Overall Sales
      ↓
💰 Revenue Analysis
      ↓
📅 Monthly / Quarterly / Yearly Trends
      ↓
🌍 State & City Analysis
      ↓
👥 Customer Analysis
      ↓
📦 Product & Category Analysis
      ↓
🏷️ Brand Analysis
      ↓
💳 Payment Analysis
      ↓
🎁 Discount & Pricing Analysis
      ↓
⭐ Rating & Review Analysis
      ↓
🚚 Delivery Analysis
      ↓
💼 Business Insights

------------------------------------------------------------------------

# 📈 Business Insights

The following insights are based on the dashboard observations
documented in the SQL project. The listed questions can be used to
validate each observation against the underlying data.

------------------------------------------------------------------------

## 🚀 1. Sales Show Strong Growth

The dashboard highlights a positive sales trend over time, with multiple
high-performing months.



------------------------------------------------------------------------

## 🌍 2. Top States Drive Maximum Sales

The dashboard identifies **Uttar Pradesh, Rajasthan and Haryana** among
the states contributing the highest sales.





------------------------------------------------------------------------

## 👥 3. Young Customers Lead Purchases

The dashboard shows the **26--35 age group** as the largest contributor
to total sales, followed by **18--25** and **36--45**.




------------------------------------------------------------------------

## 💳 4. UPI Is the Most Preferred Payment Method

The dashboard highlights **UPI** as the most preferred payment method,
followed by COD, Debit Card and Credit Card.



------------------------------------------------------------------------

## 🚚 5. High Order Delivery Success

The dashboard indicates that a large majority of orders are successfully
delivered.

This can be evaluated using order status, delivery percentage and
delivery-time analysis.



------------------------------------------------------------------------

## 🤝 6. Strong Customer Base & Engagement

The dashboard highlights a high number of unique customers and repeat
orders, helping analyze customer engagement.




------------------------------------------------------------------------

# 💡 Key Findings Framework

The project can be used to answer six major business areas:

### 💰 Revenue

Identify:

-   Total revenue
-   Average order value
-   Revenue by state
-   Revenue by city
-   Revenue by category
-   Revenue by brand
-   Revenue by payment mode
-   Revenue contribution percentages

### 👥 Customers

Identify:

-   Total customers
-   Repeat customers
-   High-value customers
-   Customer spending segments
-   Customer tiers
-   Age-group purchasing behavior

### 📦 Products

Identify:

-   Best-selling products
-   Highest-revenue products
-   Products with high reviews
-   Products with high ratings
-   Low-stock products
-   Products with high discounts

### 💳 Payments

Compare:

-   UPI
-   COD
-   Debit Card
-   Credit Card
-   Order count
-   Revenue
-   Average order value

### 🌍 Geography

Analyze:

-   States
-   Cities
-   State revenue
-   Top 10 states
-   Top 10 cities
-   Unique customers by state

### 🚚 Delivery

Analyze:

-   Delivery success percentage
-   Average delivery days
-   State-wise delivery time
-   Order status
-   Revenue by order status

------------------------------------------------------------------------

# 🛠️ Tools & Technologies

```{=html}
<p align="center">
```
`<img src="https://img.shields.io/badge/MySQL-8.0%2B-4479A1?style=flat-square&logo=mysql&logoColor=white">`{=html}
`<img src="https://img.shields.io/badge/SQL-Data%20Analysis-00A98F?style=flat-square">`{=html}
`<img src="https://img.shields.io/badge/GitHub-Version%20Control-181717?style=flat-square&logo=github&logoColor=white">`{=html}
`<img src="https://img.shields.io/badge/Data%20Analytics-Portfolio-FFB000?style=flat-square">`{=html}
```{=html}
</p>
```
### Main Technology

**MySQL 8.0+**

### Recommended SQL Environment

-   MySQL Workbench
-   MySQL Server 8.0+
-   GitHub

------------------------------------------------------------------------

# 🚀 How to Run the Project

## 1️⃣ Install MySQL

Install **MySQL Server 8.0+** and optionally MySQL Workbench.

------------------------------------------------------------------------

## 2️⃣ Create a Database

``` sql
CREATE DATABASE flipkart_sales_analysis;

USE flipkart_sales_analysis;
```

------------------------------------------------------------------------

## 3️⃣ Create the Tables

Create the following tables:

``` text
customers
products
sales
```

Make sure the column names match the SQL queries.

------------------------------------------------------------------------

## 4️⃣ Load the Data

Import the data into the corresponding tables:

``` text
customers → customers table
products  → products table
sales     → sales table
```

------------------------------------------------------------------------

## 5️⃣ Run the SQL File

Open:

``` text
Flipkart_Sales_Analysis.sql
```

Run the queries in MySQL Workbench.

------------------------------------------------------------------------

## 6️⃣ Explore the Results

Start with:

``` text
Q1 → Basic Data Exploration
Q16 → State Revenue
Q18 → Payment Revenue
Q21 → Monthly Trend
Q22 → Yearly Revenue
Q26 → Age Group Analysis
Q34 → Category Revenue
Q35 → Brand Revenue
Q43 → Top Products
Q44 → Customer Tier Revenue
Q57 → Top Customers
Q63 → State Contribution
Q73 → Preferred Payment Mode
Q75 → Delivery Time
```

------------------------------------------------------------------------

# 📁 Project Structure

Recommended GitHub repository structure:

``` text
📦 Flipkart-Sales-Analysis
│
├── 📄 README.md
├── 📄 Flipkart_Sales_Analysis.sql
│
├── 📁 assets
│   ├── 🖼️ flipkart-dashboard.png
│   ├── 🖼️ revenue-analysis.png
│   └── 🖼️ customer-analysis.png
│
└── 📁 data
    ├── customers.csv
    ├── products.csv
    └── sales.csv
```

> You can add your dashboard screenshots inside `assets/` and update the
> image names in this README.

------------------------------------------------------------------------

# 📊 Suggested Dashboard Sections

If this SQL project is connected to a BI dashboard, the dashboard can be
organized into:

### 🏠 Overview

-   Total Revenue
-   Total Orders
-   Total Quantity
-   Average Order Value
-   Delivery Success %

### 💰 Sales Analysis

-   Monthly Revenue
-   Quarterly Revenue
-   Yearly Revenue
-   Revenue by Order Status

### 🌍 Geography

-   State Revenue
-   Top 10 States
-   City Revenue
-   Top 10 Cities

### 👥 Customer Analysis

-   Age Group Revenue
-   Customer Tier Revenue
-   Top Customers
-   Repeat Customers

### 📦 Product Analysis

-   Category Revenue
-   Brand Revenue
-   Top Products
-   Quantity Sold
-   Ratings & Reviews

### 💳 Payment Analysis

-   Payment Mode Revenue
-   Payment Mode Orders
-   Average Order Value by Payment Mode

### 🚚 Delivery Analysis

-   Delivery Success %
-   Average Delivery Days
-   State-wise Delivery Time

------------------------------------------------------------------------

# 🧩 SQL Learning Journey

This project demonstrates a progression from simple SQL queries to
practical business analysis:

``` text
BEGINNER
   │
   ├── SELECT
   ├── WHERE
   ├── DISTINCT
   ├── ORDER BY
   └── LIMIT
   │
   ▼
INTERMEDIATE
   │
   ├── COUNT / SUM / AVG
   ├── GROUP BY
   ├── HAVING
   ├── CASE
   └── Date Functions
   │
   ▼
PRACTICAL ANALYTICS
   │
   ├── INNER JOIN
   ├── LEFT JOIN
   ├── Subqueries
   ├── Revenue Analysis
   ├── Customer Analysis
   └── Product Analysis
   │
   ▼
ADVANCED
   │
   └── Window Functions
       ├── RANK()
       ├── LAG()
       └── ROW_NUMBER()
```

------------------------------------------------------------------------

# 📌 Conclusion

The **Flipkart Sales Analysis** project demonstrates how SQL can be used
to transform transactional e-commerce data into meaningful business
information.

The analysis covers the complete journey from **basic data exploration
to business-focused insights**, including:

-   💰 Revenue performance
-   📈 Sales trends
-   🌍 Geographical performance
-   👥 Customer behavior
-   📦 Product performance
-   🏷️ Brand analysis
-   💳 Payment preferences
-   🎁 Discount analysis
-   ⭐ Ratings and reviews
-   🚚 Delivery performance

The project also demonstrates practical SQL skills including
**aggregation, filtering, grouping, conditional logic, joins, subqueries
and date-based analysis**.

Overall, this project provides a strong practical example of using SQL
for **e-commerce data analysis and business decision support**.

------------------------------------------------------------------------

# 🏆 Skills Demonstrated

```{=html}
<p align="center">
```
`SQL` • `MySQL` • `Data Cleaning` • `Data Exploration` • `Data Analysis`
• `Business Analysis` • `Aggregation` • `Joins` • `Subqueries` •
`CASE Statements` • `Date Analysis` • `E-commerce Analytics`

```{=html}
</p>
```

------------------------------------------------------------------------

# 👨‍💻 Author

## **Abhishek Verma**

🎓 **Data Analytics / SQL Project**

💡 Interested in:

-   Data Analytics
-   SQL
-   Business Intelligence
-   Data Visualization
-   E-commerce Analytics

------------------------------------------------------------------------

# ⭐ Support the Project

If you found this project useful:

⭐ **Star the repository**

🍴 **Fork the repository**

💬 **Share your feedback**

------------------------------------------------------------------------

```{=html}
<p align="center">
```
`<b>`{=html}🛒 Flipkart Sales Analysis`</b>`{=html}`<br>`{=html}
`<i>`{=html}Turning SQL queries into meaningful business
insights.`</i>`{=html}
```{=html}
</p>
```
```{=html}
<p align="center">
```
`<sub>`{=html}Made with ❤️ using MySQL & SQL`</sub>`{=html}
```{=html}
</p>
```
