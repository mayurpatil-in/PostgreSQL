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








