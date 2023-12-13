#sql 

They work like an `If statement` in any programming language, there is a conditional and if it is satisfied, something happens, if it isn't, something else happens.

```SQL
SELECT statement,
CASE
	WHEN conditional THEN do_something
	ELSE do_something_else
END AS alias_name
FROM table_name
```

There can be multiple `WHEN` clauses with different conditionals in a `Case statement`

```SQL
SELECT statement,
CASE
	WHEN conditional THEN do_something
	WHEN conditional2 THEN do_something2
	WHEN conditional3 THEN do_something3
	ELSE do_something_else
END AS alias_name
FROM table_name
```