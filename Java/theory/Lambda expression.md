#theory 

It is a short block of code that takes in parameters and returns a value. Lambda expressions are similar to [methods](Method.md), but they don't need a name and can be implemented right in the body of the method.

```java
parameter -> expression
```

or

```java
(parameter1, parameter2) -> expression
```

The expressions are limited. They have to immediately return a value, and they cannot contain variables, assignments, or statements such as **if** or **for**. To do more complex operations, a code block can be used with curly braces. If the lambda expression needs to return a value, then the code block should have a return statement.

```java
(parameter1, parameter2) -> { code block }
```