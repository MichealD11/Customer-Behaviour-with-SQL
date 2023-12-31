# SQL Project – Unveiling Customer Insights

## Table of Contents

- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Tool Used](#tool-used)
- [Datasets](#datasets)
- [Database and Table Creation](#database-and-table-creation)
  	- [Sales Table](#sales-table)
  	- [Menu Table](#menu-table)
  	- [Members Table](#members-table)
- [Case Study Questions](#case-study-questions)

## Project Overview

This project is aimed at analyzing Dany's dinner restaurant's (a japanese cuisine) customer behaviour using MySQL. By analyzing various aspects of the data, we seek to gain a deeper understanding of the chocolate company's sales performance by using the following SQL statements;

## Problem Statement

Danny is eager to leverage the data collected within the first few months of operation to unravel key insights about his customers. He yearns to uncover the visiting patterns, discover how much they spend and their favourite menu items. Armed with this knowledge, Danny believes he can ddeliver a personalized experience that will keep his loyal customers coming back for more.

Additionally, Danny wishes to utilize these insights to make informed decisions about expanding his customer loyalty program. 

## Tool Used

- SQL

## Datasets

To help in this case study, Danny has provided us with three (3) vital datasets.

  1. Sales - This dataset holds valuable information about the transactions that takes place at Dany's diner, including the customer ID, menu items ordered, and order date.
  2. Menu - It encompasses all the delightful culinary creations offered at the restaurant wich are curry, ramen and sushi. It contains details about the item names, and theor prices.
  3. Menu - This datasets hold information about when customers joined the beta version of Danny's loyalty program

## Database and Table Creation

Writing SQL queries that will create a database and tables to hold the information Danny has shared.

```
CREATE DATABASE dannys_diner;

USE dannys_diner;
```
### Sales Table

```
customer_id VARCHAR(1),
	order_date DATE,
	product_id INTEGER
);

INSERT INTO sales
	(customer_id, order_date, product_id)
VALUES
	('A', '2021-01-01', 1),
	('A', '2021-01-01', 2),
	('A', '2021-01-07', 2),
	('A', '2021-01-10', 3),
	('A', '2021-01-11', 3),
	('A', '2021-01-11', 3),
	('B', '2021-01-01', 2),
	('B', '2021-01-02', 2),
	('B', '2021-01-04', 1),
	('B', '2021-01-11', 1),
	('B', '2021-01-16', 3),
	('B', '2021-02-01', 3),
	('C', '2021-01-01', 3),
	('C', '2021-01-01', 3),
	('C', '2021-01-07', 3);
```
### Menu Table

```
CREATE TABLE menu(
	product_id INTEGER,
	product_name VARCHAR(5),
	price INTEGER
);

INSERT INTO menu
	(product_id, product_name, price)
VALUES
  	(1, 'sushi', 10),
    (2, 'curry', 15),
    (3, 'ramen', 12);
```
### Members Table

```

CREATE TABLE members(
	customer_id VARCHAR(1),
	join_date DATE
);

INSERT INTO members
	(customer_id, join_date)
VALUES
	('A', '2021-01-07'),
    ('B', '2021-01-09');
```


## Case Study Questions

1.   What is the total amount each customer spent at the restaurant?
2.   How many days has each customer visited the restaurant?
3.   What was the first item from the menu purchased by each customer?
4.   What is the most purchased item on the menu and how many times was it purchased by all customers?
5.   Which item was the most popular for each customer?
6.   Which item was purchased first by the customer after they became a member?
7.   Which item was purchased just before the customer became a member?
8.   What is the total items and amount spent for each member before they became a member?
9.   If each $1 spent equates to 10 points and sushi has a 2x points multiplier – how many points would each customer have?
10.   In the first week after a customer joins the program (including their join date) they earn 2x points on all items, not just sushi. How many points do customer A and B have at the end of January?
11.   Recreate the table output using the available data
12.   Rank all the things


🖥️ 😄
