# SQL Joining Tables Tutorial

This tutorial is designed to help you understand how to join tables in SQL to retrieve data from multiple related tables. Joining tables is a fundamental aspect of SQL querying and is crucial for performing complex data retrieval operations.

## Prerequisites
- Basic understanding of SQL syntax
- Familiarity with creating and managing databases
- Knowledge of primary and foreign keys

## Table of Contents
1. [Introduction to SQL Joins](#introduction-to-sql-joins)
2. [Types of Joins](#types-of-joins)
    - Inner Join
    - Left Join
    - Right Join
    - Full Outer Join
3. [Joining Tables Syntax](#joining-tables-syntax)
4. [Examples](#examples)
5. [Conclusion](#conclusion)
6. [Additional Resources](#additional-resources)

## Introduction to SQL Joins

In SQL, a join is used to combine rows from two or more tables based on a related column between them. This allows us to retrieve data that spans multiple tables and create meaningful relationships between them.

## Types of Joins

### Inner Join
An inner join returns only the rows that have matching values in both tables. It selects records that have matching values in both tables' columns.

### Left Join
A left join returns all the rows from the left table and matching rows from the right table. If there is no match, the result is NULL on the right side.

### Right Join
A right join returns all the rows from the right table and matching rows from the left table. If there is no match, the result is NULL on the left side.

### Full Outer Join
A full outer join returns all rows from both tables, matching them where possible and filling in NULLs for missing matches.

## Joining Tables Syntax

The general syntax for joining tables in SQL is as follows:

```sql
SELECT columns
FROM table1
JOIN table2 ON table1.column = table2.column;
```

## Examples

### Inner Join Example

```sql
SELECT Orders.OrderID, Customers.CustomerName
FROM Orders
INNER JOIN Customers ON Orders.CustomerID = Customers.CustomerID;
```

### Left Join Example

```sql
SELECT Orders.OrderID, Customers.CustomerName
FROM Orders
LEFT JOIN Customers ON Orders.CustomerID = Customers.CustomerID;
```

### Right Join Example

```sql
SELECT Orders.OrderID, Customers.CustomerName
FROM Orders
RIGHT JOIN Customers ON Orders.CustomerID = Customers.CustomerID;
```

### Full Outer Join Example

```sql
SELECT Orders.OrderID, Customers.CustomerName
FROM Orders
FULL OUTER JOIN Customers ON Orders.CustomerID = Customers.CustomerID;
```

## Conclusion

Understanding how to join tables in SQL is essential for querying databases effectively. By mastering SQL joins, you can retrieve and analyze data from multiple related tables efficiently.

## Additional Resources

- [SQL Joins Explained: Inner, Outer, Left, and Right Joins](https://www.sqlshack.com/sql-joins-explained-inner-outer-left-and-right-joins/)
- [W3Schools SQL Joins Tutorial](https://www.w3schools.com/sql/sql_join.asp)