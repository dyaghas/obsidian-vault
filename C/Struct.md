#C

Structure is a composite `data type` used to group together variables of different data types, those variables are called `members`. 
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

---------------------

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

-----------------

## Initialization

There are two types of `structure initialization` in C, `implicit initialization` and `explicit initialization`.

Consider this `structure` for the following examples:

```C
//structure example
typedef struct Guy {
	char *name;
	int age;
} Guy;
```

#### Implicit initialization

```C
Guy {
	"Peter",
	25
}
```

This type of initialization can be confusing on bigger `structures` as the variable that is being initialized is not named.

#### Explicit initialization

```C
Guy {
	.name = "Peter";
	.age = 25;
}
```

The variable names are explicit and they can be initialized out of order.

---------------

#### Nested initialization

A structure can be initialized inside another one:

```C
//consider the structure Guy and a new Car struct
Car {
	.brand = "Nissan",
	.year = 2023,
	.owner = {
		.name = "Gabriel",
		.age = 30,
	},
}
```

------------------------

[[BitField]]