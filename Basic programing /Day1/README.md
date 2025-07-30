1. ## Conversion  of upper case to lower case
```
#include <stdio.h>

int main() 
{
    char ch;
    printf("enter the upper case value");
    scanf("%c",&ch);
    if(ch>='A' && ch<='Z'){
    ch=ch+('a'-'A');
    printf("lower case value %c \n",ch);}
    else{
    printf("entered number is not upper case value");
    }
    

    return 0;
}
```
Output
```
enter the upper case valueB
lower case value b 
```
2. ## Calculate the area of circle
```
#include<stdio.h>
#define pi 3.14
int main()
{
    float radius,area;
    printf("enter the radius of circle ");
    scanf("%f",&radius);
    area=pi*radius*radius ;
    printf("area of circle is %.2f\n",area);
    return 0;
}
```
Output
```
nter the radius of circle 2
area of circle is 12.56
```
3. ## Given two character inputs, find number of characters between them. For example, if input is ‘A’ and ‘E’ the output is 3.
```
#include<stdio.h>
#include<stdlib.h>
int main(){
char ch1,ch2;
int diff;
printf("enter the first character ");
scanf(" %c",&ch1);
printf("enter the second character ");
scanf(" %c",&ch2);
diff=abs(ch1-ch2)-1;
if(diff<0)
diff=0;
printf("difference between '%c' and '%c' is:%d\n ",ch1,ch2,diff);
return 0;
}
```
Output
```
enter the first character A
enter the second character B
difference between 'A' and 'B' is:0
 ```

