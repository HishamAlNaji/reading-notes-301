# Reading 14a Database Normalization

## What is Database Normalization?

- Database Normalization is the process of organizing data in a database. This includes creating tables and establishing relationships between those tables according to rules designed both to protect the data and to make the database more flexible by eliminating redundancy and inconsistent dependency.

## What is the importance of Database Normalization?

-  Eliminate the flaws of a database with bad design. A poorly designed database is inconsistent and create issues while adding, deleting or updating information

## Stages of Database Normalization:

* First Normal Form (1NF):
- Data is stored in tables with rows uniquely identified by a primary key
- Data within each table is stored in individual columns in its most reduced form
- There are no repeating groups
* Second Normal Form (2NF):
- Everything from 1NF
- Only data that relates to a table’s primary key is stored in each table
*Third Normal Form (3NF):
- Everything from 2NF
- There are no in-table dependencies between the columns in each table
- Note that there are actually six levels of normalization; however, the third normal form is considered the highest level necessary for most applications. 

## Resource link:

https://www.essentialsql.com/get-ready-to-learn-sql-database-normalization-explained-in-simple-english/



