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
   query: SELECT \* FROM table_name;
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

1. Numeric: INT , DOUBLE, FLOAT, DECIMAL
2. String: VARCHAR
3. Boolean:BOOLEAN
4. Date: DATE

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
   Establishes a relationship between two tables and ensures referential integrity by linking a column to the primary key of another table.
5. DEFAULT Constraint  
   Assigns a default value to a column if no value is provided.
6. SERIAL Constraint  
   It can auto increment the number

## TASK 1:

Create a table called "employees" with the following columns: emp_id,fname,lname,email,department,salary  
hire_date.

### Solution:

query:    
CREATE DATABASE bank;   
CREATE TABLE employee(    
emp_id SERIAL PRIMARY KEY,  
fname VARCHAR(255) NOT NULL,    
lname VARCHAR(255) NOT NULL,   
email VARCHAR(255) UNIQUE NOT NULL,  
department VARCHAR(255) NOT NULL,    
salary DECIMAL(10,2) DEFAULT 30000.00,    
hire_date DATE DEFAULT CURRENT_DATE    
);  
#### Note insert data as your wish.  
# Section 4: 
## clause  
clause are the keyword that are used while executing query.It is use to provide condition while fetching data.  
### Most widely used clause are :
1. WHERE clause:  
It is used to filter records and return only those records that fulfill the specified condition.  
It is commonly used in SQL queries to restrict the rows returned by a SELECT, UPDATE, DELETE,  
or INSERT INTO statement based on one or more conditions.  
2. DISTINCT clause: 
It is used to return only unique (distinct) values, eliminating duplicate rows in the result set.  
It is typically used with the SELECT statement to ensure that only non-repeating data is retrieved   
from a column or set of columns.  
3. ORDER BY clause :  
It is used to sort the result set in ascending or descending order based on one or more columns.  
4. LIMIT clause: It is used to limit the number of rows returned in the result set. It is typically used   
with the SELECT statement to control how many records are displayed, often for performance optimization  
or pagination purposes.  
5. LIKE clause: It is used to search for a specified pattern in a column. It is commonly used with  
the WHERE clause to filter records that match the pattern, where % represents any sequence of characters,  
and _ represents a single character.  

## some useful operators in postgreSQL. It is also example of WHERE clause    
1. IN operator:  
It is used to specify multiple values in a WHERE or FROM clause.    
example:  
SELECT * FROM employee WHERE department IN ('IT','HR','Finance');  
2. BETWEEN operator:  
It is used to specify a range of values in a WHERE or FROM clause.  
example:  
SELECT * FROM employee WHERE salary between 40000 AND 60000;  
3. NOT operator:  
It is used to negate the result of a condition.  
example:  
SELECT * FROM employee WHERE NOT department = 'IT';  
also we can use not operator like this  
SELECT * FROM employee WHERE department NOT IN ('IT','HR','Finance');   

## DISTINCT clause :  
It is used to return only unique (distinct) values, eliminating duplicate rows in the result set.  
example: 
it is useful for fetching like country ,city,department etc.  
SELECT DISTINCT department from employee;  
## ORDER BY clause :  
It is used to sort the result set in ascending or descending order based on one or more columns.
example:  
SELECT * FROM employee id ORDER BY asc;  
## LIMIT clause : 
It is used to limit the number of rows returned in the result set.  
example:  
SELECT * FROM employee LIMIT 5;  
## LIKE clause :  
It is used to search for a specified pattern in a column.  
example: 
finding fname who contain letter i in them (anywhere)   
SELECT * FROM employee WHERE fname LIKE '%a%';   
finding fanme who contain first letter A in them  
SELECT * FROM employee WHERE fname LIKE 'A%';  
finding fname who contain last letter a in them   
SELECT * FROM employee WHERE fname LIKE '%a';  

# Section 5:  
## postgreSQL Calculation:  
1. COUNT (): It is used to count total number of column.  
2. SUM (): It is used to calculate the total of a numeric column. 
3. AVG (): It is used to calculate the average of a numeric column.  
4. MAX (): It is used to find the maximum value in a column.  
5. MIN (): It is used to find the minimum value in a column.  





