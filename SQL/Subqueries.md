#sql

A subquery, also known as a nested query or inner query, is a query embedded within another SQL statement. They are enclosed in parentheses and are used to retrieve data that will be used by the main query as a condition to further restrict the data to be retrieved. Subqueries can be used in various parts of a SQL statement, including the `SELECT`, `FROM`, `WHERE`, and `HAVING` clauses, for example:

```sql
SELECT * FROM books WHERE pages = (SELECT MAX(pages) FROM books);
```

The query above will return the book with the most amount of pages present in the table. It is important to note that subqueries are very demanding on big databases and it is preferable to use other aproaches like `join` whenever possible.
