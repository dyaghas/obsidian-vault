#C

`Bitwise operators` works with data bit by bit instead of considering the entire value one thing. The `bitwise operators` are: AND, OR, NOT, XOR, right shift and left shift.

**Bitwise right shift and left shift**

Those operations shifts the bits a specified number of times. For example:

```C
//20 is 10100 in binary
A = 20;

//After a two bits right shift, the value of A will be 00101
A = A >> 2;
```
The bits that go over the boundaries are lost, a right shift of 4 bits in a 5 bits number will lose the 4 rightmost bits.
