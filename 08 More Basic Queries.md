#Link to code for creating the company database

[link](https://www.giraffeacademy.com/databases/sql/creating-company-database/)

-- Find all employees:

  SELECT *
  FROM employees;

-- Find all clients:

  SELECT * 
  FROM client;

-- Find all employees by salary

  SELECT *
  FROM employee
  ORDER BY salary DESC;

-- Find all emplyees ordered by sex then name

  SELECT *
  FROM employee
  ORDER BY sex, first_name, last_name;

-- Find the first 5 employees in the table

  SELECT *
  FROM employee
  LIMIT 5;

-- Find the first and last names of all emplyees

  SELECT first_name, last_name
  FROM employee;

-- Find the forename and surnames of all employees

  SELECT first_name AS forename, last_name AS surname
  FROM employee;

-- Find out all the different genders

  SELECT DISTINCT sex
  FROM employee;


