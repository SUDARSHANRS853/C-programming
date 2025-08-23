```
#include<stdio.h>
int main()
{
    int a[3][3],i,j,sr,sc;
    for(int i=0;i<3;i++)
    {
        for(int j=0;j<3;j++)
        {
            scanf("%d",&a[i][j]);
        }
   
    }
    for(int i=0;i<3;i++)
    {
        for(int j=0;j<3;j++)
        {
            printf("%d\t",a[i][j]);
        }
         printf("\n");
    }
    for(int i=0;i<3;i++)
    {
        sr=0,sc=0;
        for(int j=0;j<3;j++)
        {
            sr=sr+a[i][j];
            sc=sc+a[j][i];
        }
        printf("sr=%d,sc=%d",sr,sc);
        
    }
    return 0;
}
```
Output
```
1 2 3 4 5 6 7 8 11 12 13 14
1	2	3	
4	5	6	
7	8	11	
sr=6,sc=12sr=15,sc=15sr=26,sc=20

=== Code Execution Successful ===
