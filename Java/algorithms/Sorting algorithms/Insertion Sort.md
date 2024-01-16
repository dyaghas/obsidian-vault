#algorithm 

it is a brute-force sorting algorithm that does fewer comparisons than the `Selection Sort`.
`Insertion Sort` works by choosing an item and ordering the direct neighbors whether they are greater/smaller than the chosen item. As the number of sorted items builds, the algorithm checks new items against the sorted items and inserts the new item into the right position in the list. Mainly used when there are only a few elements left to sort or the array is small.

It is an **in-place** sorting algorithm, which means that it doesn't need any extra memory allocation as the sorting is contained in the array itself.

![[Insertion-sort-example-300px.gif]]

---------

#### Big O

- average case: O(n²)

- worst case: O(n²) -> when the array is sorted in reverse order

- best case: O(n²) -> when the dataset is already sorted
