```
Insertion Sort is a simple sorting algorithm that builds the final sorted array one element at a time. It takes each element from the unsorted portion and inserts it into its correct position in the sorted portion by shifting larger elements one position to the right. This process continues until the entire list is sorted.
```

Here is the Insertion sort
```
#include <stdio.h>

int main() {
    int A[] = {5, 2, 4, 6, 1};
    int n = sizeof(A) / sizeof(A[0]);

    for (int j = 1; j < n; j++) {
        int key = A[j];
        int i = j - 1;

        while (i >= 0 && A[i] > key) {
            A[i + 1] = A[i];
            i--;
        }

        A[i + 1] = key;
    }

    printf("Sorted array: ");
    for (int i = 0; i < n; i++)
        printf("%d ", A[i]);

    return 0;
}

```
