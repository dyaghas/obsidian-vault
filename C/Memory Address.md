#C

Every variable in `C` has a `memory address` associated with it when created. It is the location where the variable is stored on the computer. Larger variables consumes more than 1 contiguous byte in memory, forming a group that represents this data. For example, a `floating point` consumes 4 bytes in memory.

To access the `memory address` of a variable, use the reference operator `&`. For example:

```C
int num = 10;
print("%p", &num); //This will output the memory address of the variable 'num'
				   //%p means 'pointer'
```

In this algorithm, `&num` is a [pointer](Pointer.md) that has the `memory address` of the variable `num` as its value.

- Memory addresses are represented in the `hexadecimal` form. Example: 0x7ffe5367e044

---------------------

## Buffer overflow

Be careful when writing or reading information, as they can be placed adjacent to one another and some programming languages does not perform any sort of range checking when accessing a memory address, which means that you can accidentally manipulate information from another array if the specified index overflows. Look at the example below:

```C
char A[8] = "";
unsigned short B = 1979;
```

![[Pasted image 20230817214848.png]]

Consider That the variables `A` and `B` are adjacent in memory, `A` has 8 bytes and `B` has 2 bytes allocated. See what happens if you try to store the string `excessive` which has 10 bytes (C language default library uses null-terminated strings, which means that they always end with a null character, adding an extra byte), in the variable `A`:

![[Pasted image 20230817214903.png]]

The excessive 2 bytes overflows and corrupts the variable `B` data.

`Buffer Overflow` is a major problem as malicious hackers can use it to access or change information in a program.

-----------------

[[Bitwise Operators]]