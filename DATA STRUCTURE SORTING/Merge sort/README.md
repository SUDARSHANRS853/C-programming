## Definition
```
Merge Sort is a divide-and-conquer sorting algorithm. It works by recursively dividing the array into two halves, sorting each half, and then merging the two sorted halves into a single sorted list. Its time complexity is O(n log n) in all cases and it is a stable sorting technique.
```


Here is the Merge sort
```
#include <stdio.h>

// Function to merge two halves
void merge(int A[], int lb, int mid, int ub) {
    int i = lb;       // starting index of left half
    int j = mid + 1;  // starting index of right half
    int k = lb;       // index for temporary array

    int B[1000];      // temporary array (size should be >= array size)

    // Merge the two halves into B[]
    while (i <= mid && j <= ub) {
        if (A[i] <= A[j]) {
            B[k] = A[i];
            i++;
        } else {
            B[k] = A[j];
            j++;
        }
        k++;
    }

    // Copy remaining elements of left half
    while (i <= mid) {
        B[k] = A[i];
        i++;
        k++;
    }

    // Copy remaining elements of right half
    while (j <= ub) {
        B[k] = A[j];
        j++;
        k++;
    }

    // Copy sorted values back to original array A[]
    for (k = lb; k <= ub; k++) {
        A[k] = B[k];
    }
}

// Merge sort function
void mergeSort(int A[], int lb, int ub) {
    if (lb < ub) {
        int mid = (lb + ub) / 2;

        mergeSort(A, lb, mid);     // Sort left half
        mergeSort(A, mid + 1, ub); // Sort right half
        merge(A, lb, mid, ub);     // Merge them
    }
}

int main() {
    int A[] = {15, 5, 24, 8, 1, 3, 16, 10, 20};
    int n = sizeof(A) / sizeof(A[0]);

    printf("\nOriginal Array:\n");
    for (int i = 0; i < n; i++)
        printf("%d ", A[i]);

    mergeSort(A, 0, n - 1);

    printf("\n\nSorted Array:\n");
    for (int i = 0; i < n; i++)
        printf("%d ", A[i]);

    printf("\n");
    return 0;
}
```

```

