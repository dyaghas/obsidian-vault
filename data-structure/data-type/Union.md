#data_type

In C, `Union` is a `data type` that can store mutiple variables of different data types in the `same memory location`.

Let's say that a program needs two different ways to access a memory location. One that access an entire byte and another one that access it bit by bit:

```C
typedef struct {
  uint8_t enable : 1;
  uint8_t ready : 1;
  uint8_t mode : 2;
  uint8_t something_else : 2;
} structEx;

typedef union {
  RegBits bits;
  uint8_t byte;
} unionEx;

//Main method here
unionEx myUnion = {.byte = 0x01};

regA.bits.mode = 3;

```

This union has two variables, one of type `structEx` (the bit field defined right above it) and another one of type uint8_t. In the execution a union `myUnion` is defined with its byte value set to 0x01 (10000000 bits) and in the following line the value 3 is stored in the bits that corresponds to `mode` . After doing that, the final value will be 0xD (10110000 bits) as the third and fourth bits where changed to 11 (3 in hexadecimal).

Note: the bit field variables definition order matters as it will define where each bit will be positioned.