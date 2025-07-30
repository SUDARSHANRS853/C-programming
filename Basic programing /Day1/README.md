# Conversion  of upper case to lower case
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
