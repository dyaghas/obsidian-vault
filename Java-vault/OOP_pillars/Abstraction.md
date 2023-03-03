#oop 

Responsible for hiding unnecessary information, allowing the user to implement complex logic without worrying about all the hidden complexity

Ex: public abstract class Person {

**You cannot create instances of an abstract class, it can only be accessed through subclasses. For example, if we have two abstract classes called Vehicle and Car, our car object will reference Car as the Vehicle class may not have every characteristic needed to fufill the role of a car.**

abstract methods does not have a body and the subclasses must override it.

-------

#### Through abstraction you can achieve both **implementation** and **interface**.

**Implementation**: instance variables, methods and anything related to common behavior that a class should have.

**Interface**: defines which method signatures have to be overriten in a subclass.

*If you want an interface but no implementation, use an interface instead of an abstract class (when there's no common code, for example).*

*Classes can inherit from an abstract class and multiple interfaces at the same time.*