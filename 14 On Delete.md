# On Delete
The DELETE statement is used to delete existing records in a table.

There are two options
1) ON DELETE SET NULL
2) DELETE ON CASCADE

See [w3schools link](https://www.w3schools.com/mysql/mysql_delete.asp)

# "ON DELETE SET NULL"
Delete or update the row from the parent table and set the foreign key column or columns in the child table to NULL.

# "DELETE ON CASCADE"
Delete or update the row from the parent table and automatically delete or update the matching rows in the child table. It automatically deletes the rows instead of setting them to null. 

See [this link]([text](https://dev.mysql.com/doc/refman/8.4/en/create-table-foreign-keys.html))

CREATE TABLE branch_supplier (
  branch_id INT,
  supplier_name VARCHAR(40),
  supply_type VARCHAR(40),
  PRIMARY KEY(branch_id, supplier_name),
  FOREIGN KEY(branch_id) REFERENCES branch(branch_id) ON DELETE CASCADE
);

Earlier code example using ON DELETE SET NULL:

CREATE TABLE branch (
  branch_id INT PRIMARY KEY,
  branch_name VARCHAR(40),
  mgr_id INT,
  mgr_start_date DATE,
  FOREIGN KEY(mgr_id) REFERENCES employee(emp_id) ON DELETE SET NULL
);

DELETE FROM employee
WHERE emp_id = 102;

SELECT * from branch;

// returns a mgr_id of NULL as a result of the "ON DELETE SET NULL" clause above.





