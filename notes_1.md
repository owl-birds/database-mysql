# SQL (Structured Query Language)

SQL is language that has been used to communicate to a RELATIONAL DATABASES SYSTEM.

the meaning of communicate here is to like manage, read, view, create and anything else taht related to the data that u want to store in the database.

### SQL can be categorized into two parts

## Data Definition Language (DDL)

is a language that is used to manipulate database structure,
there are a few instructions that are included in this category, for example creating (CREATE), changing (ALTER) and removing/deleting (DROP) data storage structure, database, table, column and data type.
DDL can be used to determine constraints that applied to table, for example Primary Key and Foreign Key.

## Data Manipulation Language (DML)

is a language that contain instructions to process data inside a database.
for example: to get data (SELECT), inserting data (INSERT), updating data (UPDATE) and removing data (DELETE)

# RELATIONAL DATABASE MANAGEMENT SYSTEM (RDBMS)

is a program that allow u to store and manage data
the data is structured in tables (column and row) that has relation to each other. and in other to work with relational database u will need SQL to manage it.

## Relational databases have structure hierarchy that look like below

1. Database
2. Table
3. Column or field

;;; database -> Table -> Column/Field (top to bottom)

### SELECT

'''
SELECT column_name1, column_name2, ...
FROM table_name
WHERE condition1, condition2, ... ;
'''

if u want to gett all the data in each column u can use \* (star) or its usually called wildcard
a symbol to select all column in the table

'''SELECT \* FROM ... WHERE ... ;'''

### LIMIT

if u want to limit the data that u want to get or u only want a specific number of data that u want to get from the database u can use DML LIMIT

sintax;;;
'''
SELECT ... FROM ... WHERE ... LIMIT n;
SELECT ... FROM ... LIMIT n;
'''

### SELECT DISTINCT

if u want to get unique data without its duplicate u can use SELECT DISTINCT to only get unique datas.

the use case is for example if u want to get only the unique visitors of ur website

syntax;;;
'''
SELECT DISTINCT ... FROM ... ;
'''

## PREFIXS and ALIASES

usually prefixs is used if u want to get data from more than one tables, because if it only one table its obvious where the column/field cames from.

aliases is used to change the column/field name when u get ur data based on ur needs

'''
SELECT t1.column_name1 AS "FIRST COLUMN NAME", t1.column_name2 AS second_column_name FROM table_name as t1;
'''
'''
SELECT table_name.column_name FROM table_name;
'''
u can even remove AS on ur SQL sintax
'''
SELECT column_field_name new_column_field_name FROM table_name;
'''

## WHERE

WHERE instruction is used to

- filter data based on texts
- filter data based on the condition of numbers
- filter data with more than one condition is using AND and OR operator

'''
SELECT column_name FROM table_name WHERE condition;

#### Filtering with text

SELECT \* FROM staff WHERE sex = "female";
SELECT ... FROM staff WHERE column_field_name = 'value';
SELECT ... FROM staff WHERE column_field_name1 = 'value1' AND column_field_name2 = 'value2' OR ...;

#### Filtering with number

> < =

SELECT ... FROM staff WHERE num_column_field_name < 'value';

SELECT ... FROM staff WHERE condition1 AND condition2 OR ...;
'''
