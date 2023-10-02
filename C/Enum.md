#C

An `enumeration` is mainly used to create a list of predefined values to be picked from, like a menu for example:

```C
enum menu {
  COFFEE, //0
  SODA,   //1
  TEA,    //2
  JUICE,  //3
  BEER,   //4
}

int main(void) {
  enum menu mario = COFFEE;
  printf("%d", mario);
}
```

This code will create an enum menu with five beverages to choose from and an instance `mario` with the value `COFFEE`. Note that it is a good practice to name `enum` variables in UPPER CASE and with underlines to separate words.

Each value inside a `enum` variable corresponds to an integer value. By default, this value starts at 0 and increments by 1 with each addition, but individual values can be changed through an explicit declaration. Example:

```C
enum menu {
  COFFEE = 10,
  SODA = 25,
  TEA = 3,
  JUICE = 8,
  BEER,
}
```

**Obs: the value that corresponds to `BEER` is 9 and not 4, thats because the last element before this one has a value of 8.**

---------------

## Typedef

The Typedef keyword is used to create an alias in C. When used with a enum datatype, it removes the necessity to specify enum everytime it is accessed. Example:

```C
typedef enum menu {
  COFFEE,
  SODA,
  TEA,
  JUICE,
  BEER,
} Menu

int main(void) {
  Menu mario = COFFEE;  //specifying that it is a enum is unnecessary
  
}
```
