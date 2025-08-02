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
2. ## Swapping the two numbers using function
```
#include<stdio.h>

void swap(int *a, int *b){
int temp;
temp=*a;
*a=*b;
*b=temp;
}
int main(){
int x,y;
printf("enter two numbers:");
scanf("%d%d",&x,&y);
swap(&x,&y);
printf("after swaping the numbers x=%d and y=%d\n",x,y);
return 0;
}
```
Output
```
enter two numbers x and y:4 6
after swaping the numbers x=6 and y=4
```
3. ## WAP to find minimum and maximum elements in a given array using the function int find_max_min(int array[], int size,int *max, int *min);
```
#include<stdio.h>
int find_max_min(int array[],int size ,int*max,int*min){
*max=array[0];
*min=array[0];
for(int i=1;i<size;i++){
if(array[i]>*max)
*max=array[i];
if(array[i]<*min)
*min=array[i];
}
return 0;
}
int main()
{
int arr[5]={10,5,30,2,15};
int max,min;
find_max_min(arr,5,&max,&min);
printf("max=%d\n",max);
printf("min=%d\n",min);
return 0;
}
```
Output
```
maximum and minimum numbers are:
max=30
min=2
```
4. ## WAP to store 10 numbers in an array. Remove the duplicate entries in the array.
```
#include<stdio.h>
int main()
{
    int a[10],size=10;
    printf("enter the 10 different numbers:");
    for(int i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
        
    }
   
    for(int i=0;i<size;i++)
    {
        for(int j=i+1;j<size;j++)
        {
            if(a[i]==a[j])
            {
                for(int k=j;k<size-1;k++)
                {
                    a[k]=a[k+1];
                    
                }
                size--;
                j--;
            }
        }
    }
    printf("array after removing duplications:\n");
    for(int i=0;i<size;i++)
    {
        printf("%d",a[i]);
        
    }
    return 0;
}
```
Output
```
enter the 10 different numbers:2 3 4 5 6 4 3 2 2 3
array after removing duplications:
23456
```
5. ## WAP to search for a given integer in an array using the linear search technique.
```
#include<stdio.h>
int main()
{
    int a[100],n,key,found;
    printf("enter the number of elements:\n");
    scanf("%d",&n);
    printf("enter the %d elements\n",n);
    for(int i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
    }
    printf("enter the number to search:\n");
    scanf("%d",&key);
    for(int i=0;i<n;i++)
    {
        if(a[i]==key)
        {
            printf("the entered %d number is found at position %d(index %d)",key,i+1,i);
        }
    }
}
```
Output
```
enter the number of elements:
4
enter the 4 elements
1 2 3 4
enter the number to search:
4
the entered number 4 is found at position 4(index 3)
```


