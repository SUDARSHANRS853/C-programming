```
#include<stdio.h>
int main()
{
    int a[3][3],c[3][3];
    printf("enter the matrix elements:");
    for (int i=0;i<3;i++)
    {
        for(int j=0;j<3;j++)
        {
            scanf("%d",&a[i][j]);
        }
    }
    printf("elements of the matrix:\n");
    for (int i=0;i<3;i++)
    {
        for(int j=0;j<3;j++)
        {
            printf("%d\t",a[i][j]);
        }
        printf("\n");
    }
    printf("transpose of the matrix:\n");
    for (int i=0;i<3;i++)
    {
        for(int j=0;j<3;j++)
        {
            printf("%d\t",a[j][i]);
        }
        printf("\n");
    }
    printf("sum of these matrix:\n");
    for(int i=0;i<3;i++)
    {
        for(int j=0;j<3;j++)
        {
            c[i][j]=a[i][j]+a[j][i];
            printf("%d\t",c[i][j]);
        }
        printf("\n");
        
    }
    return 0;
}
```
Output
```
enter the matrix elements:1 2 3 4 5 6 7 8 9
elements of the matrix:
1	2	3	
4	5	6	
7	8	9	
transpose of the matrix:
1	4	7	
2	5	8	
3	6	9	
sum of these matrix:
2	6	10	
6	10	14	
10	14	18	


=== Code Execution Successful ===
```
