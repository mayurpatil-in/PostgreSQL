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

