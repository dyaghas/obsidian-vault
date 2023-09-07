#C 

A `pointer` is a variable that stores the `memory address` of another variable of a specified type as its value.

Example:

```C
int num = 10;
int* ptr = &num;
```

The variable `ptr` has the `num` variable address as its value. 

- The `*` character can be placed in the variable type or its name to create a pointer;
- Pointers have types like any other variable, meaning that you have to create an int pointer to access an int variable, for example.
- **Be careful!** Pointers must be handled with care, since it is possible to damage data stored in other memory addresses.