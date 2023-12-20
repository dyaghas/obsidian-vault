#sql 

[[Subqueries]]
[[Case statement]]
[[Window functions]]

## INNER JOIN

The SQL `INNER JOIN` keyword is used to select rows from both tables as long as there is a match between the columns.

```SQL
SELECT table1.column1, table1.column2, table2.column2 
FROM table1 INNER JOIN table2 ON table1.column1 = table2.column2
```

The command above will select `column1` and `column2` from `table1` and `column2` from `table2` and show them if the comparison after the `ON` clause is true for the respective line.

Example:

Table atividade
![[table-atividade-innerjoin.png]]

Table funcionario
![[table-funcionario-innerjoin.png]]

```SQL
SELECT atividade.id_atividade, atividade.nome_atividade, funcionario.id_funcionario, funcionario.nome_funcionario 
FROM atividade INNER JOIN
funcionario ON atividade.id_funcionario_fk = funcionario.id_funcionario;
```

The `SQL` command is comparing `id_funcionario` and `id_funcionario_fk`, if there is a match between those two columns it will show the columns from the `SELECT` keyword

----------

## VIEW

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

The query `CREATE OR REPLACE VIEW` can be used to alter an existing view or create a new one if it does not exist:

```SQL
CREATE OR REPLACE VIEW view_name AS query
```

--------------

## ORDER BY

This keyword is used to order the result of a `SELECT` query through the specified column. In case of a text column, it orders alphabetically:

```SQL
SELECT * FROM table_name ORDER BY column1;
```

By default, the result is ordered in ascending order, but that can be changed with the `DESC` keyword after the specified column:

```SQL
SELECT * FROM table_name ORDER BY column1 DESC;
```

When specifying various columns in a select statement, the `ORDER BY` command can be used with a number as a parameter, specifying which of the columns should be used to order the data:

```SQL
SELECT column1, column2, column3 FROM table_name ORDER BY 3;
```

This query will use `column3` as a parameter for `ORDER BY`.

Another thing to note is that `ORDER BY` can be used with multiple columns as its parameters which will order by the first parameter, then the second etc.

---------------------
## GROUP BY

The GROUP BY keyword summarizes or aggregates identical data into single rows. For example: in a library database there can be multiple books that where written by the same author, now take a look at the following query:

```SQL
SELECT author_name FROM books GROUP BY author_name;
```

Result:

![[Pasted image 20231130134858.png]]

This will return all the author names in the database without any repetition, because the `GROUP BY` keyword groups every instance of an author name in the same row. By itself it is not very useful, but `GROUP BY` can be used with other functions like `COUNT` to retrieve very useful data, like how many books where written by every author, for example:

```SQL
SELECT COUNT(author_name), author_name FROM books GROUP BY author_name;
```

Result:

![[Pasted image 20231130134808.png]]

#### WITH ROLLUP

This keyword will add an summary of the entire table after all groups in a query with `GROUP BY` . For example:

```SQL
SELECT AVG(rating) FROM reviews GROUP BY series_id WITH ROLLUP;
```

In a TV series review database, this query can return the average rating of each series and the average rating of every series combined in the end.

Notes: 
- like the `ORDER BY` statement, `GROUP BY` accepts multiple parameters, meaning that it can group the authors entire name by selecting `authors_first_name` and `authors_last_name`, for example.
- To add conditionals to a `GROUP BY`, use the `HAVING` keyword instead of `WHERE`

--------------------

