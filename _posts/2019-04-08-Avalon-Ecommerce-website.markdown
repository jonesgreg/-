---
layout:     post
title:      Avalon E-Commerce Website
date:       2019-04-08 19:51:19
summary:    Database management Systems (DBMS351)
categories: web dev
---
## Abstract

The past recent years, the Internet has increasingly become the best channels for collecting information and gradually into the traditional circulation, so e-commerce began to pop up and has become a popular topic. The online shopping has become a more accessible way of shopping. Users can quickly find their favorite goods, making shopping more affordable, faster, and convenient. Online store has achieved great success. For example, we are  familiar with Amazon.

**PHP and MySQL** combination has become useful in most businesses. PHP and MySQL combination has become the ideal solution for building an online shopping system.


My group and I decided to develop our e-commerce website as our project for our Database management systems class. We decided to call the site Avalon because one of the group member's Mom used to own a clothing store in Avalon, New Jersey before it was shut down due to a destructive storm.

---------------------------------------------------------------------------------------------------------------------------------------------------
### Development Process
<img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/developmentprocess.png" height="250">


This project was my first experience in actually going through an entire development cycle, which included constructing the layouts for the website.



&nbsp;<center><strong>Phase 1: Constructing the Layout</strong></center>

To start, I worked on developing the business rules for the relational database. My goal was to discuss the structure and components of a database for a real-world e-commerce system.


&nbsp;<center><strong>Problem</strong></center>

<center>What are we going to sell for the consumer?</center>


&nbsp;<center><strong>Solution</strong></center>

<center>We went for selling men and women t-shirts. We then discuss relevant components of a typical e-commerce database system for the admin user.
Finally, we illustrate the layout and detailed design of an e-commerce website that correlates with the database system.</center>


&nbsp;<center><strong>Business Rules</strong></center>
<center> - A user can have zero or many orders</center>
<center> - Orders are assigned to only one user</center>
<center> - A User can only be assigned to a cart</center>
<center> - A user can remove one or more products from the cart</center>
<center> - A cart can only be assigned to one user</center>
<center> - An order can be assigned to only one product</center>
<center> - A product can have zero or many orders</center>
<center> - A quantity size can be assigned to only one product</center>
<center> -  A product can have one or many quantity sizes</center>
<center> -  A category can have one or many products listed</center>
<center> -  A product can only one be assigned to one category.</center>


### ERD Diagram & UML Diagram
<p align="center">
<img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/UML.png" height="500"/>&nbsp;
</p>

&nbsp;<img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/ERD-Diagram.png" height="500" width="1500"/>


&nbsp;<center><strong>Phase 2: Building User Interface & Database Connectivity</strong></center>

The next step, we decided to use bootstrap framework as our front-end interface. We followed the **CRUD (Create, Read, Update, and Delete) operation**. I worked on the **Read** operation, which is viewing the products for the end-user to purchase and check out an product.

&nbsp;<center><strong>Fetching data from the database</strong></center>

<p align="center">
<img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/fetch-data.png" height="250" weight="300"/>&nbsp;
</p>

I fetched data from **MySQL tables** by executing a SQL SELECT statement through PHP function called **mysql_query**.  I used a while loop to bring the results from the table using **$result -> fetch_assoc())**. This PHP function returns the row as an associative array. The content of the rows are assigned to the variable **$row**, and the values in rows are the printed.

&nbsp;<center><strong>Phase 3: Incorporating Triggers and Procedures</strong></center>

&nbsp;<center><strong>Triggers</strong></center>

My group and I decided to include triggers and procedures in our database. Triggers execute to specific events in our table. It helps maintain the integrity of the information on the database. If we decided to make a change in a table, the move would occur throughout the database. For instance, lets say the admin wants to delete a product because it is out of stock, so let's create a trigger before we delete the product in the product table. First, we must remove the **old product id** from the table for the product to be deleted. Another instance, is if we want to update a product, we must set the **new product attributes** to the **old product attributes**.

<p align="center">
<img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/triggers.png" height="350"/>&nbsp;
</p>

When using SQL programs there is two methods which are available for storing and executing programs. You can **store the programs locally** and **create applications** that send the commands to SQL Server and process them, or you can **save the programs as stored procedures** in SQL Server and create applications that execute the stored procedures and process the results. You can create a stored procedure once, store it in the database, and call it any number of times in a program.

&nbsp;<center><strong>Stored Procedures</strong></center>

The **GetAllProducts()** stored procedures select all products from the products table. We use the **CREATE PROCEDURE statement** to create a new stored procedure. We specify the name of the stored procedure after the **CREATE PROCEDURE statement**. In this case, the name of the stored procedure is **GetAllProducts**. We put the parentheses after the name of the stored procedure.

<p align="center">
<img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/StoredProcedures.png" height="200"/>&nbsp;
</p>

### Prototypes

&nbsp;<center><strong>Outline of the website</strong></center>
<p align="center">
<img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/pro1.png" height="400"/>&nbsp;
</p>

<p align="center">
<img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/pro2.png" height="400"/>&nbsp;
</p>

&nbsp;<center><strong>Final Design</strong></center>
<p align="center">

<img src="https://raw.githubusercontent.com/jonesgreg/gregoryjones/gh-pages/images/pro3.png" height="400"/>&nbsp;
</p>

&nbsp;<center><strong>UI Demo</strong></center>
<iframe src="https://player.vimeo.com/video/339638159" width="900" height="400" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>
## Credits
- _Gregory Jones, <mrjonesgregory@gmail.com>_
- _Danni Jin, <dj6702098@sju.edu>_
- _Megha Ukkali, <mu721466@sju.edu>_
