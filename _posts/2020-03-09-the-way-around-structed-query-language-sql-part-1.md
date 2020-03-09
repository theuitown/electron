---
layout: post
title: 'The way around Structed Query Language (SQL) : Part 1'
postimg: /assets/uploads/screenshot_20200309-214943~2.png
date: 2020-03-09T16:33:31.429Z
author: iamharsh
---
SQL(Structured Query Language) is a standard language for accessing and manipulating databases.

Here we will learn the basics of SQL language.

**We are using MYSQL as SQL client.**

• CREATE DATABASE - Creates a new database.

• USE command: to select and open an already existing database.

. CREATE TABLE: creates a table

• ALTER TABLE: modifies a table.

• DROP TABLE: deletes a table.

SELECT statement - To extract information from the table.

• INSERT INTO statement - To insert new data into a table.

• UPDATE statement - To modify data in a table.

DELETE - To delete data(tuples) from a table(not the column).

## DATA TYPES IN SQL

 INTEGER : Used to store numeric values.

• CHARACTER(CHAR(SIZE))

 • VARCHAR(X): Used to store STRINGS.

 • DATE: Used to store date in "yyyy/mm/dd' format.

• BOOLEAN : Used to store values as TRUE or FALSE

• TIME:Used to store time in hh:mm:ss format.

## Database

How you can create a database? Well thats simple

SYNTAX: 
CREATE DATABASE <name-of-database>;

Now you have to use that database.
syntax:USE <database>; 

Query: You want remove database.

Solution:DROP DATABASE <database-name>;

## Tables

Query: Create a SQL table,

Syntax : 
CREATE TABLE <name-of-table>
(<COLUMN-NAME> <DATA-TYPE><SIZE>, <COLUMN-NAME> <DATA-TYPE><SIZE>);

Query: Insert value into table columns.

Syntax: INSERT INTO <table-name>
VALUES(<valuel>,<value2>.so on);

Query : Display data of table 
Syntax: SELECT * FROM <table>;

## Modify

To modify data in table or to make changes, we use UPDATE statement.

Syntax for UPDATE:

UPDATE <table-name> SET <column>:<value> WHERE <column 2>:<value>;

Here, we are specifying the rows to be modified using the WHERE clause and the new data is written into the respective record using SET keyword.