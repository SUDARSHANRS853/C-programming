1. ## Enter a 5 digit number and find the sum of its digits. For E.g. if int number = 12345; then sum = 15;
```
#include<stdio.h>
int main()
{
int number ,sum=0 ;
printf("enter the 5digit number");
scanf("%d",&number);
if(number<10000|| number>99999){
printf("entered number is invalid.\n");

return 1;
}
while(number!=0){
sum+=number%10;
number /=10;
}
printf("sum of digits=%d\n",sum);
return 0;
}
```
Output
```
enter the 5digit number12345
sum of digits=15
```
2. ## Write a program to reverse the number. For E.g. If int number = 12345; then the output reverse = 54321;
```
#include<stdio.h>
int main()
{
int number ,reverse=0;
printf("enter the number");
scanf("%d",&number);
while (number!=0){
reverse=reverse*10+number%10;
number/=10;
}
printf("reverse number =%d\n",reverse);
return 0;
}
```
Output
```
enter the number12345
reverse number =54321
```
3. ## WAP to check if a given number is a palindrome. For e.g. 12321, 56788765;
```
#include<stdio.h>
int main()
{
int number ,reverse=0,remainder,original;
printf("enter the  number\n");
scanf("%d",&number);
original=number;
while(number !=0)
{
remainder=number%10;
reverse =reverse*10+remainder;
number/=10;
}
if(original==reverse){
printf("%d is a palindrome number.\n",original);}
else
{
printf("%d is not a palindrome number.\n",original);
}
return 0;
}
```
Output
```
enter the  number
12344321
12344321 is a palindrome number.
```
4. ## Generate the pattern of right angle triangle using ( * )
```
#include<stdio.h>
int main()
{
    int i,j,n;
    printf("enter the number of rows");
    scanf("%d",&n);
    for(int i=0;i<=n;i++){
        for(int j=0;j<i;j++){
            printf("*");
            
        }
       
        printf("\n");
    }
    return 0;
}
```
Output
```
enter the number of rows:10

*
**
***
****
*****
******
*******
********
*********
**********
```
5. ## Generate the pattern number triangle
```
#include<stdio.h>
int main()
{
    int i,j,n;
    printf("enter the number of rows:");
    scanf(" %d",&n);
    for(i=0;i<=n;i++)
    {
        for(j=1;j<i;j++)
        {
            printf("%d",j);
            
        }
        printf("\n");
    }
    return 0;
}
```
Output
```
enter the number of rows:10


 1
 1 2
 1 2 3
 1 2 3 4
 1 2 3 4 5
 1 2 3 4 5 6
 1 2 3 4 5 6 7
 1 2 3 4 5 6 7 8
 1 2 3 4 5 6 7 8 9
```
6. ## Generate the pattern of inverted triangle
```
#include<stdio.h>
int main()
{
    int i,j,n;
    printf("enter the number of rows:");
    scanf("%d",&n);
    for(i=n;i>=1;i--)
    {
        for(j=1;j<i;j++)
        {
            printf("%d",j);
            
        }
        printf("\n");
        
    }
    return 0;
}
```
Output
```
enter the number of rows:10
123456789
12345678
1234567
123456
12345
1234
123
12
1
```

