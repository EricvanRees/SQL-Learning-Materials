# Structured Query Language (SQL)

* SQL is a language used for interacting with Relational Database Management Systems (RDBMS)
* You can use SQL to get the RDBMS to do things for you
  * Create, retrieve, update & delete data
  * Create & manage databases
  * Design & create database tables
  * Perform administration tasks (security, user management, import/export, etc)

# Structured Query Language (SQL)
* SQL implementations vary between systems
  * Not all RDBMS' follow the SQL standard to a 'T'
  * The concepts are the same but the implementation may vary

# Structured Query Language (SQL)
* SQL is a hybrid language, it's basically 4 types of languages in one
  * **Data Query Language (DQL)**
    * Used to query the database for information
    * Get information that is already stored there
  * **Data Definition Language (DDL)**
    * Used for defining database schemas
  * **Data Control Language (DCL**)
    * Used for controlling access to the data in the database
    * User & permissions management
  * **Data Manipulation Language (DML)**
    * Used for inserting, updating and deleting data from the database

# Queries

* A query is a set of instructions given to the RDBMS (written is SQL) that tell the RDBMS what information you want it to retrieve for you
  * TONS of data in a DB
  * Often hidden in a complex schema
  * Goal is to only get the data you need

Example:

  SELECT employee.name, employee.age
  FROM employee
  WHERE employee.salary > 30000

# SQL Keys

SQL offers several types of Keys, each serving a distinct purpose in the database ecosystem: 

**1) Primary Key:** It is an identifier for each record in a table. It ensures data uniqueness and serves as a reference for establishing relationships.  

**2) Unique Key:** Like a Primary Key, a Unique Key enforces uniqueness but allows null values. It's used for columns that must be unique but might contain missing information.  

**3) Foreign Key:** A Foreign Key establishes a link between two tables based on a standard column. It maintains referential integrity and enforces relationships between tables.  

**4) Composite Key:** A Composite Key uses multiple columns to create a unique identifier. It's useful when a single column cannot ensure uniqueness.  

**5) Candidate Key:** Candidate Keys are potential options for Primary Keys. They share the properties of uniqueness and minimal redundancy.  

**6) Alternate Key:** An Alternate Key is a candidate key that isn't chosen as the Primary Key. It provides additional options for uniquely identifying records.  

**7) Super Key:** It is a set of attributes that, taken together, uniquely identify records. It can include more details than necessary for a primary key. 