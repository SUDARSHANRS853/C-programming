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
4. ## Write a program to convert temperature from Celsius to Fahrenheit 
```
#include <stdio.h>
int main()
{
    float celsius,fahrenheit;
    printf("enter the temperature in celsius");
    scanf("%f",&celsius);
    fahrenheit=(celsius*9/5)+32;
    printf("temperature in fahrenheit:%.2f\n",fahrenheit);
    return 0;
}
```
Output
```
enter the temperature in celsius35
temperature in fahrenheit:95.00
```
5. ## Check if entered number is even or odd.
```
#include<stdio.h>
int main(){
    int number;
    printf("enter an integer ");
    scanf("%d",&number);
    if(number%2==0)
    printf("entered number is even\n",number);
    else
    printf("entered number is odd\n",number);
    return 0;
}
```
Output 
```
enter an integer 18
entered number is even
```
6. ## Check if entered year is leap year or not.
```
#include<stdio.h>
int main(){
    int year;
    printf("enter the year:");
    scanf("%d",&year);
    if((year%4==0&& year%100!=0)||(year%400==0))
    printf("the year %d is leap year  \n",year);
    else
    printf("the year %d is not leap year\n",year);
    return 0;
    
}
```
Output
```
enter the year:2022
the year 2022 is not leap year
```
7. ## WAP to find power of 2^N using left shift operator.
```
#include<stdio.h>
int main()
{
    int n,result;
    printf("enter the values of N(for 2^N):");
    scanf("%d",&n);
    result=1<<n;
    printf("2^%d=%d\n",n,result);
    return 0;
    
}
```
Output 
```
enter the values of N(for 2^N):3
2^3=8
```
8. ## Check if given input is a character or integer. (Use integer input within the range 0-9).
```
#include<stdio.h>
int main()
{
    char input;
    printf("enter a single character");
    scanf("%c",&input);
    if(input>='0'&& input<='9'){
    printf("entered number %c is integer\n",input);
    }
    else if((input>='A'&&input<='Z')||(input>='a'&& input<='z')){
        printf("enter number %c is character\n",input);
    }
    else{
    printf("entered number neither character nor integer",input);
    return 0;
    }
}
```
Output
```
enter a single character:
5
entered number 5 is integer
enter a single character:
a
enter number a is character
enter a single character:
$
entered number neither character nor integer
```
9. ## Generate two random numbers and find its sum (Hint: use rand() from stdlib.h)
```
#include<stdio.h>
#include<stdlib.h>
#include<time.h>

int main(){
    int num1,num2,sum;
    srand(time(0));
    num1=rand()%100;
    num2=rand()%100;
    sum=num1+num2;
    printf("the frist number:%d\n",num1);
    printf("the second number:%d\n",num2);
    printf("the sum of two number is:%d\n",sum);
    return 0;   
}
```



