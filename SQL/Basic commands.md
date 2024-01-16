#sql

Here you can find some basic commands in SQL.

[[Value modifiers]]

For more advanced commands, take a look at [[Commands]]

## CREATE DATABASE

The SQL `CREATE DATABASE` command is used to create a new table in a relational database.

```SQL
CREATE DATABASE database_name;
```

Obs: in SQL, it is good practice to use single quotation `'` markers for text instead of double `"`

----------------------

## CREATE TABLE

The SQL `CREATE TABLE` command is used to create a new table in a relational database. 

```sql
CREATE TABLE table_name ( column1 datatype constraints, 
 column2 datatype constraints, 
 column3 datatype constraints, 
 ... 
 table_constraints );
```

----------------------

## INSERT

The SQL `INSERT` command is used to add new rows of data into a table. 

```sql
INSERT INTO table_name (column1, column2, column3, ...) 
VALUES (value1, value2, value3, ...);
```

----------------
## SELECT

The SQL `SELECT` statement is used to retrieve data from one or more tables in a database.

```sql
SELECT column1, column2, ... FROM table_name WHERE condition;
```

The `SELECT` statement can also be used with various SQL functions, such as COUNT, SUM, AVG, MAX, and MIN, to perform aggregate calculations on the data. For example:

```sql
SELECT COUNT(*) AS num_customers FROM customers;
```

--------------
### WHERE

The `WHERE` clause is used in conjunction with the `SELECT` statement to filter rows from a table based on a specified condition. This clause allows you to specify a condition that must be met for a row to be included in the query result. Here's the basic syntax of the `SELECT` statement with a `WHERE` clause:

```SQL
SELECT column1, column2, ... 
FROM table_name 
WHERE condition;
```

The `WHERE` statement can implement different conditionals like:

- Functions: LENGTH(), SUM(), AVG();
- [[Logical operators]]: AND, OR, NOT;
- Comparison operators: >, <, >=, <=;

Those are only some examples.

--------------------
## UPDATE

The SQL `UPDATE` statement is used to modify existing data in one or more rows of a table.

```sql
UPDATE table_name SET column1 = value1, column2 = value2, ... WHERE condition;
```

--------------

## DELETE

The SQL `DELETE` statement is used to remove one or more rows from a table.

```sql
DELETE FROM table_name WHERE condition;
```

--------------

## TRUNCATE

The SQL `TRUNCATE` statement is used to remove all the rows from a table in a database while keeping the table structure intact. Unlike the `DELETE` statement, which removes rows one by one and generates a lot of transaction log entries, the `TRUNCATE` command is typically faster because it deallocates the data pages used by the table and does not generate individual delete operations for each row.

```SQL
TRUNCATE TABLE table_name;
```

There are some important points to note about the `TRUNCATE` command:

- The table itself is not removed, only its rows;
- **Transaction**: Depending on the database system, `TRUNCATE` may be executed as an atomic transaction, meaning it can be rolled back if needed. However, this behavior can vary between database systems, so it's essential to consult the documentation for your specific database;
- **Conditions**: You cannot use a `WHERE` clause with the `TRUNCATE` command. It removes all rows from the table.

-------------------------

## ALTER TABLE

#### ALTER COLUMN

To alter an existing column in a table, you can use the `ALTER TABLE` statement with the `ALTER COLUMN` clause.

```sql
ALTER TABLE table_name ALTER COLUMN column_name data_type;
```

where `table_name` is the name of the table that contains the column you want to alter, `column_name` is the name of the column you want to alter, and `data_type` is the new data type that you want to assign to the column.

For example, if we have a table called `customers` with a column called `phone` that has a data type of `varchar(20)`, and we want to change the data type to `varchar(30)`, the SQL statement would look like:

```sql
ALTER TABLE customers ALTER COLUMN phone varchar(30);
```

#### ADD COLUMN

To add a column to a table, you can use the `ALTER TABLE` statement with the `ADD COLUMN` keyword.

```SQL
ALTER TABLE orders ADD COLUMN order_date DATE;
```

In this example, we are adding a new column called "order_date" to the "orders" table. The data type of the column is specified after the column name, in this case it is DATE.

You can also specify other column properties such as `NOT NULL`, `DEFAULT` value, or `UNIQUE` constraints when adding a column.

----------------------

#### RENAME COLUMN

To change the name of an existing column in a table, you can use the `ALTER TABLE` statement with the `RENAME COLUMN` clause.

```sql
ALTER TABLE table_name RENAME COLUMN old_column_name TO new_column_name;
```

-------------------

## DROP

The SQL `DROP` statement is used to delete an existing database, table, index, view, or other object in a database.

```sql
DROP object_type object_name
```

where `object_type` is the type of object you want to drop (e.g. DATABASE, TABLE, INDEX, VIEW, etc.), and `object_name` is the name of the object you want to drop.

For example, if we have a table called `customers` and we want to delete it from the database, the `DROP` statement would look like:

```sql
DROP TABLE customers;
```

This would delete the `customers` table from the database.

Note that when you drop an object, it cannot be undone and all data associated with that object will be permanently deleted. It's a good practice to always create a backup of the object or database before executing a DROP statement, and to use caution when dropping objects in a production environment.

---------


