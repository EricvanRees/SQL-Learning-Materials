# MySQL COUNT(), AVG() and SUM() Functions

The COUNT() function returns the number of rows that matches a specified criterion.

The AVG() function returns the average value of a numeric column. 

The SUM() function returns the total sum of a numeric column. 

See [this w3schools link](https://www.w3schools.com/mysql/mysql_count_avg_sum.asp). 

-- Find the number of employees

  SELECT COUNT(emp_id)
  FROM employee;

-- Find the number of female employees born after 1970

  SELECT COUNT(emp_id)
  FROM employee
  WHERE sex = "F" and birth_date > '1971-01-01';

-- Find the average of all employee's salaries

  SELECT AVG(salary)
  FROM employee
  WHERE sex = 'M';

-- Find the sum of all employee's salaries

  SELECT SUM(salary)
  FROM employee;

-- Find out how many males and females there are

  SELECT COUNT(sex), sex
  FROM employee
  GROUP BY sex;

-- Find the total sales of each salesman

  SELECT SUM(total_sales), emp_id
  FROM works_with
  GROUP BY emp_id;

-- How much does each client spend?

  SELECT SUM(total_sales), client_id
  FROM works_with
  GROUP BY client_id;

