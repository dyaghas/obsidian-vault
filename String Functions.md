#sql 

In SQL, String Functions are used to manipulate strings in the database, changing their value, doing concatenations, comparisons etc.

---------------------------

## CONCAT

This function takes any number of strings as parameters and concatenates them into a single one:

```sql
SELECT CONCAT("This", "is", "a", "string");

--An example with variables first_name and last_name:
SELECT CONCAT(first_name, last_name);
```

#### Notes

 - The `AS` keyword can be used to change the `SELECT` column name;
 - There is the `CONCAT_WS` variant (Concatenate With Separator) that accepts a separator that will be placed between every concatenated variable as its first parameter.

----------------

## SUBSTRING

It receives three parameters, the string, the first index and its length. After that, the function returns the substring between the specified range:

```sql
SELECT SUBSTRING("This is a string", 4, 7);

--Returns 's is a '
```

#### Notes

- If the substring `length` is not specified, the function will consider the entire range after the starting index;
- Negative numbers can be used to start counting from the last character in descending order;
- `SUBSTR()` is a smaller version of the exact same function.

--------------

## REPLACE

The `REPLACE` function takes three parameters: string, the substring that will be replaced and its new value.

```sql
SELECT REPLACE('Hello World', 'World', "Universe");

--Returns 'Hello Universe'
```

It is important to note that this function does not make any changes to the original data, only to the `SELECT` statement itself.

---------------

