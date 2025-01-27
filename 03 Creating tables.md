# List of all data types to be used with SQL

* INT - whole numbers
* DECIMAL(10, 4) - Decimal numbers, exact value
* VARCHAR(1) - String of text of length 1
* BLOB - Binary very large object, large data
* DATE - YYY-MM-DD
* TIMESTAMP - YY-MM-DD HH:MM:SS

# Create database
mysql> CREATE DATABASE student;

# Select database
mysql> USE student;

# Create tables + different columns and attributes

CREATE TABLE student (
  student_id INT PRIMARY KEY,
  var VARCHAR(20),
  major VARCHAR(20)
);

# Describe table
DESCRIBE student;

# Delete table
DROP TABLE student;

# Add column to table 
ALTER TABLE student ADD gpe DEcIMAL(3, 2;)

# Delete a single column
ALTER TABLE student DROP COLUMN gpa;