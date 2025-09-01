# 02: Basic Queries

This guide covers the fundamental statements for retrieving data from a database. It explains how to select columns, limit results, and use aliases to format output.

---

## The `SELECT` and `FROM` Statements

The most basic query consists of two parts: the `SELECT` statement, which specifies the columns to retrieve, and the `FROM` clause, which identifies the table containing those columns.

- **Query**: A request for data from a database.

- `SELECT`: The keyword that initiates a data query. It is followed by a comma-separated list of the columns to be retrieved.
  
- `*`: A wildcard character used in place of column names to select all available columns from the table.

- `FROM`: The clause that specifies the table from which to retrieve the data.

```sql
-- Syntax
SELECT * FROM table_name;

-- Select all columns from the 'customers' table
SELECT * FROM customers;

-- Select only the customer's name and city
SELECT customerName, city FROM customers;
```

---

## Limiting Results

The `LIMIT` clause restricts the number of rows returned by a query. This is useful for previewing a large table without retrieving the entire dataset, which improves performance and readability.

- `LIMIT`: A clause that takes an integer to specify the maximum number of rows to return. It is placed at the end of the query.

```sql
-- Retrieve the first 5 records from the 'products' table
SELECT productName, productLine, buyPrice
FROM products
LIMIT 5;
```

---

## Column Aliases

An alias provides a temporary, custom name for a column in the query's result set. Aliases do not change the column's permanent name in the table; they only affect the display in the current query's output, which is useful for improving readability.

- `AS`: The keyword used to assign an alias to a column. If the alias contains spaces or special characters, it must be enclosed in double quotes (`"`).

```sql
-- Select the customerName column and display it as "Client Name"
-- Select the country column and display it as "Location"
SELECT
  customerName AS "Client Name",
  country AS Location
FROM customers;
```