Here there is selection sort
```
#include <stdio.h>

int main() {
    int array[] = {5, 2, 8, 1, 4};
    int n = sizeof(array) / sizeof(array[0]);

    for (int x = 0; x < n; x++) {

        int index_of_min = x;

        // Find the index of the smallest element in the remaining array
        for (int y = x + 1; y < n; y++) {
            if (array[index_of_min] > array[y]) {
                index_of_min = y;
            }
        }

        // Swap the smallest element with the element at position x
        int temp = array[x];
        array[x] = array[index_of_min];
        array[index_of_min] = temp;
    }

    // Print sorted array
    printf("Sorted array: ");
    for (int i = 0; i < n; i++) {
        printf("%d ", array[i]);
    }

    return 0;
}

```

