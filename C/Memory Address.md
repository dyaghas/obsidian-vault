#C

Every variable in `C` has a `memory address` associated with it when created. It is the location where the variable is stored on the computer. Larger variables consumes more than 1 contiguous byte in memory, forming a group that represents this data. For example, a `floating point` consumes 4 bytes in memory.

To access the `memory address` of a variable, use the reference operator `&`. For example:

```C
int num = 10;
print("%p", &num); //This will output the memory address of the variable 'num'
				   //%p means 'pointer'
```

In this algorithm, `&num` is a [pointer](Pointer.md) that has the `memory address` of the variable `num` as its value.