#data_structure 

A [variable](Variable.md) access can be changed through visibility modifiers to make the code more readable and not as prone to human failure.

----

**Protected**: can be accessed by the same class, package and any subclass.

**Package**: can be accessed by the same class or package.

**Public**: can be accessed from anywhere.

**Private**: can be accessed by the same class only.

**Static**: means that a method or variable is defined for the class, but not a particular object in the class.

----

- It is a good practice to only use **protected** and **package** modifiers when extremely necessary.

- **Static** methods and variables should be used with caution, they can easily make your code hard to read and debug when programming in OOP and also break encapsulation because any object of the current class will be able to access it.