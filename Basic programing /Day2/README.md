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
7. ## Generate the pattern of pyramid triangle
```
#include<stdio.h>
int main()
{
    int i,j,n,space;
    printf("enter the number of rows:");
    scanf("%d",&n);
    for(i=0;i<=n;i++)
    {
        for(space=0;space<=n-i;space++)
        {
            printf(" ");
        }
        for(j=0;j<=i;j++)
        {
            printf("%d",j);
            
        }
        printf("\n");
        
        }
        return 0;
    }
}
```
Output
```
enter the number of rows:10
           
          1
         12
        123
       1234
      12345
     123456
    1234567
   12345678
  123456789
 12345678910
```
8. ## Generate the 60 degree triangle with star(*)
```
#include<stdio.h>
int main()
{
    int i,j,n,space;
    printf("enter the number of rows:");
    scanf("%d",&n);
    for(i=0;i<=n;i++)
    {
        for(space=0;space<=n-i;space++)
        {
            printf(" ");
        }
        for(j=1;j<=i;j++)
        {
            printf("* ");
            
        }
        printf("\n");
        
        }
        return 0;
    }
```
Output
```
Enter the number of rows:10
           
          * 
         * * 
        * * * 
       * * * * 
      * * * * * 
     * * * * * * 
    * * * * * * * 
   * * * * * * * * 
  * * * * * * * * * 
 * * * * * * * * * *
```
9. ## Write a C program, which will print two digit numbers whose sum of both digit isnine. e.g. 18,27,36......
```
#include<stdio.h>
int main()
{
    int i,num, digit1,digit2;
    printf("Enter two digit number whose add up to 9:\n");
    for(num=10;num<=99;num++)
    {
        digit1=num/10;
        digit2=num%10;
        if(digit1+digit2==9){
        printf(" %d",num);}
        
    }
    return 0;
}
```
Output
```
Enter two digit number whose add up to 9:
 18
 27
 36
 45
 54
 63
 72
 81
 90
```
10. ## Generate the first 'N' prime numbers. For Eg. If N=5 then 2,3,5,7,11
```
#include<stdio.h>
int main()
{
int n,count=0,num=2,i,isprime;
printf("enter the number of prime numbers to genrate: ");
scanf("%d", &n);
printf("first %d prime numbers",n);
while(count<n){
isprime=1;
for(i=2;i*i<=num;i++){
if(num%i==0){
isprime=0;
break;
}
}
if(isprime){
printf("%d ",num);
count++;
}
num++;
}
return 0;
}
```
Output
```
enter the number of prime numbers to genrate: 10
first 10 prime numbers2 3 5 7 11 13 17 19 23 29
```
11. ## Generate the  prime numbers with in range of 100 ,(0-100)
```
#include<stdio.h>
int main()
{
int i,j,isprime,n;
printf("enter the value of n:");
scanf("%d",&n);
printf("prime numbers up to%d are:\n",n);
for(i=2;i<=n;i++){
isprime=1;
for(j=2;j*j<=i;j++){
if(i%j==0){
isprime=0;
break;
}
}
if(isprime)
printf("%d ",i);
}
return 0;
}
```
Output
```
enter the value of n:100
prime numbers up to100 are:
2 3 5 7 11 13 17 19 23 29 31 37 41 43 47 53 59 61 67 71 73 79 83 89 97
```
12.  ## enter the number1232132 enter the digit to count2 digit 2 occurs 3 times in 1232132. 
```
#include<stdio.h>
int main(){
int number,digit,count=0,remainder;
printf("enter the number");
scanf("%d",&number);
printf("enter the digit to count");
scanf("%d",&digit);
int temp=number;
while(temp>0){
remainder=temp%10;
if(remainder==digit){
count++;
}
temp/=10;
}
printf("digit %d occurs %d times in %d. \n",digit,count,number);
return 0;
}
```
Output
```
enter the number1232132
enter the digit to count2
digit 2 occurs 3 times in 1232132.
```
13. ## Write a C program to display and find the sum of the series 1+11+111+....111 up to n.For eg. if n=4, the series is:1+11+111+1111. Take the value of 'n' as input from the user
```
#include<stdio.h>
int main()
{
int n, i;
long sum=0,term=0;
printf("enter the number of terms:");
scanf("%d", &n);
printf("the series is: ");
for(i=1;i<=n;i++){
term=term*10+1;
printf("%1d", term);
sum +=term;
if(i!=n)
printf(" + ");
}
printf("\nsum of series is %1d\n",sum);
return 0;
}
```
Output
```
enter the number of terms:5
the series is: 1 + 11 + 111 + 1111 + 11111
sum of series is 12345
```
14. ## A number is called an Armstrong number if the sum of the cubes of the digits of the number is equal to the number. For example 153 = 1^3 + 5^3 + 3^3. Write a C program that asks the user to enter a number and returns if it is Armstrong or not.
```
#include<stdio.h>
int main()
{
int num,originalNum,remainder,result=0;
printf("enter the number ");
scanf("%d",&num);
originalNum=num;
while(num!=0){
remainder=num%10;
result+=remainder*remainder*remainder;
num/=10;
}
if(result==originalNum)
printf("%d is an Armstrong number.\n",originalNum);
else
printf("%d is not an Armstrong number.\n",originalNum);

return 0;
}
```
Output
```
enter the number 153
153 is an Armstrong number.
enter the number 1234
1234 is not an Armstrong number.
```
15. ## Amicable numbers are found in pairs. A given pair of numbers is Amicable if the sumof the proper divisors (not including itself) of one number is equal to the other numberand vice – versa.For example 220 & 284 are amicable numbers. First we find the proper divisors of220:220:1, 2, 4, 5, 10, 11, 20, 22, 44, 55, 110; 1+ 2 + 4 + 5 + 10 + 11 + 20 + 22 + 44 + 55+ 110 = 284Now, 284: 1, 2, 4, 71, 142; 1 + 2 + 4 + 71 + 142 = 220Write a C program to check that the input pair of numbers is amicable
```
#include <stdio.h>

// Function to calculate the sum of proper divisors of a number
int sumOfProperDivisors(int num) {
    int sum = 0;
    for (int i = 1; i <= num / 2; i++) {
        if (num % i == 0)
            sum += i;
    }
    return sum;
}

int main() {
    int num1, num2;

    // Taking input from the user
    printf("Enter first number: ");
    scanf("%d", &num1);

    printf("Enter second number: ");
    scanf("%d", &num2);

    // Calculating the sum of proper divisors
    int sum1 = sumOfProperDivisors(num1);
    int sum2 = sumOfProperDivisors(num2);

    // Checking if the numbers are amicable
    if (sum1 == num2 && sum2 == num1) {
        printf("%d and %d are Amicable Numbers.\n", num1, num2);
    } else {
        printf("%d and %d are NOT Amicable Numbers.\n", num1, num2);
    }

    return 0;
}
```
Output
```
Enter first number: 220
Enter second number: 284
220 and 284 are Amicable Numbers.
```
16. ## Write a menu driven program to read two integers & find their sum, difference & product.
```
#include <stdio.h>

int main() {
    int num1, num2, choice;
    int result;

    // Input two integers
    printf("Enter the first number: ");
    scanf("%d", &num1);

    printf("Enter the second number: ");
    scanf("%d", &num2);

    // Displaying menu
    printf("\n--- MENU ---\n");
    printf("1. Sum\n");
    printf("2. Difference\n");
    printf("3. Product\n");
    printf("Enter your choice (1-3): ");
    scanf("%d", &choice);

    // Switch case to perform selected operation
    switch (choice) {
        case 1:
            result = num1 + num2;
            printf("Sum = %d\n", result);
            break;

        case 2:
            result = num1 - num2;
            printf("Difference = %d\n", result);
            break;

        case 3:
            result = num1 * num2;
            printf("Product = %d\n", result);
            break;

        default:
            printf("Invalid choice! Please enter 1, 2 or 3.\n");
    }

    return 0;
}
```
Output
```
Enter the first number: 345
Enter the second number: 345

--- MENU ---
1. Sum
2. Difference
3. Product
Enter your choice (1-3): 1
Sum = 690
```
17. ## Write a C program to calculate the volume of the following shapes: Cube, Cuboid,Sphere, Cylinder and Cone. Ask the user which one s/he wants to calculate, and takethe appropriate required inputs. Then print the result. The input should be taken in themain function and calculations for every solid should be done in a separate function by passing appropriate arguments.Example: If the user chooses the option for cube, only one input is required i.e., theside. The volume is then calculated and printed.If the user chooses the option for cuboid, only three inputs are required i.e., length,breadth and height. The volume is then calculated and printed.
```
#include <stdio.h>
#define PI 3.14159

// Function to calculate volume of a cube
float volumeCube(float side) {
    return side * side * side;
}

// Function to calculate volume of a cuboid
float volumeCuboid(float length, float breadth, float height) {
    return length * breadth * height;
}

// Function to calculate volume of a sphere
float volumeSphere(float radius) {
    return (4.0 / 3.0) * PI * radius * radius * radius;
}

// Function to calculate volume of a cylinder
float volumeCylinder(float radius, float height) {
    return PI * radius * radius * height;
}

// Function to calculate volume of a cone
float volumeCone(float radius, float height) {
    return (1.0 / 3.0) * PI * radius * radius * height;
}

int main() {
    int choice;
    float side, length, breadth, height, radius;

    // Display Menu
    printf("Select the shape to calculate volume:\n");
    printf("1. Cube\n");
    printf("2. Cuboid\n");
    printf("3. Sphere\n");
    printf("4. Cylinder\n");
    printf("5. Cone\n");
    printf("Enter your choice (1-5): ");
    scanf("%d", &choice);

    switch (choice) {
        case 1:
            // Cube
            printf("Enter the side of the cube: ");
            scanf("%f", &side);
            printf("Volume of Cube = %.2f\n", volumeCube(side));
            break;

        case 2:
            // Cuboid
            printf("Enter length, breadth, and height of the cuboid: ");
            scanf("%f %f %f", &length, &breadth, &height);
            printf("Volume of Cuboid = %.2f\n", volumeCuboid(length, breadth, height));
            break;

        case 3:
            // Sphere
            printf("Enter the radius of the sphere: ");
            scanf("%f", &radius);
            printf("Volume of Sphere = %.2f\n", volumeSphere(radius));
            break;

        case 4:
            // Cylinder
            printf("Enter the radius and height of the cylinder: ");
            scanf("%f %f", &radius, &height);
            printf("Volume of Cylinder = %.2f\n", volumeCylinder(radius, height));
            break;

        case 5:
            // Cone
            printf("Enter the radius and height of the cone: ");
            scanf("%f %f", &radius, &height);
            printf("Volume of Cone = %.2f\n", volumeCone(radius, height));
            break;

        default:
            printf("Invalid choice! Please enter a number between 1 and 5.\n");
    }

    return 0;
}
```
Output
```
Select the shape to calculate volume:
1. Cube
2. Cuboid
3. Sphere
4. Cylinder
5. Cone
Enter your choice (1-5): 1
Enter the side of the cube: 3
Volume of Cube = 27.00
```
18. ## . An Electricity board charges the following rates for use of electricity. For the First 200 units : Rs 5 per unitFor the next 100 units : Rs7 per unit Beyond 300 units : Rs 10 Per unit.Write a C Program to read no of units consumed and print out total charge amount.
```
#include <stdio.h>

int main() {
    int units;
    float total = 0;

    // Input: number of units
    printf("Enter the number of units consumed: ");
    scanf("%d", &units);

    // Calculate bill based on slabs
    if (units <= 200) {
        total = units * 5;
    } else if (units <= 300) {
        total = (200 * 5) + ((units - 200) * 7);
    } else {
        total = (200 * 5) + (100 * 7) + ((units - 300) * 10);
    }

    // Output total charge
    printf("Total charge for %d units is: ₹%.2f\n", units, total);

    return 0;
}
```
Output
```
Enter the number of units consumed: 120
Total charge for 120 units is: ₹600.00
```
19. ## WAP to convert a binary number to decimal and vice versa.
```
#include <stdio.h>
#include <math.h>

// Function to convert binary to decimal
int binaryToDecimal(long long binary) {
    int decimal = 0, base = 1, rem;
    
    while (binary > 0) {
        rem = binary % 10;
        decimal += rem * base;
        binary /= 10;
        base *= 2;
    }
    return decimal;
}

// Function to convert decimal to binary
long long decimalToBinary(int decimal) {
    long long binary = 0;
    int rem, base = 1;

    while (decimal > 0) {
        rem = decimal % 2;
        binary += rem * base;
        decimal /= 2;
        base *= 10;
    }
    return binary;
}

int main() {
    int choice;
    long long binary;
    int decimal;

    printf("Menu:\n");
    printf("1. Binary to Decimal\n");
    printf("2. Decimal to Binary\n");
    printf("Enter your choice (1 or 2): ");
    scanf("%d", &choice);

    switch (choice) {
        case 1:
            printf("Enter a binary number: ");
            scanf("%lld", &binary);
            printf("Decimal equivalent: %d\n", binaryToDecimal(binary));
            break;

        case 2:
            printf("Enter a decimal number: ");
            scanf("%d", &decimal);
            printf("Binary equivalent: %lld\n", decimalToBinary(decimal));
            break;

        default:
            printf("Invalid choice!\n");
    }

    return 0;
}
```
Output
```
Menu:
1. Binary to Decimal
2. Decimal to Binary
Enter your choice (1 or 2): 1
Enter a binary number: 1010
Decimal equivalent: 10
```
20. ## Generate a sequence of numbers such that every number in the sequence is the sum ofthe previous three numbers. The first three numbers are 0,0,1.
```
#include <stdio.h>

int main() {
    int n;
    long long a = 0, b = 0, c = 1, next;

    // Get number of terms from user
    printf("Enter the number of terms to generate: ");
    scanf("%d", &n);

    // Check if at least 3 terms are needed
    if (n < 1) {
        printf("Please enter a positive number.\n");
        return 0;
    }

    printf("Sequence: ");

    for (int i = 1; i <= n; i++) {
        if (i == 1) {
            printf("%lld ", a);
        } else if (i == 2) {
            printf("%lld ", b);
        } else if (i == 3) {
            printf("%lld ", c);
        } else {
            next = a + b + c;
            printf("%lld ", next);
            a = b;
            b = c;
            c = next;
        }
    }

    printf("\n");
    return 0;
}
```
Output
```
Enter the number of terms to generate: 10
Sequence: 0 0 1 1 2 4 7 13 24 44 
```





