#sql 

It works like a `GROUP BY` in a query, but instead of grouping various rows into a single one with the desired data (like the average salary of a department for example), it returns all the lines AND a the function result for that group in each of its lines. For example:

```SQL
SELECT emp_no, department, salary, AVG(salary) OVER() FROM employees;
```

This query will return a table with each employee number, its respective department and salary, but the last column `AVG(salary) OVER()` will also show the average salary of all the employees in all departments. This information is shown in every row and can be used to compare the employee salary with the average of the company, for example.

The `OVER` clause is used to construct a `window`. When it's empty, it will include all records.

![[Pasted image 20231220132017.png]]

-----------------------------
### PARTITION BY

```SQL
SELECT emp_no, department, salary, 
AVG(salary) OVER(PARTITION BY department)
FROM employees;
```

This does the same as the previous query, except that now the window function will return the average salary the department instead of the entire company. So if a employee works in the engineering department, the average salary of all engineers will be returned in its row.

![[Pasted image 20231220131921.png]]

------------------------------------

### ORDER BY

The `ORDER BY` clause can be used in a window function, but it will behave differently and will have different usages, for example:

```SQL
SELECT emp_no, department, salary, AVG(salary) OVER(PARTITION BY department ORDER BY salary) FROM employees;
```

In this case, it will show the same information as the query in the `PARTITION BY` section, but the window function column will show the average salary of said department up to the selected row, meaning that on the third row, the average salary shown will only consider this row and the previous ones (considering that they are all from the same department). Consequently, the last row of each department will show the average salary in its entirety.

![[Pasted image 20231220133257.png]]

