#sql

An SQL view is a read-only virtual table derived from the result of a `SELECT` query. It allows you to create a reusable and virtual representation of a subset of data of one or more tables. Views have many purposes like simplyfing complex queries and creating a consistent interface to the data for different applications and users.

Example: 

```SQL
CREATE VIEW viewName AS
SELECT * FROM tableName WHERE id= 5;
```

The query above will create a view that will select all instances from the `tableName` that has an id = 5. This is a simple query but more complex ones with multiple tables, `JOIN`, `GROUP` and more can be inserted into a view with no problem.

To access a view, use the `SELECT` statement:

```SQL
SELECT * FROM viewName;
```
