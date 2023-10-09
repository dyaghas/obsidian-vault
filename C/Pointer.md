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

------------------------------

## Dereference

A pointer is used to reference the memory address of a variable, but it can also access its value through a process called `dereferencing`.

Example:
```C
int x = 10;
int *ptr = &x;

printf("%d", *ptr) // The pointer is dereferenced with an *, called the `dereference operator`;
```

----------------------------------------

## NULL pointer Assignment

```C
int *ptr = NULL;
```

In C, the NULL variable is the same as ((void *) 0), which means that it is a void pointer (can be cast to any other type of pointer) that points to the neniry address 0, which is always invalid. In that case, values cannot be stored into this pointer before it receives a valid address or a runtime error will occur.

--------------------

## Pointers and Constants

The `const` keyword can be used in a pointer in two different cases: constant value or constant memory address.

### Constant Pointer

```C
int *const ptr = &some_data
```

The memory address stored in the pointer cannot be changed.

### Pointer to Constants

```C
const int *ptr = &some_data
```

The value pointed to cannot be changed by the pointer.

### Everything Constant

```C
const int const* ptr = &some_data
```

Neither the pointer nor the value it points to can be changed.
