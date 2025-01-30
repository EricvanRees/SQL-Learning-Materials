# Basic Queries using "Select"

See: [W3Schools link](https://www.w3schools.com/mysql/mysql_select.asp) 

  "SELECT *" means select all columns from database

select only one or two columns:

  SELECT student.name, student.major
  FROM student
  ORDER BY name;

* orders the student names alphabetically
* prepending the table name is optionally but can come in handy with more complex queries

  SELECT *
  FROM student
  ORDER BY major, student_id;

* orders data using two column names

  SELECT *
  FROM student
  ORDER BY major, student_id DESC;

* orders data in descending order

  SELECT *
  FROM student
  LIMIT 2;

* Limit the results to 2

Combine different examples:

  SELECT *
  FROM student
  ORDER BY student_id DESC
  LIMIT 2;

# Filter results using "WHERE"

See: [W3Schools link](https://www.w3schools.com/mysql/mysql_where.asp)

  SELECT *
  FROM name, major
  WHERE major = 'Chemistry';

second example:

  SELECT name, major
  FROM student
  WHERE major = 'Chemistry' OR name = 'Kate';

Use more complex examples using comparison operators: 
<, >, <=, >=, =, <>, AND, OR

Example:

  SELECT name, major
  FROM student
  WHERE major <> 'Chemistry';

= "select all all names and major where major is not equal to Chemistry"

  SELECT * 
  FROM student
  WHERE student_id < 3;

= only returns rows for students 1 and 2

or:

  SELECT *
  FROM student
  WHERE student_id <= 3 AND name <> 'Jack';

# "In" Operator

See [W3Schools link](https://www.w3schools.com/mysql/mysql_in.asp)

  SELECT * 
  FROM student
  WHERE name IN ('Claire', 'Kate', 'Mike');

or 

  SELECT * 
  FROM student
  WHERE major IN ('Biology', 'Chemistry') AND student_id > 2;

