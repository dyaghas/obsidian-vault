#C

`Bitwise operators` works with data bit by bit instead of considering the entire value one thing. The `bitwise operators` are: AND, OR, NOT, XOR, right shift and left shift.

----------------------

**Bitwise right shift and left shift**

Those operations shifts the bits a specified number of times. For example:

```C
//20 is 10100 in binary
A = 20;

//After a two bits right shift, the value of A will be 00101
A = A >> 2;
```
The bits that go over the boundaries are lost, a right shift of 4 bits in a 5 bits number will lose the 4 rightmost bits.

------------------------------

## Bitmask

A `bitmask` manipulate registers in a register memory at bit level. There are 4 bitmasks that corresponds to AND, OR, NOT and XOR.

---------------------

### Bit Clearing and Bit testing

Does an `AND` operation with the value and its mask: if the value is 1, it will test the bit, if it is 0, the value will be cleared.

Example of Bit Testing and Bit Clearing:

```C
  int a = 0b10101010;
  int b = 0b00001111;

  //The result will be 00001010
  int res = a & b;
```

-------------------

### Bit Setting

Does an `OR` operation with the value and its mask: if the mask bit is 0, the result will be the value itself, if it's 1, the result will be 1.

```C
  int a = 0b10101010;
  int b = 0b00001111;

  //The result will be 10101111
  int res = a & b;
```

----------------

### Bit Toggling

Does an `XOR` operation with the value and its mask: if the mask bit is 0, the result will be the value itself, if it's 1, the result will be the value's complement (its opposite).

```C
  int a = 0b10101010;
  int b = 0b00001111;

  //The result will be 10101111
  int res = a & b;
```

**Obs: to create bitmasks more effectively, use a `bitwise left shift`. For example:**

```C
//Bit setting

int a = 0b00101010;
//the same as a | 0b10000000
int res = a | (1 << 6);

//00101010 OR 10000000 = 10101010
```

Example 2:

```C
//Bit clearing

int a = 0b10101010;

//the same as a & 11011111
int res = a & ~(1 << 5);

//10101010 AND 11011111 = 10001010
```

This will clear the bit of index 5.

------------------

### Bit selection

You can select specific bits with bitwise operations. For example:

If there is a variable with the binary value of 10110010101 and you want to select the bits of indexes 4 to 7, the following command will do the job:

```C
int a = 0b10110010101;

int res = (a >> 4) & 0b1111111;
```

The (a >> 4) command will remove the bits of index 0 to 3 and the `0b1111` mask will sets the answer legth to 4.
