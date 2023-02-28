#algorithm

It is the simplest searching algorithm and works by swapping the items between them if they are in the wrong order. Can be used when simple code is prefered and time complexity is not a big deal. **Not really usable in real situations because of its inefficiency when compared to [[Selection Sort]].**

![[Bubble-sort-example-300px.gif]]

--------

#### Big O

worst case: O(n²)
average case: O(n²)
best case: O(n) -> happens when data is already sorted

----

```java
public static void bubbleSort(int[] arr) {
    int n = arr.length;
    for (int i = 0; i < n - 1; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j+1]) {
                // Swap arr[j] and arr[j+1]
                int temp = arr[j];
                arr[j] = arr[j+1];
                arr[j+1] = temp;
            }
        }
    }
}
```