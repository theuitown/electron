---
layout: post
title: 'The way around Structed Query Language (SQL)'
postimg: /assets/uploads/screenshot_20200309-214943~2.png
date: 2020-03-09T16:33:31.429Z
author: iamharsh
category: [rdbms,crash_course]
---
## What is SQL?

SQL stands for Structured Query Language and it is an ANSI standard computer language for accessing and manipulating database systems. It is used for managing data in relational database management system which stores data in the form of tables and relationship between data is also stored in the form of tables. SQL statements are used to retrieve and update data in a database.

Here we will learn the basics of SQL language.

**We are using MYSQL as SQL client.**

1.CREATE DATABASE - Creates a new database.

2.USE command: to select and open an already existing database.

3.CREATE TABLE: creates a table

4.ALTER TABLE: modifies a table.

5.DROP TABLE: deletes a table.

6.SELECT statement - To extract information from the table.

7.INSERT INTO statement - To insert new data into a table.

8.UPDATE statement - To modify data in a table.

9.DELETE - To delete data(tuples) from a table(not the column).

## DATA TYPES IN SQL

**INTEGER** : Used to store numeric values.

**CHARACTER(CHAR(SIZE))**.

**VARCHAR(X)**: Used to store STRINGS.

**DATE**: Used to store date in "yyyy/mm/dd' format.

**BOOLEAN** : Used to store values as TRUE or FALSE

**TIME**: Used to store time in hh:mm:ss format.

## Database

How you can create a database? Well thats simple

SYNTAX: 
```
CREATE DATABASE <name-of-database>;
```
Now you have to use that database.

Syntax:
```
USE <database>; 
```
Query: You want remove database.

Solution:
```DROP DATABASE <database-name>;```

## Tables

Query: Create a SQL table,

Syntax : 
```
CREATE TABLE <name-of-table>
(<COLUMN-NAME> <DATA-TYPE><SIZE>, <COLUMN-NAME> <DATA-TYPE><SIZE>);
```
Query: Insert value into table columns.

Syntax: 
```
INSERT INTO <table-name>
VALUES(<valuel>,<value2>.so on);
```
Query : Display data of table.

Syntax: ```SELECT * FROM <table>;```

## Modify

To modify data in table or to make changes, we use UPDATE statement.

Syntax for UPDATE:
```
UPDATE <table-name> SET <column>:<value> WHERE <column 2>:<value>;
```
Here, we are specifying the rows to be modified using the WHERE clause and the new data is written into the respective record using SET keyword.

## SQL Operators

While working with SELECT statement using WHERE clause, condition based query is processing is carried out.

1.Arithmetic Operators.

2.Relational Operators.

3.Logical Operators.

4.Special Operators (Condition based).

## Arithmetic Operators

**Utility**: To perform arithmetic operations like **+, -, *./.%**.

**How to:** 
```
SELECT 5 + 10; =15 
SELECT 5*4 FROM DUAL;
*DUAL is default table in MYSQL.*
SELECT Name, Marks+10 FROM student;
```
This will display Name and Marks for all Students increased by 10.

## Relational Operators

**Utility:** To perform comparison between two values.
```
= Equal to
> Greater than
< Less than
<>, != Not equal to
```
Example:
```
SELECT * FROM student WHERE Marks>80;
```
This will display the details of students whose marks are greater than 80.

## Logical Operators

**Utility:** To combine multiple conditions and display data accordingly.

List of logical operators
*AND, OR, NOT operator.*

**Examples**
```
1.SELECT * FROM students WHERE Marks > 80 and Gender='M';

To list all the details of students who scored more than 80 and are male.

2.SELECT * FROM students WHERE NOT (Stream="Science')':

To list all the details of students who are not in science stream more.
```

## SPECIAL OPERATORS

*1.Condition based on Range- BETWEEN AND*

*2.Condition based on List IN*

*3. Condition based on Pattern - LIKE*

