# Union operator
The UNION operator is used to combine the result-set of two or more SELECT statements.

Every SELECT statement within UNION must have the same number of columns
The columns must also have similar data types
The columns in every SELECT statement must also be in the same order

Link [w3schools](https://www.w3schools.com/mysql/mysql_union.asp)

-- Find a list of employee and branch names

SELECT first_name AS Company_Names
FROM employee;
UNION
SELECT branch_name
FROM branch
UNION
SELECT client_name
FROM client;

-- Find a list of all clients & branch suppliers' names

SELECT client_name, branch_id
FROM client
UNION
SELECT supplier_name, branch_id
FROM branch_supplier;

-- Find a list of all money spent or earned by the company

SELECT salary
FROM employee
UNION 
SELECT total_sales
FROM works_with;





