#sql 

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


--------------