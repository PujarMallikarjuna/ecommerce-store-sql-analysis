# 🛒 Capstone Project - Database Design for an E-commerce Store

## 📌 Project Overview

This project focuses on designing and analyzing a relational database for a simulated e-commerce store using MySQL.

The objective is to build a structured database for customers, products, orders, order items, and payments, and then use SQL queries to answer practical business questions related to revenue, customers, products, orders, and sales performance.

This project demonstrates my ability to design relational databases and use SQL for business-oriented data analysis.

---

## 🎯 Project Objectives

- Design a normalized relational database for an e-commerce business
- Create relationships between multiple tables using primary and foreign keys
- Insert and manage sample transactional data
- Use SQL joins to combine data from multiple tables
- Perform revenue and sales analysis
- Identify top customers and best-selling products
- Analyze order status and payment methods
- Analyze revenue by city, product category, and order date
- Generate meaningful business insights using SQL

---

## 🗂️ Database Schema

The database consists of five main tables:

### 1. Customers
Stores customer information.

**Columns:**
- `customer_id` - Primary Key
- `name` - Customer name
- `email` - Customer email
- `city` - Customer city
- `signup_date` - Registration date

### 2. Products
Stores information about products available in the store.

**Columns:**
- `product_id` - Primary Key
- `product_name` - Product name
- `category` - Product category
- `price` - Product price
- `stock` - Available inventory

### 3. Orders
Stores customer order information.

**Columns:**
- `order_id` - Primary Key
- `customer_id` - Foreign Key
- `order_date` - Date of order
- `order_status` - Order status

### 4. Order Items
Stores products included in each order.

**Columns:**
- `order_item_id` - Primary Key
- `order_id` - Foreign Key
- `product_id` - Foreign Key
- `quantity` - Quantity purchased

### 5. Payments
Stores payment information for orders.

**Columns:**
- `payment_id` - Primary Key
- `order_id` - Foreign Key
- `payment_mode` - Payment method
- `amount` - Payment amount
- `payment_date` - Payment date

---

## 🔗 Database Relationships

```text
Customers
    │
    │ 1
    │
    └──────────< Orders
                    │
                    │ 1
                    │
                    ├──────────< Order Items >────────── Products
                    │
                    │ 1
                    │
                    └────────── Payments
