#algorithm

The QuickSort works with a variable called `pivot` that will have a huge impact in the algorithm's efficiency. Ideally, the `pivot` has to be as close as possible to the average value in the dataset, dividing it into two parts of similar size. For the sake of simplicity, sometimes the `pivot` is chosen as the first or last element on a list, with no regards to its value or impact.

The sorting works with two pointers, one starts at index 0 and the other one at -1, let's call them **i** and **j**, respectively. **i** is the value that is being compared to the `pivot`, if it is smaller than the `pivot`, **j** is incremented by one. Each time **i** and **j** are in different indexes, their values are swapped, but if they are in the same index, nothing happens. After this step is done, the dataset will have two parts, one before the `pivot` with values smaller than it and another after the `pivot`, with values bigger than it. Those values will be separated into two arrays through recursion, which means that those resulting arrays will suffer the same process until there are multiple arrays with only one element each, when this step is done, the array will be sorted. 

--------------------

#### Big O

- Average case: O(n log(n))

- Worst case: O(n²): Occurs when the pivot is the biggest or smallest element in the dataset, dividing it into a big array and a small one.

- Best case: O(n log(n)): Happens when the pivot is as close as possible to the average value in the dataset, dividing it into two similar sized arrays.
