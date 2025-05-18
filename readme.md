# 📦 E-commerce SQL Task

This project demonstrates the creation of a basic **e-commerce database system** using **MySQL**. It includes essential operations such as table creation, data insertion, normalization, and running queries to analyze and manage the system efficiently.

---

## 📌 Task Overview

A simple database design for an e-commerce platform that includes:

* 🧑 **Customers**
* 📦 **Products**
* 🛒 **Orders**
* 📋 **Order Items** (normalized)

---

## ✅ Completed Tasks

* ✔️ Created a database named `ecommerce`
* ✔️ Defined and created the following tables:

  * `customers`
  * `products`
  * `orders`
  * `order_items`
* ✔️ Inserted **sample data** into each table
* ✔️ Performed a series of **SQL queries** for analysis and reporting
* ✔️ Normalized order data using an `order_items` table

---

## 🗂️ Project Structure

```
ecommerce-sql-task/
│
├── QUERIES.txt      # Full SQL code: schema creation, data insertion, queries
├── README.md        # Project documentation (this file)
```

---

## 📄 Database Schema

### 1. `customers`

Stores customer details.

| Column  | Type         |
| ------- | ------------ |
| id      | INT (PK)     |
| name    | VARCHAR(100) |
| email   | VARCHAR(100) |
| address | VARCHAR(255) |

---

### 2. `products`

Holds product listings.

| Column      | Type           |
| ----------- | -------------- |
| id          | INT (PK)       |
| name        | VARCHAR(100)   |
| price       | DECIMAL(10, 2) |
| description | TEXT           |
| discount    | DECIMAL(5, 2)  |

---

### 3. `orders`

Links customers to purchases.

| Column        | Type                    |
| ------------- | ----------------------- |
| id            | INT (PK)                |
| customer\_id  | INT (FK → customers.id) |
| order\_date   | DATE                    |
| total\_amount | DECIMAL(10, 2)          |

---

### 4. `order_items`

Normalized table to handle product quantities per order.

| Column      | Type                   |
| ----------- | ---------------------- |
| id          | INT (PK)               |
| order\_id   | INT (FK → orders.id)   |
| product\_id | INT (FK → products.id) |
| quantity    | INT                    |

---

## 🧠 Queries Executed

1. **Recent Orders**: Retrieve customers with orders in the last 30 days.
2. **Customer Spend Summary**: Total amount spent by each customer.
3. **Product Update**: Update product prices.
4. **Schema Changes**: Add a new `discount` column.
5. **Top Products**: List top 3 most expensive products.
6. **Join Queries**: Get customers who ordered a specific product.
7. **Order Summary**: Join orders and customers to display order dates.
8. **Order Filters**: Retrieve orders over a specific amount.
9. **Database Normalization**: Created and populated `order_items` table.
10. **Aggregation**: Average total amount of all orders.

> All queries with output are available in [QUERIES.txt](./QUERIES.txt)

---

## 📊 Example Output (Selected)

### Total Spend by Customers

| Name    | Total Spent |
| ------- | ----------- |
| Alice   | ₹130.00     |
| Bob     | ₹100.00     |
| Charlie | ₹160.00     |

---

### Top 3 Expensive Products

| Name      | Price   |
| --------- | ------- |
| Product D | ₹100.00 |
| Product C | ₹55.00  |
| Product B | ₹30.00  |

---

## 📈 Future Enhancements

* Add user authentication table
* Extend order tracking with statuses (pending, shipped, etc.)
* Implement triggers for inventory management
* Create stored procedures for reports

---

