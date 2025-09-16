# PostgreSQL
This repository demonstrates the use of PostgreSQL for modern application development. It includes database schema design, optimized queries, and integration examples with different backends (FastAPI, Flask, Django, Node.js).

## PostgreSQL Commands
Here are some commonly used Conda commands.
## 1. Basic Commands
- ### All Clear
```bash
\! cls
\! clear
```
- ### All Database List:
```bash
\l
\list
\SELECT datname FROM pg_database;
```
- ### Create new database:
```bash
CREATE DATABASE test;
```
- ### Change database:
```bash
\c test;
```
- ### Delete database:
```bash
DROP DATABASE test;
```
---
## 2. CRUD Commands
- ### Create Table:
```bash
CREATE TABLE person (id INT, name VARCHAR(50), city VARCHAR(50));
```
- ### Show All Table List:
```bash
\dt
```
- ### Show under table details:
```bash
\d person
```
- ### Insert data in table:
```bash
INSERT INTO person(id, name, city)
VALUES (101, 'Mayur', 'Kolhapur'), (102, 'Raju', 'Mumbai');
```
- ### View/Read data:
```bash
SELECT * FROM person;
```
- ### Update data:
```bash
UPDATE person SET city= 'Sangali' WHERE id=103;
```
- ### Delete data from a Table:
```bash
DELETE FROM person WHERE id= 103;
```
---
## 3. Constraints
- ### Primary Key, Not null & Default:
```bash
CREATE TABLE person
    ( id INT PRIMARY KEY,
      name VARCHAR(50) NOT NULL,
      city VARCHAR(50) NOT NULL DEFAULT 'India');
```
- ### Autoincrement -> SERIAL :
```bash
CREATE TABLE person
    ( id SERIAL PRIMARY KEY,
      name VARCHAR(50) NOT NULL,
      city VARCHAR(50) NOT NULL DEFAULT 'India');
```
- ### If primary key then enter values already their then set values:
```bash
select setval('employees_emp_id_seq', 1)
select currval('employees_emp_id_seq')
```
---
## 4. Clauses
- ### Where -> Fetch Specific data:
```bash
SELECT * FROM employees WHERE emp_id=5;
```
- ### Autoincrement -> SERIAL :
```bash
CREATE TABLE person
    ( id SERIAL PRIMARY KEY,
      name VARCHAR(50) NOT NULL,
      city VARCHAR(50) NOT NULL DEFAULT 'India');
```
- ### If primary key then enter values already their then set values:
```bash
select setval('employees_emp_id_seq', 1)
select currval('employees_emp_id_seq')
```
- ### AND, OR Operator:
```bash
SELECT * FROM employees WHERE dept='IT' AND dept='FIN';
SELECT * FROM employees WHERE dept='IT' OR dept='FIN';
```
- ### IN Operator:
```bash
SELECT * FROM employees WHERE dept IN('IT','FIN','HR');
```
- ### BETWEEN Operator:
```bash
SELECT * FROM employees WHERE salary BETWEEN 40000 AND 65000;
```
- ### DISTINCT -> Findout unique value:
```bash
SELECT DISTINCT dept FROM employees;
```
- ### ORDER BY -> Sorting:
```bash
SELECT * FROM employees ORDER BY fname;
SELECT * FROM employees ORDER BY fname DESC;
```
- ### LIMIT -> Number of record show:
```bash
SELECT * FROM employees LIMIT 3;
```
- ### LIKE -> Shows record by perticular character name
- Starts with 'A': LIKE 'A%'
- Ends with 'A': LIKE '%A'
- Contains 'A': LIKE '%A%'
- Second character is 'A': LIKE '_A%'
- Case-insensitive contains 'john': ILIKE '%john%':
```bash
SELECT * FROM employees WHERE fname LIKE '%a';
```
---
## 5. Aggregate Functions
- ### COUNT:
```bash
SELECT COUNT(emp_id) from employees;
```
- ### SUM :
```bash
SELECT SUM(salary) from employees;
```
- ### AVG :
```bash
SELECT AVG(salary) from employees;
```
- ### MIN :
```bash
SELECT MIN(salary) from employees;
```
- ### MAX :
```bash
SELECT MAX(salary) from employees;
```
---
## 6. Group By
- ### Group By:
```bash
SELECT dept, COUNT(emp_id) from employees GROUP BY dept;
SELECT dept, SUM(salary) from employees GROUP BY dept;
```
---
## 7. String Functions
- ### CONCAT, CONCAT_WS:
```bash
SELECT emp_id, CONCAT(fname,lname) As Fullname, dept FROM employees;
SELECT emp_id, CONCAT_WS(' ', fname, lname) AS Fullname, dept FROM employees;
```
- ### SUBSTR:
```bash
SELECT SUBSTR('Hello Buddy!', 1,5);
SELECT SUBSTR(fname, 1,3) FROM employees;
```
- ### REPLACE:
```bash
SELECT REPLACE(dept, 'IT', 'TECH') from employees;
```
- ### REVERSE:
```bash
SELECT REVERSE(fname) from employees;
```
- ### LENGTH:
```bash
SELECT LENGTH(dept) FROM employees;
SELECT * FROM employees WHERE LENGTH(fname) > 5;
```
- ### UPPER:
```bash
SELECT UPPER(fname) FROM employees;
```
- ### LENGTH:
```bash
SELECT LOWER(fname) FROM employees;
```
- ### LEFT:
```bash
SELECT LEFT('Hello World', 4);  -> Hell
```
- ### RIGHT:
```bash
SELECT RIGHT('Hello World', 4);  -> orld
```
- ### TRIM:
```bash
SELECT LENGHT(TRIM('   Hello World   '));  -> Avoid Spaces
```
- ### POSITION:
```bash
SELECT POSITION('om' in 'Thomas');  -> Check position- here 3
```
---
## 7. Alter Table
- ### ADD:
```bash
ALTER TABLE person ADD COLUMN age INT;
```
- ### DROP:
```bash
ALTER TABLE person DROP COLUMN age;
```
- ### RENAME:
```bash
ALTER TABLE person RENAME COLUMN name TO fname;
```
- ### Modified Table:
```bash
ALTER TABLE person
ALTER COLUMN fname
SET DATA TYPE VARCHAR(150);  -> Chaange fname column datatpye value VARCHAR(100) TO VARCHAR(150)
```
- ### CASE:
```bash
SELECT fname, salary,
CASE
    WHEN salary >=50000 THEN 'High'
    ELSE 'Low'
END AS Sal_cal
FROM employees;
```
---








