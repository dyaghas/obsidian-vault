#basics 

A package in [[Java]] is used to group related [classes](Class), it works like a folder in a file directory. Its main usage is to avoid name conflicts and make the code more maintainable. Packages are divided into two categories:

**Built-in Packages**: are packages from the Java API, a library of prewritten classes that are free to use and contains components for managing input, database programming, and more. This library is divided into packages and classes, which allows an entire package or an individual class to be imported.

**User-defined Packages**: created by the user.

```java
import package.name.Class;   // Import a single class
import package.name.*;   // Import the whole package
```