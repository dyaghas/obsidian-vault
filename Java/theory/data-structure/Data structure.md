#data_structure

A structure used to store and organize data in such a way that it can be accessed, processed and retrieved efficiently. It is built using one or more data types

----------

## Linear data structure

Data elements are arranged sequentially or linearly, meaning that each element is attached to the previous and next one.

**Ex: array, stack, queue and linked list.**

#### Static data structure

Has a fixed memory size, the elements are easier to access but the data structure size can't be changed.

[[Array]]

#### Dynamic data structure

The size is not fixed, meaning it can be randomly updated during runtime which may be considered efficient concerning the memory complexity of the code.

Instead of having a List class, Java has a list interface that is implemented in different classes like **ArrayList**.

[[ArrayList]]

[[LinkedList]]

[[Stack]]

[[Queue]]

-------------

## Non-linear data structure

Data elements are not placed sequentially or linearly. The elements cannot be iterated in a single run only.

**Ex: trees and graphs.**

**Hash table**: stores values which have keys associated with each of them. Lookup is very efficient if the key associated with the value is known, irrespective of the table size. **Direct addressing** uses the one-to-one mapping between the values and keys when storing in a table. however, there is a problem with this approach when there is a large number o key-value pairs. The table will be huge with so mnay records and may be impractical or even impossible to be stored. To avoid this problem, a [[hash function]] is used.

[[HashMap]]
[[TreeMap]]
[[LinkedHashMap]]
[[HashSet]]
[[TreeSet]]
[[LinkedHashSet]]


--------

- In Java, it is common for a data structure like ArrayList, LinkedList, HashMap or any other to implement an interface or extend an abstract class. This allows for easier code reusability and better organization.