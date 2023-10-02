#C

`Char` is a `datatype` that can store a single character. Computers does not understand characters, so to be able to interpret a character, it converts a numerical value to a character through the `ASCII Table`, which goes from the integer 0 to 255. Because of that, a `char` occupies 1 byte in memory or 8 bits (The amount necessary to represent the number 255 in binary).

The following line of code creates a `char` variable:

```C
char var = 'A';
```

----------------------------

## Strings

C does not have a `string` datatype, instead, it works with arrays of characters:

```C
char var[] = "String example";
```

You can access the whole array or a single character through its index:

```C
//prints the whole string
printf("%s", var);

//prints the character with the corresponding index from a string
printf("%c", var[0]);
```
