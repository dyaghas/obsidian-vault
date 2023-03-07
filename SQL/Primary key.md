#sql 

In SQL, a primary key is a column or combination of columns in a table that uniquely identifies each row in the table. The primary key is used to enforce data integrity and to ensure that each row in the table can be uniquely identified.

To create a primary key in a table, you can use the PRIMARY KEY constraint. The basic syntax for creating a primary key is as follows:

```sql
CREATE TABLE table_name (
	column1 datatype PRIMARY KEY,
	column2 datatype,
	...
);
```

In this case, `column1` is the primary key.

Example:

```sql
CREATE TABLE Customers (
	id int PRIMARY KEY,
	first_name varchar(50),
	last_name varchar(50),
	email varchar(100)
);
```

Note that a primary key must have unique values and cannot contain NULL values. If you try to insert a row with a duplicate primary key value or a NULL value in the primary key column, the database will return an error.

-----------

## DROP PRIMARY KEY

A `PRIMARY KEY` constraint can be dropped like the this:

```sql
ALTER TABLE table_name
DROP PRIMARY KEY;
```

or

```sql
ALTER TABLE table_name
DROP CONSTRAINT column_with_primary_key;
```

------------

Related: [[Foreign key]]