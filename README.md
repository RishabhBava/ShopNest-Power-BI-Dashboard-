# 📊 ShopNest E-Commerce Data Analysis & Dashboard (Power BI)

## 🚀 Project Overview

This project focuses on analyzing **ShopNest (NexusGoods) e-commerce data** to uncover meaningful business insights using **data cleaning, data modeling, and interactive dashboarding in Power BI**.

The goal is to transform raw datasets into actionable insights that help understand:

* Customer behavior
* Sales performance
* Delivery efficiency
* Product trends

---

## 📁 Dataset Description

The project uses multiple datasets representing different aspects of an e-commerce business:

* Customers Dataset
* Geolocation Dataset
* Orders Dataset
* Order Items Dataset
* Order Payments Dataset
* Order Reviews Dataset
* Products Dataset
* Sellers Dataset
* Product Category Translation Dataset

---

## 🧹 Data Cleaning & Preprocessing

Data cleaning was performed using Power Query to ensure consistency, accuracy, and usability.

### Key Cleaning Steps:

* Removed duplicates from primary keys (Customer ID, Seller ID, Product ID)
* Standardized zip codes for proper dataset joins
* Converted data types (DateTime, Decimal, Whole Number)
* Handled missing values using:

  * Null replacement
  * Median imputation (for product dimensions)
* Standardized city names (capitalization)
* Replaced errors with null values
* Created a **Revenue column (Price + Freight)**

📄 Detailed documentation available here: 

---

## 🔗 Data Modeling

A well-structured relational model was built using **one-to-many relationships**.

### Key Relationships:

* Orders ↔ Customers (Customer ID)
* Orders ↔ Order Items (Order ID)
* Orders ↔ Payments (Order ID)
* Orders ↔ Reviews (Order ID)
* Order Items ↔ Products (Product ID)
* Order Items ↔ Sellers (Seller ID)
* Customers ↔ Geolocation (Zip Code)

### 📅 Date Table (DAX)

A custom Date Table was created for time-based analysis:

* Year, Month, Month Number, Quarter

---

## 📐 DAX Measures Created

* **Total Revenue** = Price + Freight
* **Total Orders** = Distinct Order Count
* **Average Rating** = Customer Satisfaction
* **Delayed Orders (By Category)**
* **Revenue by State**
* **Avg Rating by Product**
* **Total Payments by Method**

### 🚚 Delivery Status Logic:

```DAX
Delivery Status = 
IF(
    order_delivered_customer_date > order_estimated_delivery_date,
    "Delayed",
    "On-Time"
)
```

---

## 📊 Dashboard Insights

An interactive Power BI dashboard was created to visualize business performance.

📄 Dashboard documentation: 

### 🔍 Key Analysis Performed:

### 1️⃣ Top Categories by Sales

* Identified top 10 revenue-generating categories

### 2️⃣ Delayed Orders Analysis

* Highlighted categories with maximum delivery delays

### 3️⃣ Monthly Delivery Performance

* Compared **On-Time vs Delayed orders** across months

### 4️⃣ Payment Method Analysis

* Identified most frequently used payment methods

### 5️⃣ Product Rating Analysis

* Top 10 highest-rated products
* Bottom 10 lowest-rated products

### 6️⃣ State-wise Sales

* Identified high-performing and low-performing states

### 7️⃣ Seasonal Trends

* Quarterly revenue patterns

### 8️⃣ Yearly Revenue Trends

* Growth analysis over time

---

## 🎛️ Dashboard Features

* Interactive slicers:

  * Year
  * Category
  * Customer State
  * Payment Type
* Clean and minimal design
* Dynamic filtering and drill-down capability

---

## 🛠️ Tools & Technologies

* **Power BI**
* **Power Query**
* **DAX (Data Analysis Expressions)**
* **Excel / CSV Data Sources**

---

## 💡 Key Business Insights

* Identified revenue-driving product categories
* Detected delivery inefficiencies
* Analyzed customer satisfaction trends
* Evaluated regional performance
* Discovered seasonal sales patterns

---

## 📌 Conclusion

This project demonstrates how raw e-commerce data can be transformed into meaningful insights using **data analytics and visualization techniques**.

It highlights strong skills in:

* Data Cleaning
* Data Modeling
* DAX Calculations
* Business Intelligence & Dashboarding

---

## ⭐ If you like this project

Feel free to **star ⭐ this repository** and connect with me!

---
