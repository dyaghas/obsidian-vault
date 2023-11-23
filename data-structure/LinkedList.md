#data_structure

It has  a very similar implementation to an [arrayList](ArrayList.md) but they work in different ways. While an [arrayList](ArrayList.md) has a regular array and creates another one when an element is added or deleted, the  `linkedList`  is a sequential [data structure](Data%20structure.md) consisting of items that are linked to each other. Data has to be accessed sequentially and random access is not possible. It works as the following: the elements are known as nodes, each node contains a key and a pointer to its successor node known as next. The first and last elements are called head and tail, respectively. nodes can be removed and inserted.

![[linkedlist_image.png]]

*ArrayList usage: data storage and access | LinkedList usage: data manipulation*

Creation syntax:

```Java
import java.util.LinkedList;

LinkedList<String> linkedListName = new LinkedList<String>();
```

## Useful methods

`LinkedList` has all of the same methods as the [[ArrayList]] class because they both implement the `list` interface. In addition to those methods, `LinkedList` also has some interesting ones:

- addFirst()
- addLast()
- removeFirst()
- removeLast()
- getFirst()
- getLast()

Those method names are pretty self explanatory, they can access the first and last elements in a `LinkedList`.