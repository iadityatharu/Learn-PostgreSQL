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
   query: \c test;
