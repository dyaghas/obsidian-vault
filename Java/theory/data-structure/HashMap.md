It stores items in **key / value** pairs that can be accessed by a String index, for example. One object is used as a key (index) to another object (value). Keys and values don't have to store data of the same type, a `HashMap` can have a int key and a String value, for example.

![[Pasted image 20230426132026.png]]

Syntax:

```Java
import java.util.HashMap;

HashMap<keyType, valueType> hashMapName = new HashMap<keyType, valueType>();
```

## Useful methods

Add item
```Java
hashMapName.put(keyVar, valueVar);
```

Access item
```java
hashMapName.get(keyVar);
```

Remove item
```java
//remove single item through its key
hashMapName.remove(keyVar);

//remove all items
hashMapName.clear();
```

Get hashMap size
```java
hashMapName.size();
```

## Iterate a HashMap

loop through keys
```java
for(keyType i : hashMapName.keySet()) {
	//do something
}
```

loop through values
```java
for(valueType i : hashMapName.values()) {
	//do something
}
```

- Keys and values in a HashMap are actually objects.