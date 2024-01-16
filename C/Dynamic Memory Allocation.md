#C 

Library: stdlib.h

## Malloc

```C
void *pointer_var = malloc(size);
//an alternative more usable in real cases
void *pointer_var = malloc(size*sizeof(type));
```

This function allocates a memory block of `size` bytes and returns a pointer of the specified type. All the values are undefined.

----------------------------

# Calloc

```C
void *var = calloc(num, size);
```

Calloc allocates a memory block of `num * size` bytes and returns a pointer of the specified type. all the values are initialized to 0.

--------------------------

## Realloc

```C
void *var = realloc(var, new_size)
```

Receives an address of memory already allocated `var` and changes its size to `new_size` through a new pointer. The address cannot be freed before using realloc or the program will crash.

It either expands or contracts the memory block (if possible) or allocates a new memory block of size `new_size` and frees the old block.

------------------

## Free

```C
free(pointer_var)
```

It deallocates space previously allocated by `malloc`, `calloc` or any other dynamic allocation method. If `free` is called two times in the same block of memory, the program will crash.