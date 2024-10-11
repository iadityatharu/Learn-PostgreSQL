# What is PostgreSQL?

PostgreSQL is an open-source, advanced relational database management system (RDBMS) that supports both SQL (relational) and JSON (non-relational) querying. Known for its robustness, scalability, and standards compliance, it is often used for handling complex queries and transactions in various applications.

## Section 1

1. Creating database
   query: CREATE DATABASE test;
2. To list down all database
   query: SELECT datname from pg_database;
   or
   shortcut: \l
3. To change database
   query: \c <db_name>;

## Section 2

Table: A table is a collection of organized and related data in postgreSQL it is in row and columns format.
CRUD:
C:CREATE R:READ U:UPDATE D:DELETE

1. To create table
   query: CREATE TABLE <table name > (
   id INT,
   name VARCHAR(255),
   city VARCHAR(255)
   );

2) To insert data into table
   query: INSERT INTO <table name> (id, name, city) VALUES (101,'Aditya','Banganga');
3) To select data from table
   query: SELECT * FROM <table name>;
4) To update data in table
   query: UPDATE <table name> SET name = 'Rahul' WHERE id = 101;
5) To delete data from table
   query: DELETE FROM <table name> WHERE id = 101;
