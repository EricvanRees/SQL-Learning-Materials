# Join
A JOIN clause is used to combine rows from two or more tables, based on a related column between them.

Link [w3schools](https://www.w3schools.com/mysql/mysql_join.asp)

# Supported Types of Joins in MySQL

*INNER JOIN: Returns records that have matching values in both tables
*LEFT JOIN: Returns all records from the left table, and the matched records from the right table
*RIGHT JOIN: Returns all records from the right table, and the matched records from the left table
*CROSS JOIN: Returns all records from both tables

Example of Inner Join:

INSERT INTO branch VALUES(4, 'Buffalo', NULL, NULL);

-- Find all branches and the names of their managers
SELECT employee.emp.id, employee.first_name, branch.branch_name
FROM employee
JOIN branch
ON employee.emp_id = branch.mgr_id;

