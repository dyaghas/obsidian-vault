#theory 

Narrowing refers to passing a higher size data type like an int to a lower size one like short. You can cast the `reference(object)` of one `class` type to other, but one of the two classes should inherit the other.

when a line of code snippet like the following is written:

```java
Person s = new Student("Cara", 1234);
s.getName();
```

At compile time, Java will look for the `getName()` at the `Person s` reference. Then, at runtime, it will look for the same method at the `Student` object. If it is not present in one of them, a compile time or runtime error will happen.

To solve this problem, a technique known as `narrowing` can be used, for example:

```java
subclass ref = (Subclass) superRef;
((Student)s).getSID();
```

*A call to super in a method get bound at compile time, so it refers to the class above the one it is inside*

*A call to "this" in a method get bound at runtime, so it refers to the object type.*