# What is a database?

Any collection of related information:
+ phone book
+ shopping list
+ todo list
+ your 5 best friends
+ Facebook's user base

Databases can be stored in different ways:
+ on paper
+ in your mind
+ on a computer
+ a powerpoint
+ comments section

# Computers + Datbases = <3

###### Amazon.com
* Keeps track of products, reviews, purchase orders, credit cards, users, media, etc.
* Trillions of pieces of information need to be stored and readily available.
* Information is extremely valuable and critical to Amazon.com's functioning
* Security is essential, Amazon stores people's personal information (cc number, SSN, address, phone)
* Information is stored on a computer 
**computers are great at keeping track of large amounts of information**

###### Shopping list
* Keeps track of consumer products that need to be purchased
* 10-20 pieces of information need to be stored and readily available
* Information is for convenience sake only and not necessary for shopping
* Security is not important
* Information is stoerd on a piece of paper or even in someone's memory. 

# What are Database Management Systems (DBMS)?

Special software that helps users create and maintain a database
* Makes it easy to manage laerge amounts of information
* Handles security
* Backups
* Importing/exporting data
* Concurrency
* Interacts with software applications
  * Programming languages 

Amazon.com will interact with the DBMA in order to create, read, update and delete information. 

# C.R.U.D.

Create, read, update, delete = 4 core operations a database will perform.

# Two Types of Databases

Relational Databases (SQL)

* Organize data info one or more tables
  * Each table has columns and rows
  * A unique key identifies each row
  
Non-relational (noSQL / not just SQL)

* Organize data is anything but a traditional table
  * Key-value stores
  * Documents (JSON, XML, etc)
  * Graphs
  * Flexible tables

# Relational Databases (SQL)

* Relational Database Management Systems (RDBMS)
  * Help users create and maintain a relational database (mySQL, Oracle, postgreSQL, mariaDB, etc.)

* Structured Query Language (SQL)
  * Standardized lanuage for interacting with RDBMS
  * used to perform C.R.U.D. operations, as well as other administrative tasks (user management, security, backup, etc.)
  * Used to define tables and structures
  * SQL code used on one RDBMS is not always portable to another without modification

# Non-relational Databases (noSQL / not just SQL)

Document: JSON, BLOB, XML, etc.

Graph: relational nodes

Key-Value Hash
Keys are mapped to values (strings, json, blob, etc.)

#Non-relational Databases (noSQL / not just SQL)

* Non-Relational Database Management Systems (NRDBMS) 
  * Help users create and maintain a non-relational database (mongoDB, dynamoDB, apache cassandra, firebase, etc.)

* Implementation-specific
  * Any non-relational database falls under this category, so there's no set language standard
  * Most NRDBMS will implement their own language for performing C.R.U.D. and administrative operations on the database. 

 # Database Queries
 Queries are requests made to the database management system for specific information.

 As the database's structure becomes more and more complex, it becomes more difficult to get the specific pieces of information we want. 

 A Google search is a query.

 # Wrap Up

 * A database is any collection of related information
 * Computers are great for storing databases
 * Database Management Systems (DMBS) make it easy to create, maintain, and secure a database
 * DBMS allow you to perform the C.R.U.D. operations and other administrative tasks
 * There are wo types of databases: relational and non-relational
 * Relational databases use SQL and store data in tables with rows and columns
 * Non-relational databases store data using other data structures
  
