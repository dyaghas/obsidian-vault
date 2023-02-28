#sql

Here you can find some basic commands in SQL

## CREATE TABLE
The SQL CREATE TABLE command is used to create a new table in a relational database. 

The basic syntax of the this command is as follows:

```sql
CREATE TABLE table_name ( column1 datatype constraints, 
 column2 datatype constraints, 
 column3 datatype constraints, 
 ... 
 table_constraints );
```

----------------------

## INSERT
The SQL INSERT command is used to add new rows of data into a table. 

The basic syntax of this command is as follows:

```sql
INSERT INTO table_name (column1, column2, column3, ...) 
VALUES (value1, value2, value3, ...);
```

----------------

## SELECT

The SQL SELECT statement is used to retrieve data from one or more tables in a database. The basic syntax of the this statement is as follows:

```sql
SELECT column1, column2, ... FROM table_name WHERE condition;
```

The SELECT statement can also be used with various SQL functions, such as COUNT, SUM, AVG, MAX, and MIN, to perform aggregate calculations on the data. For example:

```sql
SELECT COUNT(*) AS num_customers FROM customers;
```

--------------------

## UPDATE

The SQL UPDATE statement is used to modify existing data in one or more rows of a table. The basic syntax of this statement is as follows:

```sql
UPDATE table_name SET column1 = value1, column2 = value2, ... WHERE condition;
```

--------------

## DELETE

The SQL DELETE statement is used to remove one or more rows from a table. The basic syntax of the DELETE statement is as follows:

```sql
DELETE FROM table_name WHERE condition;
```

--------------

## ALTER TABLE

To alter an existing column in a table, you can use the ALTER TABLE statement with the ALTER COLUMN clause. The basic syntax for altering a column is as follows:

```sql
ALTER TABLE table_name ALTER COLUMN column_name data_type;
```

where `table_name` is the name of the table that contains the column you want to alter, `column_name` is the name of the column you want to alter, and `data_type` is the new data type that you want to assign to the column.

For example, if we have a table called `customers` with a column called `phone` that has a data type of `varchar(20)`, and we want to change the data type to `varchar(30)`, the SQL statement would look like:

```sql
ALTER TABLE customers ALTER COLUMN phone varchar(30);
```

----------------------

## RENAME COLUMN

To change the name of an existing column in a table, you can use the ALTER TABLE statement with the RENAME COLUMN clause. The basic syntax for renaming a column is as follows:

```sql
ALTER TABLE table_name RENAME COLUMN old_column_name TO new_column_name;
```

-------------------

## DROP

The SQL DROP statement is used to delete an existing database, table, index, view, or other object in a database. The basic syntax of the DROP statement is as follows:

```sql
DROP object_type object_name
```

where `object_type` is the type of object you want to drop (e.g. DATABASE, TABLE, INDEX, VIEW, etc.), and `object_name` is the name of the object you want to drop.

For example, if we have a table called `customers` and we want to delete it from the database, the SQL DROP statement would look like:

```sql
DROP TABLE customers;
```

This would delete the `customers` table from the database.

Note that when you drop an object, it cannot be undone and all data associated with that object will be permanently deleted. It's a good practice to always create a backup of the object or database before executing a DROP statement, and to use caution when dropping objects in a production environment.

---------
