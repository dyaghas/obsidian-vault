#C

`Char` is a `datatype` that can store a single character. Computers does not understand characters, so to be able to interpret one, it converts a numerical value to a character through the `ASCII Table`, which goes from the integer 0 to 255. Because of that, a `char` occupies 1 byte in memory or 8 bits (The amount necessary to represent the number 255 in binary).

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

The number of rows is left empty because the compiler will deduce it automatically according to the number of days inside the matrix. Its columns, on another hand, have to be specified so the compiler knows the maximum number of characters in each row plus the ending `NULL` character.

To print those weekdays , a for loop like the following will do the job: 

```C
for(int i = 0; i < 7; i++) {
  printf("%s\n", days[i]);
}
```

This algorithm will print the **i**th line in the matrix, meaning that each loop will print an entire day string.

The same ´array of strings´ can be created with pointers like the following:

```C
char *days[]  = {
"Monday",
"Tuesday",
"Wednesday",
"Thursday",
"Friday",
"Saturday",
"Sunday",
};
```

Those information will be allocated different in memory. With a matrix like in the first case, every empty index up to 10 on each string will be stored with an empty valuee, meaning that every string will have a length of 10, but with pointers, a single dimensional array will be defined storing pointers that refers to different strings, each one with different lengths, storing only one index with the `NULL` value. This can save memory space as each string will store only the necessary amount of information.

#### Reading a string input


```C
char var[10]

scanf("%s, var);
```

This method of scanning a string has some drawbacks, like only being able to strings with a size of up to the defined array length and storing only one word at a time, because the method scanf starts reading at the first character after a whitespace and stops when it finds a whitespace before a character.
