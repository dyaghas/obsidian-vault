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

//option 1
char var[] = "String example";

//option 2
char var[] = {'S', 't', 'r', 'i', 'n', 'g', ' ', 'e', 'x', 'a', 'm', 'p', 'l', 'e', '\0'};

//option 3
char var[14] = {'S', 't', 'r', 'i', 'n', 'g', ' ', 'e', 'x', 'a', 'm', 'p', 'l', 'e'};
```

**Obs:** strings in C always ends with a `NULL` value, which means that an array with 14 characters will need 15 indexes, one for the `NULL` value. This is particularly important to remember when using `option 2` to define a string. in option 3, don't forget to reserve one more index for the `NULL` element.

#### Printing a string

You can access the whole array or a single character through its index:

```C
//prints the whole string
printf("%s", var);

//prints the character with the corresponding index from a string
printf("%c", var[0]);
```

#### Constant Strings

Strings can be made constant through the `constant` keyword or a pointer:

```C
//Constant keyword
const char var[] = "This is a string";

//constant string through a pointer
char *var = "This is a string";
```

Declaring a constant string through a `pointer` is not very straightfoward, but the value it points to can be changed, which means that the variable can store another completely different string, even if it is bigger than the previous one.

```C
char *str = "Hello";

str = "This is another string";
```
#### String matrix

A bidimensional matrix can be created to store the weekdays for example:

```C
char days[][10] = {
"Monday",
"Tuesday",
"Wednesday",
"Thursday",
"Friday",
"Saturday",
"Sunday",
};

printf("%s", days[3]); 
```
