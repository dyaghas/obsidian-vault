#data_structure 

In Java, user input is proccessed through an instance of the **Scanner** class.

```java
Scanner scannerName = new Scanner(System.in);
variable = scannerName.nextLine();
```

Other methods can be used like nextInt() or nextDouble(), but be careful because after reading an int or any other specific datatype, the method will leave a newline character ('\n') in the input stream, meaning that if nextLine() is called right after that, it will read an empty line.