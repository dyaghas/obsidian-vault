#C

Structure is a composite data type used to group together variables of different data types, those variables are called `members`. 
It is similar to an array but with less limitation to its values and their data types. Example:

```C
struct Person {
  char name[50];
  int age;
  float height;
};
```

To create an instance of the structure Person, use the following syntax:

```C
struct Person structName;
```

To access `members` of a structure, use the `.` syntax:

```C
structName.memberName
```

When accessing a structure `member`, you can work with its value or memory address like any other variable

**Values cannot be accessed to strings directly in a structure, to do that, call the function strcpy(): **

```C
struct Person person1;
strcpy("This is a string", person1.name);
```

## Typedef

The `Typedef` keyword is used to create an `alias` in C. When used with a struct datatype, it removes the necessity to specify `struct` everytime a struct is accessed. Example:

```C
typedef struct myStruct {
  int var;
} myStruct;

//creating an instance of myStruct
myStruct struct1;

//storing a value in the 'var' variable
struct1.var = 1;
```

In the code snippet above, there's no need to type `struct myStruct struct1` when creating an instance of `myStruct`.
