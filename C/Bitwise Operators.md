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

### Bit Clearing

Does an `AND` operation with the value and its mask: the mask value is 0 and the result will be 0.

### Bit Testing

Also uses the `AND` operator: the mask value is 1 and the result will be the value itself.

Example of Bit Testing and Bit Clearing:

```C
  int a = 0b10101010;
  int b = 0b00001111;

  //The result will be 00001010
  int res = a & b;
```

### Bit Setting

Does an `OR` operation with the value and its mask: if the mask bit is 0, the result will be the value itself, if it's 1, the result will be 1.

```C
  int a = 0b10101010;
  int b = 0b00001111;

  //The result will be 10101111
  int res = a & b;
```

### Bit Toggling

Does an `XOR` operation with the value and its mask: if the mask bit is 0, the result will be the value itself, if it's 1, the result will be the value's complement (its opposite).

```C
  int a = 0b10101010;
  int b = 0b00001111;

  //The result will be 10101111
  int res = a & b;
```
