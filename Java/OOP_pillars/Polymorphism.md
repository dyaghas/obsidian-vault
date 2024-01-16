#oop 

It means several different forms and occurs when there are many classes that are related to each other by **Inheritance**. Inheritance allows attributes and methods from a superclass to be inherited and accessed by its subclasses, but each subclass can have its own implementation of said methods and attributes. This means that `polymorphism` and `inheritance` are linked to one another.

Example:

```java
class Animal {
	public void makeSound() {
		System.out.println("The animal makes a sound");
	}
}

class Dog extends Animal {
	public void makeSound() {
		System.out.println("Au au");
	}
}
```

In the example above, the subclass `Dog` inherits the method `makeSound` from its superclass `Animal` and overwrites its characteristics, meaning that both `inheritance` and `polymorphism` are in action.