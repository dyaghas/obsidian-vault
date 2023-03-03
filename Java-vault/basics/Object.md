#basics 

It is an instance of a [class](Class.md).

Example: you can consider a blue car with four doors to be an object of the [class](Class.md) Car. It is part of a bigger group but has it's own characteristics, it is individual.

```java
Student s = new Student();
```

The **new** keyword is an operator that allocates space in memory.

--------

### **Object Creation**

Objects are created from the **inside out**. It starts at the superclass Object and goes all the way down to the subclass.

Student(); is passed to the constructor.

-----------------

### **Object Instantiation**

```java
ClassName objectName = new ConstructorName(arguments);
```

Now you can call methods in an **object** like this:

```java
objectName.methodName(parameters);
```

*The keyword this refers to the calling object*.