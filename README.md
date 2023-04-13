# SQL - Learning and Practice

This repository contains notes and queries with SQL. The purpose of this repository is to learn and practice PostgreSQL.

<!-- Table of contents -->
## Table of Contents



- [Cheat Sheet](#cheat-sheet)
- [SQL Statement Fundamentals](#sql-statement-fundamentals)
    - [SELECT](#select)
    - [COUNT](#count)
    - [SELECT WHERE](#select-where)
    - [ORDER BY](#order-by)
    - [LIMIT](#limit)
    - [BETWEEN](#between)
    - [IN](#in)
    - [LIKE AND ILIKE](#like-and-ilike)
- [GROUP BY - Statements](#group-by---statements)
- [JOINS](#joins)
- [Advanced SQL Commands](#advanced-sql-commands)
- [Creating Databases & Tables](#creating-databases--tables)
- [Conditional Expressions and Procedures](#conditional-expressions-and-procedures)





## Cheat Sheet

![SQL Cheat Sheet](images/cheat_sheet.png)

## SQL Statement Fundamentals

### SELECT

```sql
-- Select a column from table
SELECT column_name FROM table_name;

-- Select more columns from table
SELECT column_name1, column_name1 FROM table_name;

-- Select all columns from table
SELECT * FROM table_name;

```



### COUNT

```sql
-- Count rows in column
SELECT COUNT(column_name/choice/*) FROM table_name;

-- Count distinct
SELECT COUNT(DISTINCT column_name) FROM talbe_name;
```

### SELECT WHERE

```sql
SELECT column1, column2
FROM table_name
WHERE conditions;
```

| Operator | Description |
| --- | --- |
| = | Equal |
| > | Greater than |
| < | Less than |
| >= | Greater than or equal to |
| <= | Less than or equal to |
| <> or != | Not equal to |

**Logical Operations:**
- AND
- OR
- NOT

```sql
-- Example SELECT WHERE
SELECT title FROM film
WHERE rental_rate > 4 AND replacement_cost >= 19.99
AND rating = 'R';
```

### ORDER BY

```sql
-- Order by a column Ascending or Descending
SELECT column_1, column_2
FROM table_name
ORDER BY column_1 ASC/DESC;

-- More than one orderings
SELECT column_1, column_2
FROM table_name
ORDER BY column_1 DESC, column_2 ASC;
```

### LIMIT

```sql
-- LIMIT Statement limits the number of rows shown by the query - like top5
SELECT column_1, column_2
FROM table_name
ORDER BY column_1 ASC/DESC 
LIMIT 5;
```

### BETWEEN

```sql
-- Using Between for numerical values 
SELECT *
FROM table_name
WHERE amount BETWEEN 8 AND 9;

-- Using the between with NOT logical statement
SELECT *
FROM table_name
WHERE amount NOT BETWEEN 8 AND 9;

-- Using Between for data values
SELECT *
FROM table_name
WHERE amount BETWEEN '2010-02-1' AND '2010-02-15';
```

### IN

```sql
-- Example of NOT IN sting values
SELECT color_name
FROM table_name
WHERE color_name IN ('red','blue') 

-- Example of IN numerical values
SELECT COUNT(*)
FROM table_name
WHERE amount IN (0.99,1.98,1.99)
```

### LIKE AND ILIKE

```sql
-- First letter example with LIKE - ! Is case sensitive
SELECT COUNT(*)
FROM customer
WHERE first_name LIKE 'J%' AND last_name LIKE 'S%'

-- ILIKE - is case insensitive - doesn't matter if you are using captital letter
SELECT COUNT(*)
FROM customer
WHERE first_name ILIKE 'j%' AND last_name ILIKE 's%'

-- Other example
SELECT COUNT(*)
FROM customer
WHERE first_name ILIKE 'er%'
```

## GROUP BY - Statements

## JOINS

## Advanced SQL Commands

## Creating Databases & Tables

## Conditional Expressions and Procedures
