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
   query: CREATE TABLE table_name (
   id INT,
   name VARCHAR(255),
   city VARCHAR(255)
   );  

2) To insert data into table  
   query: INSERT INTO table_name (id, name, city) VALUES (101,'Aditya','Banganga');  
3) To select data from table  
   query: SELECT * FROM table_name;  
4) To update data in table  
   query: UPDATE table_name SET name = 'Rahul' WHERE id = 101;  
5) To delete data from table  
   query: DELETE FROM table_name WHERE id = 101; 

# Section 3: 

# Drawback  
Above operation are basic and working on one level but this is not enough for industry level database operation.  
we have to apply schema level validation also to avoid unwanted data entry.  
# Solution  
We can use PostgreSQL's built-in features such as constraints, triggers, and views to implement schema-level.  
We have to use it's built in datatypes and constraints to avoid unwanted data entry and improve  
efficiency.  

### Example  
let's take an example to entry of one row and we don't want to entry nullish data in this situation  
we can use built-constraints of postgreSQL 'NOT NULL' 

### NOTE: Before we start building schema and model for table we have to learn about datatypes and   
### constraints of PostgreSQL.
### PostgreSQL Datatypes:
### Most widely used datatypes are :
1) Numeric: INT , DOUBLE, FLOAT, DECIMAL  
2) String: VARCHAR  
3) Boolean:BOOLEAN  
4) Date: DATE  
### constraints:  
A constraints in postgreSQL is a rule applied to a column  
### Most widely used constraints are :
1. NOT NULL Constraint  
Ensures that a column cannot contain NULL values.  
2. UNIQUE Constraint  
Ensures that all values in a column are different.  
3. PRIMARY KEY Constraint  
Ensures that all values in a column are unique and not NULL.
4. FOREIGN KEY Constraint  
Establishes a relationship between two tables and ensures referential integrity by linking a column to the   primary key of another table.  
5. DEFAULT Constraint  
Assigns a default value to a column if no value is provided.   
6. SERIAL Constraint  
It can auto increment the number  

