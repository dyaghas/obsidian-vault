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
