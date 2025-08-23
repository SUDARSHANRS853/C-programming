```
#include<stdio.h>
int main()
{
    int a[2][5];
    for(int i=0;i<2;i++)
    {
        for(int j=0;j<5;j++)
        {
            scanf("%d",&a[i][j]);
            
        }
        
    }
    printf("elementf of an array\n");
    for(int i=0;i<2;i++)
    {
        for(int j=0;j<5;j++)
        {
            printf("%d ",a[i][j]);
            
        }
        printf("\n");
    }
    return 0;
}
```
Output
```
1 2 3 4 5 6 5 6 7 8 
elementf of an array
1 2 3 4 5 
6 5 6 7 8
```
