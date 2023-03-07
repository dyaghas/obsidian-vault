#oop 

Common behavior should be kept in one class, and different behavior in separate classes. This way, the code can be reused and easily read.

All the objects should be kept in a single data structure.

Public instance variables, public methods and private instance variables are inherited.

----

Objects and references does not have to match each other. For example, a person object can reference a student like in the example:

Person p = new Student();

![[reference_object_inheritance.png]]

Likewise, an array of Person can store student objects.

You can think of it like reference - template instead of reference - object.

*The parent is called superclass and the child is called subclass.*