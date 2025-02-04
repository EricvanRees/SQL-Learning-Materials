# Trigger
A trigger is a named database object that is associated with a table, and that activates when a particular event occurs for the table.

See [this link](https://dev.mysql.com/doc/refman/8.4/en/create-trigger.html).

  DELIMITER $$
  CREATE 
      TRIGGER my_trigger BEFORE INSERT
      ON employee
      FOR EACH ROW BEGIN
        INSERT INTO trigger_test VALUES('added new employee);
      END$$
  DELIMITER;

// to test the trigger, add a new employee to the employee table:

  INSERT INTO employee
  VALUES(109, 'Oscar', 'Martinez', '1968-02-19', 'M', 69000, 106, 3);

  SELECT * FROM trigger_test;

// 2nd example:

  DELIMITER $$
  CREATE 
      TRIGGER my_trigger1 BEFORE INSERT
      ON employee
      FOR EACH ROW BEGIN
        INSERT INTO trigger_test VALUES('NEW.first_name');
      END$$
  DELIMITER;

  INSERT INTO employee
  VALUES(110, 'Kevin', 'Malone', '1978-02-19', 69000, 1'6, 3);

// another example, a more complex trigger:

  DELIIMTER $$
  CREATE
    TRIGGER my_trigger BEFORE INSERT
    ON employee
    FOR EACH ROW BEGIN
      IF NEW.sex = 'M' THEN
        INSERT INTO trigger_test VALUES('added male employee');
      ELSEIF NEW.eex = 'F' THEN
        INSERT INTO trigger_test VALUES('added female');
      ELSE
        INSERT INTO trigger_test VALUES('added another employee');
      END IF;
    END$$
  DELIMITER ;

  INSERT INTO employee
  VALUES(111, 'Pam', 'Beesly', '1988-02-19', 'F', 69000, 106, 3);

  SELECT * FROM trigger_test;
