```
#include<stdio.h>
int main()
{
    int a[3][3],b[3][3],c[3][3],d[3][3],i,j,k,sum,p1;
    printf("enter the elementd of the maatrix:\n");
    for(i=0;i<3;i++)
    {
        for(j=0;j<3;j++)
        {
            scanf("%d",&a[i][j]);
        }
    }
    printf("elements of matrix is :\n");
    for(i=0;i<3;i++)
    {
        for(j=0;j<3;j++)
        {
            printf("%d\t",a[i][j]);
        }
        printf("\n");
    }
    printf("transpose of the matrix is:\n");
    for(i=0;i<3;i++)
    {
        for(j=0;j<3;j++)
        {
           b[i][j]=a[j][i];
           printf("%d\t",b[i][j]);
        }
        printf("\n");
    }
    printf("sum of two matrix is:\n");
    for(i=0;i<3;i++)
    {
        sum=0;
        for(j=0;j<3;j++)
        {
            c[i][j]=a[i][j]+b[j][i];
            printf("%d\t",c[i][j]);
        }
        printf("\n");
    }
    printf("Product of two matrix is:\n");
    for(i=0;i<3;i++)
    {
        
        for(j=0;j<3;j++)
        {
            p1=0;
            for(k=0;k<3;k++)
            {
                p1=p1+a[i][k]*b[k][j];
                d[i][j]=p1;
            }
            printf("%d\t",d[i][j]);
        }
        printf("\n");
    }
    return 0;
    
}
```
enter the elementd of the maatrix:
1 2 3 4 5 6 7 8 9
elements of matrix is :
1	2	3	
4	5	6	
7	8	9	
transpose of the matrix is:
1	4	7	
2	5	8	
3	6	9	
sum of two matrix is:
2	4	6	
8	10	12	
14	16	18	
Product of two matrix is:
14	32	50	
32	77	122	
50	122	194	


=== Code Execution Successful ===
```
