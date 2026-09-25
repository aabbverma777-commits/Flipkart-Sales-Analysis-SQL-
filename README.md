<div align="center">

# 🛒 Flipkart E-Commerce Sales Analysis

### 📊 SQL Data Analytics Project using MySQL

<img src="https://img.shields.io/badge/SQL-MySQL%208.0%2B-4479A1?style=for-the-badge&logo=mysql&logoColor=white">
<img src="https://img.shields.io/badge/Data%20Analytics-SQL-orange?style=for-the-badge&logo=googleanalytics&logoColor=white">
<img src="https://img.shields.io/badge/Database-Flipkart-blue?style=for-the-badge&logo=databricks&logoColor=white">
<img src="https://img.shields.io/badge/Project-Business%20Analysis-success?style=for-the-badge">



### 🚀 Turning E-Commerce Data into Meaningful Business Insights Using SQL

</div>

---

# 📑 Table of Contents

- [📖 Project Overview](#-project-overview)
- [🎯 Project Objectives](#-project-objectives)
- [📂 Dataset Information](#-dataset-information)
- [🗂️ Dataset Structure](#️-dataset-structure)
- [🔗 Dataset Relationships](#-dataset-relationships)
- [🛠️ Tools & Technologies](#️-tools--technologies)
- [🧠 SQL Concepts Used](#-sql-concepts-used)
- [🔄 Data Analysis Workflow](#-data-analysis-workflow)
- [📊 Business Questions Covered](#-business-questions-covered)
- [📈 Analysis Areas](#-analysis-areas)
- [💡 Key Insights](#-key-insights)
- [🧮 Sample SQL Queries](#-sample-sql-queries)
- [📁 Project Structure](#-project-structure)
- [🚀 How to Run the Project](#-how-to-run-the-project)
- [🌟 Skills Demonstrated](#-skills-demonstrated)
- [🏁 Conclusion](#-conclusion)
- [👨‍💻 Author](#-author)

---

# 📖 Project Overview

**Flipkart E-Commerce Sales Analysis** is a SQL-based Data Analytics project
developed using **MySQL**.

The main purpose of this project is to analyze e-commerce data related to:

- 👥 Customers
- 📦 Products
- 🛒 Sales & Orders
- 🌍 Geographic Performance
- 💳 Payment Behavior
- 🚚 Delivery Performance
- 💰 Revenue
- 🏷️ Discounts
- ⭐ Product Ratings & Reviews
- 🔁 Customer Repeat Purchases

The project transforms raw transactional data into meaningful
**business insights using SQL queries**.

The SQL project contains **52 business questions and SQL solutions** covering
basic data exploration, aggregations, joins, CASE statements, date functions,
and subqueries.

---

# 🎯 Project Objectives

### 💰 Sales & Revenue Analysis
- Analyze total revenue
- Calculate average order value
- Identify high-value orders
- Analyze monthly, quarterly and yearly revenue

### 👥 Customer Analysis
- Understand customer purchasing behavior
- Analyze customer age groups
- Identify repeat customers
- Find high-value customers
- Analyze customer tiers

### 📦 Product Analysis
- Identify top-performing products
- Analyze product categories and brands
- Analyze product quantity sold
- Analyze product ratings and reviews

### 🌍 Geographic Analysis
- Analyze state-wise revenue
- Analyze city-wise revenue
- Identify high-performing states and cities

### 💳 Payment Analysis
- Identify payment methods
- Compare payment methods by revenue and order count

### 🚚 Delivery Analysis
- Calculate delivery success percentage
- Calculate average delivery time
- Compare delivery performance across states

### 🏷️ Discount Analysis
- Analyze discount percentages
- Create discount buckets
- Compare original and selling prices

---

# 📂 Dataset Information

The project uses an e-commerce dataset consisting of **three major tables**:

| 🗃️ Table | 📌 Description |
|---|---|
| 👥 `customers` | Customer master data |
| 📦 `products` | Product and catalog data |
| 🛒 `sales` | Order-level transaction data |

### 🗄️ Database

```text
flipkart_db
```

### 💻 Database System

```text
MySQL 8+
```

---

# 🗂️ Dataset Structure

## 👥 1. Customers Table

```text
customers
│
├── Customer_ID
├── Customer_Name
├── Gender
├── Age
├── Age_Group
├── Date_of_Birth
├── Email
├── Phone
├── City
├── State
├── Pincode
├── Registration_Date
├── Customer_Tier
├── Total_Orders
└── Total_Spent
```

**Used for:** customer segmentation, customer tiers, customer value,
geographic analysis and repeat-customer analysis.

---

## 📦 2. Products Table

```text
products
│
├── Product_ID
├── Product_Name
├── Category
├── Brand
├── Original_Price
├── Discount_Percent
├── Discount_Amount
├── Selling_Price
├── Stock_Quantity
├── Weight_kg
├── Avg_Rating
└── Total_Reviews
```

**Used for:** product, category, brand, pricing, discount, rating and review analysis.

---

## 🛒 3. Sales Table

Important analytical fields include:

```text
sales
│
├── Order_ID
├── Customer_ID
├── Product_ID
├── Order_Date
├── Delivery_Date
├── Quantity
├── Total_Amount
├── Order_Status
├── Payment_Mode
├── Customer_Age_Group
├── City
└── State
```

**Used for:** revenue, orders, payment, delivery, customer, geographic
and time-based analysis.

---

# 🔗 Dataset Relationships

```text
                    ┌───────────────────────┐
                    │       👥 CUSTOMERS     │
                    │    Customer_ID        │
                    │    Customer_Name      │
                    │    Customer_Tier      │
                    └───────────┬───────────┘
                                │
                                │ Customer_ID
                                ▼
                    ┌───────────────────────┐
                    │        🛒 SALES       │
                    │    Order_ID           │
                    │    Customer_ID        │
                    │    Product_ID         │
                    │    Total_Amount       │
                    │    Payment_Mode       │
                    │    Order_Date         │
                    └───────────┬───────────┘
                                │
                                │ Product_ID
                                ▼
                    ┌───────────────────────┐
                    │       📦 PRODUCTS     │
                    │    Product_ID         │
                    │    Product_Name       │
                    │    Category           │
                    │    Brand              │
                    │    Selling_Price      │
                    │    Discount_Percent   │
                    └───────────────────────┘
```

---

# 🛠️ Tools & Technologies

| 🛠️ Tool / Technology | 🎯 Purpose |
|---|---|
| 🐬 **MySQL** | Database Management |
| 💻 **MySQL Workbench** | SQL Development & Query Execution |
| 🧠 **SQL** | Data Analysis |
| 🗃️ **Relational Database** | Data Storage |
| 📊 **Dashboard** | Business Visualization |
| 📝 **GitHub** | Project Documentation |

---

# 🧠 SQL Concepts Used

### 🔹 Basic SQL
```sql
SELECT
WHERE
ORDER BY
DISTINCT
LIMIT
```

### 🔹 Aggregate Functions
```sql
COUNT()
SUM()
AVG()
MIN()
MAX()
ROUND()
```

### 🔹 Grouping
```sql
GROUP BY
HAVING
```

### 🔹 Conditional Logic
```sql
CASE
WHEN
THEN
ELSE
END
```

### 🔹 Joins
```sql
INNER JOIN
LEFT JOIN
```

### 🔹 Date Functions
```sql
YEAR()
MONTH()
MONTHNAME()
QUARTER()
DATEDIFF()
```

### 🔹 Other Concepts
- Subqueries
- NULL handling
- Data filtering
- Sorting
- Distinct values

---

# 🔄 Data Analysis Workflow

```text
                 📥 RAW E-COMMERCE DATA
                           │
                           ▼
                  🗄️ CREATE DATABASE
                           │
                           ▼
                    📋 CREATE TABLES
                           │
                           ▼
                   🔍 DATA EXPLORATION
                           │
                           ▼
                  🧹 DATA UNDERSTANDING
                           │
                           ▼
                  📊 BUSINESS QUESTIONS
                           │
                           ▼
                    🧮 SQL ANALYSIS
                           │
              ┌────────────┼────────────┐
              ▼            ▼            ▼
          👥 CUSTOMER   📦 PRODUCT    🛒 SALES
              │            │            │
              └────────────┼────────────┘
                           ▼
                      🔗 JOINS
                           │
                           ▼
                  📈 BUSINESS INSIGHTS
                           │
                           ▼
                    📊 DASHBOARD
                           │
                           ▼
                      🎯 CONCLUSION
```

---

# 📊 Business Questions Covered

The project contains **52 important business questions**.

## 📌 Basic Business Overview

1. How many customers are present?
2. How many products are available?
3. How many sales/order records are present?
4. What is the total revenue generated?
5. What is the total quantity of products sold?
6. What is the average order value?
7. What is the highest order value?
8. What is the lowest order value?
9. How many unique cities are represented?
10. How many unique states are represented?

## 📌 Sales & Order Analysis

11. Orders by order status
12. Available payment methods
13. Highest-value orders above 50,000
14. Revenue by state
15. Top 10 states by revenue
16. Revenue by payment mode
17. Orders by payment mode
18. Revenue by order status
19. Monthly revenue trend
20. Yearly revenue

## 📌 Location & Customer Analysis

21. Quarterly revenue
22. Revenue by city
23. Top 10 cities by revenue
24. Revenue by customer age group
25. Age group with highest orders
26. Age group with highest revenue
27. States with more than 100 unique customers
28. Customers with more than 5 orders
29. Repeat customers

## 📌 Product & Category Analysis

30. Average rating by category
31. Product count by category
32. Product count by brand
33. Average selling price by category
34. Revenue by product category
35. Revenue by brand
36. Top revenue-generating products
37. Products with highest sales quantity
38. Category with highest quantity sold

## 📌 Discount & Pricing Analysis

39. Products with discount of 20% or more
40. Average discount percentage by category
41. Difference between original and selling price
42. Products with highest number of reviews
43. Products by discount bucket

## 📌 Customer & Payment Insights

44. Revenue by customer tier
45. Highest revenue-generating customers
46. Average order value by payment mode
47. Most preferred payment mode

## 📌 Delivery & Business Performance

48. Delivery success percentage
49. Average delivery time
50. States with highest average delivery time

## 📌 Subquery Analysis

51. Orders above average order value
52. Products above overall average rating

---

# 📈 Analysis Areas

## 💰 Revenue Analysis

Revenue is analyzed using:

```sql
SUM(Total_Amount)
```

Analysis levels include:

```text
🌍 State
🏙️ City
📦 Category
🏷️ Brand
👥 Customer
💳 Payment Mode
📅 Month
📆 Year
📊 Quarter
```

---

## 👥 Customer Analysis

```text
                 👥 CUSTOMER
                      │
          ┌───────────┼───────────┐
          ▼           ▼           ▼
      🎂 Age       👑 Tier     🌍 Location
          │           │           │
          └───────────┼───────────┘
                      ▼
                 🛒 Orders
                      │
              ┌───────┴───────┐
              ▼               ▼
         👤 One-Time      🔁 Repeat
         Customer         Customer
```

---

## 📦 Product Analysis

Product performance is evaluated using:

- 💰 Revenue
- 📦 Quantity Sold
- ⭐ Average Rating
- 📝 Total Reviews
- 🏷️ Discount Percentage
- 💵 Selling Price
- 🗂️ Category
- 🏷️ Brand

---

## 💳 Payment Analysis

Payment methods are analyzed using:

- 📊 Number of orders
- 💰 Total revenue
- 💵 Average order value

Payment methods include:

```text
💳 UPI
💵 COD
💳 Debit Card
💳 Credit Card
```

---

## 🚚 Delivery Analysis

Delivery performance is measured using:

```sql
DATEDIFF(Delivery_Date, Order_Date)
```

### Key KPIs

```text
🚚 Delivery Success %
⏱️ Average Delivery Days
🌍 State-wise Delivery Time
```

---

## 🏷️ Discount Analysis

Products are divided into:

```text
🟢 No Discount      → 0%
🟡 Low Discount     → 1% – 10%
🟠 Medium Discount  → 11% – 20%
🔴 High Discount    → >20%
```

---

# 💡 Key Insights

> These insights are based on the dashboard/business-insight section
> contained in the SQL project.

### 📈 1. Sales Growth

The dashboard presents an overall positive sales trend with multiple
high-performing months. Monthly revenue analysis identifies the months
responsible for the strongest revenue contribution.

### 🌍 2. Geographic Performance

The dashboard highlights:

```text
🇮🇳 Uttar Pradesh
🇮🇳 Rajasthan
🇮🇳 Haryana
```

as major sales-contributing states.

### 👥 3. Customer Age Group

The dashboard highlights:

```text
🥇 26–35
🥈 18–25
🥉 36–45
```

as important customer segments in the transaction mix.

### 💳 4. Payment Preference

The dashboard highlights:

```text
🥇 UPI
🥈 COD
🥉 Debit Card
4️⃣ Credit Card
```

### 🚚 5. Delivery Performance

The dashboard indicates a high proportion of successfully delivered
orders. Delivery success percentage and average delivery time provide
operational KPIs.

### 🔁 6. Customer Engagement

The analysis focuses on repeat-order activity and separates one-time
customers from customers who place multiple orders.

### 📦 7. Product Performance

Product-level analysis combines revenue, quantity sold, rating and
review counts to understand product contribution.

### 🏷️ 8. Discount Analysis

Discount buckets separate products into no-discount, low, medium and
high-discount groups.

### 🚛 9. Operational Performance

Shipping cost and delivery-time analysis by state can reveal geographic
differences in fulfillment performance.

### 👑 10. Customer Value

Customer-level revenue and customer-tier analysis identify customers
contributing the greatest monetary value.

---

# 📊 Project Highlights

| 📌 Area | 🔍 Analysis |
|---|---|
| 💰 Revenue | State, City, Category, Brand & Customer |
| 👥 Customers | Age Group, Tier & Repeat Customers |
| 📦 Products | Category, Brand, Rating & Quantity |
| 💳 Payments | Orders, Revenue & Average Order Value |
| 🚚 Delivery | Success Rate & Delivery Time |
| 🏷️ Discounts | Discount Percentage & Buckets |
| 📅 Time | Monthly, Quarterly & Yearly |
| 🌍 Geography | State & City Performance |

---

# 🧮 Sample SQL Queries

## 💰 State-wise Revenue

```sql
SELECT
    State,
    ROUND(SUM(Total_Amount), 2) AS Total_Revenue
FROM sales
GROUP BY State
ORDER BY Total_Revenue DESC;
```

## 🏆 Top 10 States by Revenue

```sql
SELECT
    State,
    ROUND(SUM(Total_Amount), 2) AS Total_Revenue
FROM sales
GROUP BY State
ORDER BY Total_Revenue DESC
LIMIT 10;
```

## 📦 Category-wise Revenue

```sql
SELECT
    p.Category,
    ROUND(SUM(s.Total_Amount), 2) AS Total_Revenue
FROM sales s
INNER JOIN products p
    ON s.Product_ID = p.Product_ID
GROUP BY p.Category
ORDER BY Total_Revenue DESC;
```

## 🔁 Repeat Customers

```sql
SELECT
    Customer_ID,
    COUNT(DISTINCT Order_ID) AS Total_Orders
FROM sales
GROUP BY Customer_ID
HAVING COUNT(DISTINCT Order_ID) > 1
ORDER BY Total_Orders DESC;
```

## 🚚 Delivery Success Percentage

```sql
SELECT
    ROUND(
        100.0 *
        SUM(
            CASE
                WHEN Order_Status = 'Delivered'
                THEN 1
                ELSE 0
            END
        ) / COUNT(*),
        2
    ) AS Delivery_Success_Percentage
FROM sales;
```

## ⭐ Products Above Average Rating

```sql
SELECT
    Product_ID,
    Product_Name,
    Avg_Rating
FROM products
WHERE Avg_Rating > (
    SELECT AVG(Avg_Rating)
    FROM products
)
ORDER BY Avg_Rating DESC;
```

---

# 📁 Project Structure

```text
📦 Flipkart-SQL-Data-Analytics
│
├── 📄 Flipkart Sql Project.sql
├── 📄 README.md
│
├── 📊 Dashboard
│   └── Flipkart Dashboard
│
└── 📂 Dataset
    ├── 👥 customers.csv
    ├── 📦 products.csv
    └── 🛒 sales.csv
```

---

# 🚀 How to Run the Project

### 1️⃣ Install MySQL

Install MySQL Server and MySQL Workbench.

### 2️⃣ Create Database

```sql
CREATE DATABASE flipkart_db;
```

### 3️⃣ Select Database

```sql
USE flipkart_db;
```

### 4️⃣ Create Tables

Create:

```text
customers
products
sales
```

### 5️⃣ Load Dataset

Load the customer, product and sales data into the respective tables.

### 6️⃣ Run SQL File

Open:

```text
Flipkart Sql Project.sql
```

and execute the queries in MySQL Workbench.

### 7️⃣ Analyze Results

Analyze:

```text
💰 Revenue
👥 Customers
📦 Products
🛒 Orders
💳 Payments
🚚 Delivery
🏷️ Discounts
🌍 Geography
📅 Time Trends
```

---

# 🌟 Skills Demonstrated

```text
🐬 MySQL
🧠 SQL Problem Solving
🔍 Data Exploration
📊 Data Analysis
🧮 Aggregation
🔗 Table Joins
👥 Customer Analytics
📦 Product Analytics
💰 Revenue Analytics
🚚 Operational Analytics
📅 Time-Based Analysis
📈 Business Insights
```

---

# 🏁 Conclusion

This **Flipkart SQL Data Analytics Project** demonstrates how raw
e-commerce transaction data can be transformed into structured
business information using MySQL.

The project moves from basic data exploration to business analysis using:

```text
SELECT
WHERE
ORDER BY
GROUP BY
HAVING
CASE
JOIN
Aggregation
Date Functions
Subqueries
```

The analysis provides a framework for understanding:

- 💰 Product performance
- 🏷️ Discounts and coupons
- 👥 Customer value
- 💳 Payment behavior
- 🌍 Geographic performance
- 🚚 Delivery operations
- 📅 Monthly trends
- 🔁 Customer engagement

The SQL analysis can also serve as the analytical backend for an
Excel/dashboard-based Data Analytics project.

---

# 🎯 Final Project Flow

```text
             🛒 FLIPKART DATA
                    │
                    ▼
              🗄️ MYSQL DATABASE
                    │
                    ▼
        ┌───────────┼───────────┐
        │           │           │
        ▼           ▼           ▼
     👥 CUSTOMERS 📦 PRODUCTS 🛒 SALES
        │           │           │
        └───────────┼───────────┘
                    ▼
                 🔗 JOINS
                    │
                    ▼
             🧠 SQL ANALYSIS
                    │
                    ▼
             📊 52 QUESTIONS
                    │
                    ▼
             💡 KEY INSIGHTS
                    │
                    ▼
              📈 DASHBOARD
                    │
                    ▼
              🎯 BUSINESS
                INSIGHTS
```

---

# 👨‍💻 Author

<div align="center">

## **Abhishek Verma**

### 📊 Data Analytics Enthusiast

**SQL | MySQL | Excel | Python | Data Analytics**

<br>

<img src="https://img.shields.io/badge/Author-Abhishek%20Verma-blue?style=for-the-badge">
<img src="https://img.shields.io/badge/Field-Data%20Analytics-orange?style=for-the-badge">
<img src="https://img.shields.io/badge/Project-SQL%20Analytics-success?style=for-the-badge">

<br><br>

### ⭐ If you found this project useful, consider giving it a Star!

⭐ **Star this Repository**  
🍴 **Fork this Repository**  
📢 **Share this Project**

</div>

---

<div align="center">

# 🛒 Flipkart E-Commerce Sales Analysis

### Turning Data → SQL Analysis → Insights → Business Understanding

<br>

<img src="https://img.shields.io/badge/Made%20with-SQL-blue?style=for-the-badge&logo=mysql&logoColor=white">
<img src="https://img.shields.io/badge/MySQL-8.0%2B-4479A1?style=for-the-badge&logo=mysql&logoColor=white">
<img src="https://img.shields.io/badge/Hosted%20on-GitHub-black?style=for-the-badge&logo=github">

<br><br>

**© 2026 Abhishek Verma**

</div>
