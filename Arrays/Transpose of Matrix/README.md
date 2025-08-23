```
#include<stdio.h>
int main()
{
    int a[3][4],b[4][3],i,j;
    printf("enter the elements of matrix:");
    for(i=0;i<3;i++)
    {
        for(j=0;j<4;j++)
        {
            scanf("%d",&a[i][j]);
        }
      
    }
    printf("The obtained matrix is:\n");
    for(i=0;i<3;i++)
    {
        for(j=0;j<4;j++)
        {
            printf("%d\t",a[i][j]);
        }
        printf("\n");
    }
    printf("Transpose of matrix is:\n");
    for(i=0;i<4;i++)
    {
        for(j=0;j<3;j++)
        {
            b[i][j]=a[j][i];
            printf("%d\t",b[i][j]);
        }
        printf("\n");
    }
   
    return 0;
}
```
Output
```
enter the elements of matrix:1 2 3 4 5 6 7 8 11 12 13 14 
The obtained matrix is:
1	2	3	4	
5	6	7	8	
11	12	13	14	
Transpose of matrix is:
1	5	11	
2	6	12	
3	7	13	
4	8	14	


=== Code Execution Successful ===
```
