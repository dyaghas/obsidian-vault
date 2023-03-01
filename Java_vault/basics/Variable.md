#basics 

A variable has an identifier and a value associated with it

```java
int num = 5
```

int --> datatype
num --> identifier
5 --> value

----

A variable cannot be accessed outside of it's [scope](Scope).

**Local variable**: Declared inside a method. The method is it's [scope](Scope).

**Member variables**: are declared outside methods. They have a broader scope and can be used inside any [method](Method).

-------

**Argument**: value passed when a function is called

**Parameter**: an argument passed into a function or a [method](Method) definition. They behave like a local **variable**.

**Attribute**: an argument declared outside a [method](Method) in a Class, they are fields.

*The "this" keyword is optional. Java will first look in the method's scope for a variable, if it is not found there, Java will look at the object's scope.*