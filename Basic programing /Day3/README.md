1. ## WAP to sort the given array in ascending and descending order.
```
#include <stdio.h>

int main() {
    int array[100], n, i, j, temp;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    printf("Enter %d elements:\n", n);
    for(i = 0; i < n; i++) {
        scanf("%d", &array[i]);
    }

    // Sorting in ascending order
    for(i = 0; i < n - 1; i++) {
        for(j = i + 1; j < n; j++) {
            if(array[i] > array[j]) {
                temp = array[i];
                array[i] = array[j];
                array[j] = temp;
            }
        }
    }

    printf("\nAscending order: ");
    for(i = 0; i < n; i++) {
        printf("%d ", array[i]);
    }

    // Sorting in descending order
    for(i = 0; i < n - 1; i++) {
        for(j = i + 1; j < n; j++) {
            if(array[i] < array[j]) {
                temp = array[i];
                array[i] = array[j];
                array[j] = temp;
            }
        }
    }

    printf("\nDescending order: ");
    for(i = 0; i < n; i++) {
        printf(" %d ", array[i]);
    }

    printf("\n");
    return 0;
}
```
Output
```
Enter the number of elements: 4
Enter 4 elements:
1 2 3 4

Ascending order: 1 2 3 4 
Descending order:  4  3  2  1 
```



```
