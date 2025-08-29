# 02: Basic Queries

This guide covers the fundamental statements for retrieving data from a database. It explains how to select columns, limit results, and use aliases to format output.

---

## The `SELECT` and `FROM` Statements

[description/intro]

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

```sql
```

---

## Column Aliases

```sql
```