# 📚 Online Bookstore SQL Project

## 📌 Project Overview

This project is a complete SQL-based data analysis project built using an **Online Bookstore Dataset**. The project demonstrates SQL skills required for a **Data Analyst** role, including:

* Database creation
* Table relationships
* Data importing
* Data analysis using SQL queries
* Business problem solving
* Revenue and sales analysis
* Customer behavior analysis

The project uses three datasets:

* Books
* Customers
* Orders

---

# 🛠️ Tools & Technologies Used

* SQL
* PostgreSQL
* CSV Files
* GitHub

---

# 📂 Dataset Files

| File Name                             | Description                                                          |
| ------------------------------------- | -------------------------------------------------------------------- |
| Books.csv                             | Contains book details such as title, author, genre, price, and stock |
| Customers.csv                         | Contains customer information                                        |
| Orders.csv                            | Contains order transaction details                                   |
| online_bookstore_complete_project.sql | Complete SQL project file                                            |

---

# 🗂️ Database Schema

## 📘 Books Table

| Column Name    | Description      |
| -------------- | ---------------- |
| Book_ID        | Unique book ID   |
| Title          | Book title       |
| Author         | Author name      |
| Genre          | Book genre       |
| Published_Year | Publication year |
| Price          | Book price       |
| Stock          | Available stock  |

---

## 👤 Customers Table

| Column Name | Description        |
| ----------- | ------------------ |
| Customer_ID | Unique customer ID |
| Name        | Customer name      |
| Email       | Customer email     |
| City        | Customer city      |
| Country     | Customer country   |

---

## 🛒 Orders Table

| Column Name  | Description             |
| ------------ | ----------------------- |
| Order_ID     | Unique order ID         |
| Customer_ID  | Customer reference      |
| Book_ID      | Book reference          |
| Order_Date   | Order date              |
| Quantity     | Number of books ordered |
| Total_Amount | Total order value       |

---

# 🔗 Entity Relationship

* `Books.Book_ID` → `Orders.Book_ID`
* `Customers.Customer_ID` → `Orders.Customer_ID`

---

# 📊 SQL Concepts Used

This project covers:

* SELECT Statements
* WHERE Clause
* ORDER BY
* GROUP BY
* HAVING Clause
* Aggregate Functions
* INNER JOIN
* Subqueries
* Aliases
* Sorting
* Filtering
* Revenue Analysis
* Customer Analysis

---

# 📈 Business Problems Solved

## ✅ Basic SQL Queries

1. Retrieve all books in the Fiction genre
2. Find books published after 1950
3. List all customers from Canada
4. Show orders placed in November 2023
5. Retrieve total stock available
6. Find the most expensive book
7. Show customers who ordered more than 1 quantity
8. Retrieve orders where total amount exceeds $20
9. List all available genres
10. Find the book with the lowest stock
11. Calculate total revenue generated

---

## 🚀 Advanced SQL Queries

1. Total books sold for each genre
2. Average price of Fantasy books
3. Customers who placed at least 2 orders
4. Most frequently ordered book
5. Top 3 most expensive Fantasy books
6. Total quantity sold by each author
7. Cities where customers spent over $30
8. Customer who spent the most
9. Remaining stock after fulfilling orders

---

# 📌 Key Insights

* Identified highest revenue-generating books
* Analyzed customer purchasing behavior
* Found most popular genres and authors
* Calculated total sales revenue
* Tracked inventory and remaining stock
* Identified top-spending customers

---

# ▶️ How to Run This Project

## Step 1: Create Database

```sql
CREATE DATABASE online_bookstore;
```

## Step 2: Import CSV Files

Import:

* Books.csv
* Customers.csv
* Orders.csv

into your SQL database.

## Step 3: Run SQL Script

Execute:

```sql
online_bookstore_complete_project.sql
```
---

# 🎯 Skills Demonstrated

* SQL Data Analysis
* Database Management
* Data Cleaning
* Relational Database Design
* Business Analysis
* Query Optimization
* Analytical Thinking

---

# 💼 Why This Project?

This project was created to practice real-world SQL concepts used in Data Analyst roles. It demonstrates the ability to:

* Work with relational databases
* Analyze business data
* Write efficient SQL queries
* Generate insights from structured data

---

# 👨‍💻 Author

## DIGAMBAR SHINDE




# 📬 Connect With Me

You can add your:

* GitHub Profile
* https://github.com/DigamabrShinde1342/Online_Bookstore_SQL_Project


