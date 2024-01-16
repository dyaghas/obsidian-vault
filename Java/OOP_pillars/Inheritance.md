#oop 

Inheritance is one of the pillars of Object Oriented Programming. It allows the creation of subclasses that are capable of inheriting properties and behaviors of the base class, known as the superclass.

A subclass is created through the `extends` keyword as follows:

```java
public class subClassName extends SuperclassName {
	subclass code.
}
```

Common behavior should be kept in one class, and different behavior in separate classes. This way, the code can be reused and easily read.

All the objects should be kept in a single data structure.

Public instance variables, public methods and private instance variables are inherited.

----

Objects and references does not have to match each other. For example, a person object can reference a student like in the example:

Person p = new Student();

![[reference_object_inheritance.png]]

Likewise, an array of Person can store student objects.

You can think of it like `reference - template` instead of `reference - object`. See [[Narrowing]] for more information

- The parent is called superclass and the child is called subclass.

- Classes with the `final` keyword cannot be inherited from.

- [[Composition]] is another well known way of achieving code reusability