```
#include<stdio.h>
#define N 50
int main()
{
    int a[N][N],b[N][N],c[N][N],i,j,k,m,n,p,q,mul;
    printf("enter the number of rows and number of columns for first matrix:");
    scanf("%d%d",&m,&n);
    printf("enter the number of rows and number of columns in second matrix:");
    scanf("%d%d",&p,&q);
    printf("enter the elements of the matrix A:");
    for(i=0;i<m;i++)
    {
        for(j=0;j<n;j++)
        {
            scanf("%d",&a[i][j]);
        }
    }
    printf("Matrix A is:\n");
    for(i=0;i<m;i++)
    {
        for(j=0;j<n;j++)
        {
            printf("%d\t",a[i][j]);
        }
        printf("\n");
    }
    printf("entere the elements of matrix B:");
    for(i=0;i<p;i++)
    {
        for(j=0;j<q;j++)
        {
            scanf("%d",&b[i][j]);
        }
    }
    printf("Matrix B is:\n");
    for(i=0;i<p;i++)
    {
        for(j=0;j<q;j++)
        {
            printf("%d\t",b[i][j]);
        }
        printf("\n");
    }
    if(p!=n)
    {
        printf("Not able to multiply");
    }
    else
    {
        printf("Product of two matrix is:\n");
        for(i=0;i<m;i++)
        {
            for(j=0;j<q;j++)
            {
                mul=0;
                for(k=0;k<n;k++)
                {
                    mul=mul+a[i][k]*b[k][j];
                    
                }
                printf("%d\t",mul);
            }
            printf("\n");
        }
    }
}
```
Output
```
enter the number of rows and number of columns for first matrix:3 3 
enter the number of rows and number of columns in second matrix:3 3
enter the elements of the matrix A:1 2 3 4 5 6 7 8 9
Matrix A is:
1	2	3	
4	5	6	
7	8	9	
entere the elements of matrix B:1 2 3 4 5 6 7 8 9
Matrix B is:
1	2	3	
4	5	6	
7	8	9	
Product of two matrix is:
30	36	42	
66	81	96	
102	126	150	


=== Code Execution Successful ===
```
