CREATE DATABASE Online_Bookstore;


CREATE TABLE books(
		book_id INT PRIMARY KEY,
		title VARCHAR(200),
		author VARCHAR(200),
		genre VARCHAR(100),
		published_year INT,
		price NUMERIC(10,2),
		stock INT

);

SELECT * FROM books;


CREATE TABLE customers(
			customer_id INT PRIMARY KEY, 
			name VARCHAR(200),
			email VARCHAR(200),
			phone VARCHAR(20),
			city VARCHAR(100),
			country VARCHAR(100)

);

SELECT * FROM customers;



CREATE TABLE orders(
	order_id INT PRIMARY KEY,
	customer_id INT, 
	book_id INT,
	order_date DATE, 
	quantity INT, total_amount NUMERIC(10,2),


	FOREIGN KEY (customer_id)
	REFERENCES customers(customer_id),

	FOREIGN KEY (book_id)
	REFERENCES books(book_id)
);

SELECT * FROM orders;


COPY Books(Book_ID, Title, Author, Genre, Published_Year, Price, Stock)
FROM 'C:\SQL PROJECT\Books.csv'
DELIMITER ','
CSV HEADER;

SELECT * FROM books;

COPY customers(customer_id, name, email, phone, city, country)
FROM 'C:\SQL PROJECT\customers.csv'
DELIMITER ','
CSV HEADER;

SELECT * FROM customers;


COPY orders(order_id, customer_id, book_id, order_date, quantity, total_amount)
FROM 'C:\SQL PROJECT\orders.csv'
DELIMITER ','
CSV HEADER;

SELECT * FROM orders;



-- Basic Queries

-- 1) Retrieve all books in the "Fiction" genre

SELECT * 
FROM books
WHERE genre = 'Fiction';


-- 2) Find books published after the year 1950

SELECT * 
FROM books 
WHERE published_year > 1950;


-- 3)  List all customers from the Canada

SELECT * 
FROM customers
WHERE country = 'Canada';


-- 4) Show orders placed in November 2023

SELECT * 
FROM orders 
WHERE order_date BETWEEN '2023-11-01' AND '2023-11-30';


-- 5) Retrieve the total stock of books available

SELECT SUM(stock) AS total_stock
FROM books;

-- 6)  Find the details of the most expensive book

SELECT * 
FROM books 
ORDER BY price DESC
LIMIT 1;

-- 7) Show all customers who ordered more than 1 quantity of a book

SELECT * 
FROM orders 
WHERE quantity > 1;

-- 8) Retrieve all orders where the total amount exceeds $20

SELECT *
FROM Orders
WHERE Total_Amount > 20;

-- 9) List all genres available in the Books table

SELECT DISTINCT Genre
FROM Books;

-- 10) Find the book with the lowest stock

SELECT *
FROM Books
ORDER BY Stock ASC
LIMIT 1;

-- 11) Calculate the total revenue generated from all orders

SELECT SUM(Total_Amount) AS Revenue
FROM Orders;


-- Advance Queries

-- 12) Retrieve the total number of books sold for each genre

SELECT 
    b.Genre,
    SUM(o.Quantity) AS Total_Books_Sold
FROM Orders o
JOIN Books b
ON o.Book_ID = b.Book_ID
GROUP BY b.Genre;

-- 13) Find the average price of books in the "Fantasy" genre

SELECT AVG(Price) AS Average_Price
FROM Books
WHERE Genre = 'Fantasy';

-- 14) List customers who have placed at least 2 orders

SELECT 
    Customer_ID,
    COUNT(Order_ID) AS Total_Orders
FROM Orders
GROUP BY Customer_ID
HAVING COUNT(Order_ID) >= 2;

-- 15) Find the most frequently ordered book

SELECT 
    b.Title,
    COUNT(o.Order_ID) AS Order_Count
FROM Orders o
JOIN Books b
ON o.Book_ID = b.Book_ID
GROUP BY b.Title
ORDER BY Order_Count DESC
LIMIT 1;

-- 16) Show the top 3 most expensive books of 'Fantasy' Genre

SELECT *
FROM Books
WHERE Genre = 'Fantasy'
ORDER BY Price DESC
LIMIT 3;

-- 17) Retrieve the total quantity of books sold by each author

SELECT 
    b.Author,
    SUM(o.Quantity) AS Total_Sold
FROM Orders o
JOIN Books b
ON o.Book_ID = b.Book_ID
GROUP BY b.Author;

-- 18) List the cities where customers who spent over $30 are located

SELECT DISTINCT c.City
FROM Customers c
JOIN Orders o
ON c.Customer_ID = o.Customer_ID
WHERE o.Total_Amount > 30;


-- 19) Find the customer who spent the most on orders

SELECT 
    c.Name,
    SUM(o.Total_Amount) AS Total_Spent
FROM Customers c
JOIN Orders o
ON c.Customer_ID = o.Customer_ID
GROUP BY c.Name
ORDER BY Total_Spent DESC
LIMIT 1;

-- 20) Calculate the stock remaining after fulfilling all orders 

SELECT 
    b.Title,
    b.Stock - COALESCE(SUM(o.Quantity),0) AS Remaining_Stock
FROM Books b
LEFT JOIN Orders o
ON b.Book_ID = o.Book_ID
GROUP BY b.Title, b.Stock;
