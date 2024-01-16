#sql
### AND

The `AND` operator is used to combine multiple conditions in a SQL statement. It returns true if all the conditions separated by `AND` are true.

```SQL
condition1 AND condition2;
```

---------------------

### OR

This operator is used to combine multiple conditions in a SQL statement. It returns true if at least one of the conditions separated by `OR` is true.

```SQL
condition1 OR condition2;
```

--------------------------

### NOT

It is used to negate a condition in a SQL statement. It returns true if the condition following `NOT` is false, and vice versa.

```SQL
NOT condition;
```

-------------------------

### IN

The `IN` operator is used to check if a specified value matches any value in a set. It is often used in the `WHERE` clause.

```SQL
IN(value1, value2, value3...);
```

-------------

### BETWEEN

It filters the result set within a range. It returns true if the value is within the specified range (inclusive).

```SQL
BETWEEN value1 AND value2;
```

---------------

### LIKE

The SQL `LIKE` operator is used in conjunction with the `SELECT` statement to filter rows based on a specified pattern in a column. It is commonly used with text-based columns, such as strings, to perform pattern matching. The `LIKE` operator allows you to search for a specified pattern within a column's data. The two wildcard characters often used with `LIKE` are:

- `_ (Underscore)`: Represents a single character. It can be used to match a specific character at a specific position. Example: `LIKE M _ _ _` is a string with four characters, starting with `M`;
- `% (Percent Sign)`: represents one or more characters. It can be used when the number of characters in the specified portion of the string is not known. Example: `LIKE M%` is a string starting with `M` with any number of characters.

Here's the basic syntax for using the `LIKE` operator:

```SQL
SELECT column1, column2 
FROM table_name 
WHERE column_name LIKE pattern;
```

---------------

