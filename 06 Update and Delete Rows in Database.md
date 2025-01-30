#Update Database Entries

see: https://www.w3schools.com/mysql/mysql_update.asp 

SELECT * FROM student;

UPDATE student
SET major = 'Bio'
WHERE major = 'Biology';

or

UPDATE student
SET major = 'Comp Sci'
WHERE student_id = 4;

using more conditions:

UPDATE student
SET major = 'Biochemistry'
WHERE major = 'Bio' OR major = 'Chemistry';

or

UPDATE student
SET name = 'Tom', major = 'undecided'
WHERE student_id = 1;

update ALL rows at once:

UPDATE student
SET major = 'undecided';

#Delete a specific row or series of rows

delete all rows at omnce:

DELETE FROM student;

using conditions:

DELETE FROM student
WHERE student_id = 5;

or

DELETE FROM student
WHERE name = 'Tom' AND major =  'undecided';

see: https://www.w3schools.com/mysql/mysql_delete.asp