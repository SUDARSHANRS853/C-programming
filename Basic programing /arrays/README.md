1. # Addition of two arrays
```
#include<stdio.h>
int main()
{
    int i,a1[5],a2[5],sfa[5];
    for(int i=0;i<5;i++)
    {
        scanf("%d",&a1[i]);
    }
    for(int i=0;i<5;i++)
    {
        scanf("%d",&a2[i]);
    }
    for( int i=0;i<5;i++)
    {
        sfa[i]=a1[i]+a2[i];
        printf("sum of two array at index  %d is%d\n",i,sfa[i]);
    }
    
    return 0;
}
```
Output
```
1 3 4 6 7 
1 2 4 7 9
sum of two array at index  0 is2
sum of two array at index  1 is5
sum of two array at index  2 is8
sum of two array at index  3 is13
sum of two array at index  4 is16
```
2. # wap to count number of even and odd
```
#include<stdio.h>
int main()
{
    int i,a[10],even=0,odd=0;
    for(int i=0;i<10;i++)
    {
        scanf("%d",&a[i]);
        if(a[i]%2==0)
        {
            even++;
        }
        else
        {
            odd++;
        }
       
        }
         printf("total number of even numbers %d\n",even);
        printf("total number of odd numbers %d",odd);
    return 0;
}
```
Output
```
10 16 19 12 14 12 18 19 35 37
total number of even numbers 6
total number of odd numbers 4
```
