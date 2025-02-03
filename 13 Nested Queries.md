# Nested Queries  
Nested queries use multiple SELECT statements to get a specific kind of information.

-- Find names of all employees who have sold over 30,000 to a single client.

  SELECT employee.first_name, employee.last_name 
  FROM employee
  WHERE employee_id IN (
    SELECT works_with.emp_id
    FROM works_with
    WHERE works_with.total_sales > 30000
  );

-- Find all clients who are handles by the branch that Michael Scott manages. Assume you know Scott's ID

  SELECT client.client_name
  FROM client
  WHERE client.branch_id = (
    SELECT branch.branch_id
    FROM branch
    WHERE branch.mgr_id = 102
    LIMIT 1
  );






