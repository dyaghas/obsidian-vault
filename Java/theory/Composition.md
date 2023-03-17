#theory 

Composition is another aproach to achieve code reuse in object-oriented programming. As a counterpart to [[inheritance]], it creates a `has-a` relationship between classes and is more flexible as its goal is achieved through objects instead of classes and subclasses, meaning that it allows composition in different ways that can achieve different behaviors.

Here's an example of implementing composition in Java:

Suppose that we want to create a class called Car that has an Engine object. We can implement this using composition by creating an instance of the Engine class within the Car class.

```java
public class Car {
	private Engine engine

	//constructor
	public Car() {
		this.engine = new Engine();
	}

	public void start() {
		engine.start
	}

	public void stop() {
		engine.stop();
	}
}
```

In this example, the `Car` class has an instance variable called engine, which is an object of the Engine class. In the constructor of the `Car` class, we create a new instance of the Engine class and assign it to the engine variable.

We can then define methods in the Car class that delegate to the corresponding methods of the Engine class. In this example, we define a start() method and a stop() method that delegate to the start() and stop() methods of the engine object, respectively.

This allows us to use the Car class to start and stop the engine, without having to implement those methods directly in the Car class. This is an example of how composition can be used to achieve code reuse and create more modular and maintainable code.