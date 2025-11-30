```
Quick Sort is a divide-and-conquer sorting algorithm that works by selecting a pivot element,
partitioning the array into two subarrays—one containing elements smaller than the pivot and
the other containing elements greater—then recursively sorting the subarrays. It provides an
 average time complexity of O(n log n).
```
Here is the quick sort
```
#include <stdio.h>

void swap(int *a, int *b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}

int partition(int arr[], int low, int high) {
    int pivot = arr[low];     // pivot = FIRST element
    int i = low + 1;
    int j = high;

    while (i <= j) {
        // move i until element > pivot
        while (i <= high && arr[i] <= pivot)
            i++;

        // move j until element < pivot
        while (arr[j] > pivot)
            j--;

        // swap elements on wrong side
        if (i < j)
            swap(&arr[i], &arr[j]);
    }

    // place pivot in correct position
    swap(&arr[low], &arr[j]);

    return j;  // correct position of pivot
}

void quickSort(int arr[], int low, int high) {
    if (low < high) {
        int p = partition(arr, low, high);

        quickSort(arr, low, p - 1);
        quickSort(arr, p + 1, high);
    }
}

int main() {
    int arr[] = {7, 2, 9, 4, 3};
    int n = sizeof(arr) / sizeof(arr[0]);

    quickSort(arr, 0, n - 1);

    printf("Sorted array: ");
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }

    return 0;
}

```
                 
