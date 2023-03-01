#theory

Used to trace code and track [variables](Variable) values throught its execution. Example:

int var1;
var1 = 52;
int var2;
var2 = var1;
var1 = 127;
System.out.println("var1: " + var1 + "var2: " + var2);

![[memory_model_1.png]]

**Memory model with objects**

int var1 = 52;
SimpleLocation ucsd;
ucsd = new SimpleLocation(32.9, -117.2);
SimpleLocation lima = new SimpleLocation(-12.0, -77.0);
lima.latitude = -12.04;

![[memory_model_2.png]]

*lima = ucsd
when an object is said to be equal another one, what actually happens is that both objects references the same memory space. That means that changing an object parameter will actually reflect in the other object as well.*

![[memory_model_3.png]]