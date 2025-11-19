```
Bubble Sort is a simple sorting algorithm that repeatedly steps through the list, compares adjacent
 elements, and swaps them if they are in the wrong order. This process is repeated until no more
swaps are needed, indicating that the list is sorted.
```

Here  we are doing bubble sort logic 
```
#include<stdio.h>

int main() {
    int arr[] = {2,3,4,2,3,4,5,6};
    int n = sizeof(arr)/sizeof(arr[0]);
    int flag, temp;
    for(int x = 0; x < n-1; x++) {
        flag = 0;   // assume no swap happened
        for(int y = 0; y < n-x-1; y++) {
            if(arr[y] > arr[y+1]) {
                temp = arr[y];
                arr[y] = arr[y+1];
                arr[y+1] = temp;
                flag = 1;   // swap happened
            }
        }
        if(flag == 0)
            break;   // array already sorted → stop early
    }
    printf("Sorted elements: ");
    for(int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    return 0;
}
```

