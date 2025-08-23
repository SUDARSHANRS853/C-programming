```
#include<stdio.h>
int main()
{
    int  a[3][4],i,j,sum=0;
    printf("enter the elements of an array");
    for(i=0;i<3;i++)
    {
        for(j=0;j<4;j++)
        {
            scanf("%d",&a[i][j]);
            
        }
    }
    for(i=0;i<3;i++)
    {
        for(j=0;j<4;j++)
        {
            printf("%d ",a[i][j]);
            sum=sum+a[i][j];
        }
    printf("sum of elements of current  row %d\n",sum);
    
    }
    printf("sum of elements of this array %d ",sum);
    return 0;
}
```
Output
```
enter the elements of an array1 2 3 4 5 6 7 8 1 2 3 4
1 2 3 4 sum of elements of current  row 10
5 6 7 8 sum of elements of current  row 36
1 2 3 4 sum of elements of current  row 46
sum of elements of this array 46 
```