**Examples**
```
1.SYNTAX: SELECT <column-name> FROM <table-name> WHERE <column> BETWEEN <value 1> AND <value2>

2.SYNTAX for IN: SELECT <column-name> FROM <table-name> WHERE <colum> IN (value,value2,...)

3. Pattern based : SELECT <column-name> FROM <table-name> WHERE <colum> LIKE <pattern>.
```

*a). Percent (%): Matches any string*

*b). Underscore(): Matches any one character*

## SQL JOINS

An SQL JOIN clause is used to combine rows from two or more tables, based on a common field between them.

**1.Cartesian Product:** Performed when no condition exist or are invalid, it joins all the rows in first table with of second table.
```
A={1,2} & B={3,4} = { (1,3),(1,4),(2,3),(2,4) }
```
**2.Equi Joins:** It uses equal sign as comparison operator between two tables on basis of common field.
```
SYNTAX: SELECT <column 1>,<column 2>,..
FROM <table>,<table2> WHERE <table.column]>=<table2.column2>;
```

## UNION

**Utility**:The UNION operator is used to combine the result-set of two or more SELECT statement.

*The number of columns and datatypes of selected from each table should be same*

**Example**
```
SELECT Name FROM boys WHERE Rollno < 12 UNION SELECT Name FROM girls WHERE Rollno>6;
```
This will join the column of table 1 which has Rollno smaller than 12 with the column of table 2 having Rollno greater than 6.

# SQL CHEATSHEET

**Aggregate Functions**

**COUNT:** Return the number of rows in a certain table/view

**SUM:**	Accumulate the values

**AVG:**	Returns the average for a group of values

**MIN:**	Returns the smallest value of the group

**MAX:**	Returns the largest value of the group.

**Basic Keywords**

**SELECT**: Used to state which columns to query. Use * for all

**FROM**: Declares which table/view etc to select from WHERE Introduces a condition = Used for comparing a value to a specified input

**LIKE**: Special operator used with the WHERE clause to search for a specific pattern in a column

**GROUP BY**:Arranges identical data into groups.

**HAVING**:	Specifies that only rows where aggregate values meet the specified conditions should be returned. Used because the WHERE keyword cannot be used with aggregate functions

**INNER JOIN**:	Returns all rows where key record of one table is equal to key records of another

**LEFT JOIN**:	Returns all rows from the ‘left’ (1st) table with the matching rows in the right (2nd)

**RIGHT JOIN**:	Returns all rows from the ‘right’ (2nd) table with the matching rows in the left (1st)

**FULL OUTER JOIN**: Returns rows that match either in the left or right table

## Querying data from a tables

A database table is a set of data elements (values) stored in a model of vertical columns and horizontal rows. Use any of the below to query a table in SQL:

**SELECT c1 FROM t:**	Select data in column c1 from a table named t

**SELECT * FROM t:**	Select all rows and columns from a table named t

**SELECT c1 FROM t WHERE c1 = ‘test’:** Select data in column c1 from a table named t where the value in c1 = ‘test’

**SELECT c1 FROM t ORDER BY c1 ASC (DESC):** Select data in column c1 from a table name t and order by c1, either in ascending (default) or descending order

**SELECT c1 FROM t ORDER BY c1LIMIT n OFFSET offset:** Select data in column c1 from a table named t and skip offset of rows and return the next n rows

**SELECT c1, aggregate(c2) FROM t GROUP BY c1:** Select data in column c1 from a table named t and group rows using an aggregate function

**SELECT c1, aggregate(c2) FROM t GROUP BY c1HAVING condition:** Select data in column c1 from a table named t and group rows using an aggregate function and filter these groups using ‘HAVING’ clause.

## End Note
I hope you must have got some idea about the basics of SQL and its time for exam of what you have learned so far this exam is for your practice only it totally depends on you that you give this exam or not.

[Click here for exercise](https://www.w3schools.com/sql/exercise.asp)

[Download SQL Cheatsheet PDF](https://drive.google.com/file/d/1-8j5Ko3RPZef0MjmKDGByAdb-wKtbGPK/view?usp=drivesdk)
