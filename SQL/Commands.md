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