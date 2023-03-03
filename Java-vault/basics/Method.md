#basics 

A series of rules and actions that are defined to achieve a specific goal inside a [class](Class.md), it is associated with an object. For example: format a text or verify if a password is valid.

A method always has a return type, even if it does not return anything. Some examples are:
**void** (does not return anything), **boolean**, **int**, **float**, etc.

**Method & function**: a method is called dependently, which means the data is passed implicitly or internally. On another hand, a **function** is called independently, meaning the data is passed explicitly or externally. **TLDR**: a method is associated with an object and a function is not.

[function / method recursion](Recursion.md)

-------------------

**Constructor**: special method that gets called when an object is created. Does not have a return type, not even void.

**Getters & setters**: Are capable of accessing a private [variable](Variable.md) outside of its class, returning or changing it's value, respectively.

-----

**Method overload**: When multiple constructors are present in the same [class](Class.md), accepting different arguments.

A constructor with no arguments is called a "default constructor".

*Overloaded methods can have different return types, but having different parameters is a must.*

**method override**: When a subclass has the same method name with the same parameters as the superclass