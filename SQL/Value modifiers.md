#sql 

 [[PRIMARY KEY]]
 [[FOREIGN KEY]]
 [[String Functions]]

---------------------------------

## NOT NULL

This keyword determines that the specified column cannot be left empty:

```SQL
CREATE TABLE table_name (
column_name NOT NULL
);
```

-----------------------------

## DEFAULT

A modifier that defines a value that will be used if none is specified in the respective INSERT statement, for example:

```sql
CREATE TABLE table_name (
	column_name VARCHAR(100) default('This is a default value')
);
```

Obs: a column with `DEFAULT` can still have `NULL` values after an `ALTER` statement or an `INSERT` with a hardcoded `NULL` value.

---------------------------------

## AUTO_INCREMENT

This modifier is used to increment a value automatically. Its most common use is with numeric `primary keys`, which makes sure that each value is unique.

```sql
CREATE TABLE (
column_name INT PRIMARY KEY AUTO_INCREMENT
);
```

----------------------

