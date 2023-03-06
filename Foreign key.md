#sql 

In SQL, a foreign key is a column or a set of columns in a table that refers to the primary key of another table. A foreign key constraint is used to enforce referential integrity between two tables and to ensure that the data in the foreign key column(s) corresponds to the data in the primary key column(s) of the referenced table.

To create a foreign key constraint in a table, you can use the FOREIGN KEY keyword followed by the name of the column(s) that will reference the primary key of another table. The basic syntax for creating a foreign key constraint is as follows:

```sql
CREATE TABLE table_name (
	column1 datatype PRIMARY KEY,
	column2 datatype,
	...
	FOREIGN KEY (column2) REFERENCES other_table (other_column)
);
```