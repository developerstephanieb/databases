# 01: Syntax

This guide explains the fundamental syntax rules of the SQL language, including how to write comments, conventions for case sensitivity, and how to terminate statements.

---

## Comments

Comments are used to explain sections of SQL code and are ignored by the database engine during execution.

- `--`: A single-line comment.

- `/* text */`: A multi-line comment. Useful for longer explanations or for temporarily disabling a block of code.

```sql
-- This is a single-line comment.
SELECT
    productName,
    buyPrice
FROM
    products;

/*
This is a multi-line comment.
*/
SELECT * FROM orders;
```

---

## Case Sensitivity

SQL syntax has specific rules regarding case sensitivity that distinguish keywords from identifiers like table and column names.

- **Keywords**: SQL keywords (e.g., `SELECT`, `FROM`, `WHERE`) are case-insensitive. By convention, keywords are written in uppercase to distinguish them from table and column names.

- **Identifiers**: The case sensitivity of identifiers (names of tables, columns, etc.) depends on the specific database system and its configuration.

---

## Statement Termination

An SQL statement is a single command sent to the database. While some database clients can execute single statements without a terminator, the standard is to end each statement with a semicolon.

- `;` (Semicolon): The semicolon is the standard statement terminator in SQL. It is required when executing multiple SQL statements in a single script to signal where one command ends and the next one begins.

```sql
-- Two separate statements, each terminated by a semicolon.
SELECT * FROM customers;
SELECT * FROM products;
```
