#CONSTRAINTS
SQL constraints are used to specify rules for data in a table. Constraints can be specified when the table is created with the CREATE TABLE statement, or after the table is created with the ALTER TABLE statement.

See: [W3Schools link](https://www.w3schools.com/mysql/mysql_constraints.asp) 

For example: using NOT NULL in table scheme definition.
This prevents entering null values into the database

For example:

  CREATE TABLE student(
    student_id INT,
    name VARCHAR(20) NOT NULL,
    major VARCHAR(20),
    PRIMARY KEY(student_id)
  );

  SELECT * FROM student;

#Populate database with values

  INSERT INTO student VALUES(1, 'Jack', 'Biology);
  INSERT INTO student VALUES(2, 'Kate', 'Sociology');
  INSERT INTO student (student_id, name)VALUES(3, 'Claire');
  INSERT INTO student VALUES(4, 'Jack', 'Biology');
  INSERT INTO student VALUES(5, 'Mike', 'Computer Science');

#Constraint #2 - Default values in table definition
For example:

  CREATE TABLE student(
    student_id INT,
    name VARCHAR(20) NOT NULL,
    major VARCHAR(20) DEFAULT 'undecided',
    PRIMARY KEY(student_id)
  );

#Constraint #3 - Auto increment

  CREATE TABLE student(
    student_id INT AUTO_INCREMENT,
    name VARCHAR(20) NOT NULL,
    major VARCHAR(20) ,
    PRIMARY KEY(student_id)
  );

  INSERT INTO student (name major) VALUES('Jack', 'Biology);
  INSERT INTO student (name major) VALUES('Kate', 'Sociology);
