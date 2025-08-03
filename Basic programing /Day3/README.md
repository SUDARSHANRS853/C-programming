1. ## WAP to sort the given array in ascending and descending order.
```
#include <stdio.h>

int main() {
    int array[100], n, i, j, temp;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    printf("Enter %d elements:\n", n);
    for(i = 0; i < n; i++) {
        scanf("%d", &array[i]);
    }

    // Sorting in ascending order
    for(i = 0; i < n - 1; i++) {
        for(j = i + 1; j < n; j++) {
            if(array[i] > array[j]) {
                temp = array[i];
                array[i] = array[j];
                array[j] = temp;
            }
        }
    }

    printf("\nAscending order: ");
    for(i = 0; i < n; i++) {
        printf("%d ", array[i]);
    }

    // Sorting in descending order
    for(i = 0; i < n - 1; i++) {
        for(j = i + 1; j < n; j++) {
            if(array[i] < array[j]) {
                temp = array[i];
                array[i] = array[j];
                array[j] = temp;
            }
        }
    }

    printf("\nDescending order: ");
    for(i = 0; i < n; i++) {
        printf(" %d ", array[i]);
    }

    printf("\n");
    return 0;
}
```
Output
```
Enter the number of elements: 4
Enter 4 elements:
1 2 3 4

Ascending order: 1 2 3 4 
Descending order:  4  3  2  1 
```
2. ## Swapping the two numbers using function
```
#include<stdio.h>

void swap(int *a, int *b){
int temp;
temp=*a;
*a=*b;
*b=temp;
}
int main(){
int x,y;
printf("enter two numbers:");
scanf("%d%d",&x,&y);
swap(&x,&y);
printf("after swaping the numbers x=%d and y=%d\n",x,y);
return 0;
}
```
Output
```
enter two numbers x and y:4 6
after swaping the numbers x=6 and y=4
```
3. ## WAP to find minimum and maximum elements in a given array using the function int find_max_min(int array[], int size,int *max, int *min);
```
#include<stdio.h>
int find_max_min(int array[],int size ,int*max,int*min){
*max=array[0];
*min=array[0];
for(int i=1;i<size;i++){
if(array[i]>*max)
*max=array[i];
if(array[i]<*min)
*min=array[i];
}
return 0;
}
int main()
{
int arr[5]={10,5,30,2,15};
int max,min;
find_max_min(arr,5,&max,&min);
printf("max=%d\n",max);
printf("min=%d\n",min);
return 0;
}
```
Output
```
maximum and minimum numbers are:
max=30
min=2
```
4. ## WAP to store 10 numbers in an array. Remove the duplicate entries in the array.
```
#include<stdio.h>
int main()
{
    int a[10],size=10;
    printf("enter the 10 different numbers:");
    for(int i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
        
    }
   
    for(int i=0;i<size;i++)
    {
        for(int j=i+1;j<size;j++)
        {
            if(a[i]==a[j])
            {
                for(int k=j;k<size-1;k++)
                {
                    a[k]=a[k+1];
                    
                }
                size--;
                j--;
            }
        }
    }
    printf("array after removing duplications:\n");
    for(int i=0;i<size;i++)
    {
        printf("%d",a[i]);
        
    }
    return 0;
}
```
Output
```
enter the 10 different numbers:2 3 4 5 6 4 3 2 2 3
array after removing duplications:
23456
```
5. ## WAP to search for a given integer in an array using the linear search technique.
```
#include<stdio.h>
int main()
{
    int a[100],n,key,found;
    printf("enter the number of elements:\n");
    scanf("%d",&n);
    printf("enter the %d elements\n",n);
    for(int i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
    }
    printf("enter the number to search:\n");
    scanf("%d",&key);
    for(int i=0;i<n;i++)
    {
        if(a[i]==key)
        {
            printf("the entered %d number is found at position %d(index %d)",key,i+1,i);
        }
    }
}
```
Output
```
enter the number of elements:
4
enter the 4 elements
1 2 3 4
enter the number to search:
4
the entered number 4 is found at position 4(index 3)
```
6. WAP to search for a given integer in an array using the binary search technique
```
#include<stdio.h>
int main()
{
    int a[100],n,key,low,high,mid,found=0;
    printf("enter the number of elements:\n");
    scanf("%d",&n);
    printf("enter the %d elements\n",n);
    for(int i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
    }
    printf("enter the element to search\n");
    scanf("%d",&key);
    low = 0;
    high = n-1;
    // found=0;
    while(low<=high){
    mid=(low+high)/2;
    if(a[mid]==key)
    {
        printf("entered  number is %d at the position %d(index %d)",key,mid+1,mid);
        found=1;
        break;}
        else if(key<a[mid])
        {
            high=mid-1;
        }
        else
        {
            low=mid+1;
        }  
        }
        if(!found){
            printf("element %d not found in the array.\n",key);
        }
        return 0;
        }
```
Output
```
enter the number of elements:
4
enter the 4 elements
1 2 3 4
enter the element to search
4
entered  number is 4 at the position 4(index 3)
```
7. ## Write a C program, that reads list of n integer and print sum of product of consecutivenumbers. if n=7 and numbers are 4,5,2,5,6,4,7 then output is 4*5+5*2+2*5+5*6+6*4+4*7 = 122.
```
#include<stdio.h>
int main()
{
    int a[100],n,sum=0;
    printf("enter the number of elements\n");
    scanf("%d",&n);
    printf("enter the %d elements\n",n);
    for(int i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
        
    }
    for(int i=0;i<n-1;i++)
    {
       sum+=a[i]*a[i+1];
       
    }
    printf("%d", sum);
    return 0;
}
```
Output
```
enter the number of elements
6
enter the 6 elements
1 2 3 4 5 6
the sum of product of consecutive number is 70
```
8. ## WAP to read a string from the user and find the length of string.( Note: Do not usestring.h header file)
```
#include <stdio.h>

int main()
{
    char str[100];
    int length = 0;

    printf("Enter a string: ");
    scanf("%[^\n]", str);  // Reads string with spaces

    // Loop until null character '\0' is encountered
    while (str[length] != '\0')
    {
        length++;
    }

    printf("Length of the string = %d\n", length);

    return 0;
}
```
Output
```
Enter a string: Sudarshan rs gowda
Length of the string = 18
```
9. ## Input date, month and year from the user, and using switch case, display inworded format. e.g. input: d=16, m=7, y=1992 Output: 16th July, 1992
```
#include<stdio.h>
const char* getSuffix(int day){
    if(day>=11 && day<=13){
        return "th";
    }
    switch(day%10){
        case 1: return "st";
        case 2:return "nd";
        case 3: return "rd";
        default:return "th";
        
    }
}
int main()

{
    int day, month,year;
    printf("enter the day(1-31):");
    scanf("%d",&day);
    printf("enter the month(1-12):");
    scanf("%d",&month);
    printf("enter the year:");
    scanf("%d",&year);
    printf(" %d%s ",day,getSuffix(day));
    switch (month)
    {
        case 1:printf("january");break;
        case 2:printf("febraury");break;
        case 3:printf("March");break;
        case 4:printf("April");break;
        case 5:printf("May");break;
        case 6:printf("June");break;
        case 7:printf("July");break;
        case 8:printf("August");break;
        case 9:printf("September");break;
        case 10:printf("October");break;
        case 11:printf("November");break;
        case 12:printf("December");break;
        default:printf("invalid month");
        return 1;
        
    }
    printf(" %d\n",year);
    return 0;
}
```
Output
```
enter the day(1-31):4
enter the month(1-12):8
enter the year:2025
 4th August 2025
```
10. ## Write a function that will scan a character string passed as an argument and convertall lower-case characters into their upper-case equivalents.
```
#include<stdio.h>
void toUpperCase(char str[]){
    for (int i=0;str[i]!='\0';i++){
        if(str[i]>='a'&& str[i]<='z'){
            str[i]=str[i]-32;
        }
    }
}
int main(){
    char text[100];
    printf("enter a string:");
    fgets(text,sizeof(text),stdin);
    toUpperCase(text);
    printf("Uppercase string:%s\n",text);
    return 0;
}
```
Output
```
enter a string:"suDARSHAN"
Uppercase string:"SUDARSHAN"
```
11. ## Write a program to read a string from the user and reverse the string.( Note: Do not use string.h header file)
```
#include<stdio.h>
int main()
{
    char str[100],temp;
    int i,len=0;
    printf("enter the string:");
    fgets(str,sizeof(str),stdin);
    while(str[len]!='\0'){
        if(str[len]=='\n'){
            str[len]='\0';
            break;
        }
        len++;
        }
for(i=0;i<len/2;i++){
    temp=str[i];
    str[i]=str[len-1-i];
    str[len-1-i]=temp;
}
printf("reversed string:%s\n",str);
return 0;
}
```
Output
```
enter the string:sudarshn
reversed string:nhsradus
```
12. ## Write a program to check whether the given input string is palindrome.
```
#include <stdio.h>

int main() {
    char str[100];
    int len = 0, i, isPalindrome = 1;
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin); 


    while (str[len] != '\0') {
        if (str[len] == '\n') {
            str[len] = '\0';  
            break;
        }
        len++;
    }
    for (i = 0; i < len / 2; i++) {
        if (str[i] != str[len - 1 - i]) {
            isPalindrome = 0;  
            break;
        }
    }
    if (isPalindrome) {
        printf("The string is a palindrome.\n");
    } else {
        printf("The string is NOT a palindrome.\n");
    }

    return 0;
}
```
Output
```
Enter a string: nayan
The string is a palindrome.
```
13. ## Write a program to concatenate two stings. .( Note: Do not use string.h header file)
```
#include <stdio.h>

int main() {
    char str1[100], str2[50];
    int i = 0, j = 0;

    // Input two strings
    printf("Enter first string: ");
    fgets(str1, sizeof(str1), stdin);

    printf("Enter second string: ");
    fgets(str2, sizeof(str2), stdin);

    // Remove newline from str1 if present
    while (str1[i] != '\0') {
        if (str1[i] == '\n') {
            str1[i] = '\0';
            break;
        }
        i++;
    }

    // Append str2 to str1
    while (str2[j] != '\0') {
        if (str2[j] == '\n') {
            break;  // skip newline
        }
        str1[i] = str2[j];
        i++;
        j++;
    }

    // Null-terminate the result
    str1[i] = '\0';

    // Output result
    printf("Concatenated string: %s\n", str1);

    return 0;
}
```
Output
```
Enter first string: sudarshan
Enter second string: gowda
Concatenated string: sudarshangowda
```
14. ##  WAP to construct 5 * 5 matrix and display the contents. Use functions for construction and display of matrix.
```
#include <stdio.h>

#define SIZE 5  


void constructMatrix(int matrix[SIZE][SIZE]) {
    printf("Enter elements for a %dx%d matrix:\n", SIZE, SIZE);
    for (int i = 0; i < SIZE; i++) {
        for (int j = 0; j < SIZE; j++) {
            printf("Element [%d][%d]: ", i, j);
            scanf("%d", &matrix[i][j]);
        }
    }
}


void displayMatrix(int matrix[SIZE][SIZE]) {
    printf("\nMatrix content:\n");
    for (int i = 0; i < SIZE; i++) {
        for (int j = 0; j < SIZE; j++) {
            printf("%d\t", matrix[i][j]);  
        }
        printf("\n");  
    }
}

int main() {
    int matrix[SIZE][SIZE]; 
    constructMatrix(matrix);
    displayMatrix(matrix);  

    return 0;
}
```
Output
```
Enter elements for a 5x5 matrix:
Element [0][0]: 4 4
Element [0][1]: Element [0][2]: 4 4
Element [0][3]: Element [0][4]: 4 5
Element [1][0]: Element [1][1]: 5 4
Element [1][2]: Element [1][3]: 2 4
Element [1][4]: Element [2][0]: 4 7
Element [2][1]: Element [2][2]: 3 4
Element [2][3]: Element [2][4]: 2 3
Element [3][0]: Element [3][1]: 1 2
Element [3][2]: Element [3][3]: 5 7
Element [3][4]: Element [4][0]: 3 5
Element [4][1]: Element [4][2]: 2 4
Element [4][3]: Element [4][4]: 1 4

Matrix content:
4	4	4	4	4	
5	5	4	2	4	
4	7	3	4	2	
3	1	2	5	7	
3	5	2	4	1	
```
15. ## Given a matrix of size NxN, find it’s Transpose.
```
#include <stdio.h>

#define MAX 10  


void readMatrix(int matrix[MAX][MAX], int n) {
    printf("Enter elements of %dx%d matrix:\n", n, n);
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            printf("Element [%d][%d]: ", i, j);
            scanf("%d", &matrix[i][j]);
        }
    }
}

// Function to display matrix
void displayMatrix(int matrix[MAX][MAX], int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            printf("%d\t", matrix[i][j]);
        }
        printf("\n");
    }
}

// Function to find transpose
void transposeMatrix(int matrix[MAX][MAX], int trans[MAX][MAX], int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            trans[j][i] = matrix[i][j];
        }
    }
}

int main() {
    int matrix[MAX][MAX], trans[MAX][MAX];
    int n;

    printf("Enter the size of the square matrix (N): ");
    scanf("%d", &n);

    if (n > MAX || n <= 0) {
        printf("Invalid size. Please enter 1 to %d.\n", MAX);
        return 1;
    }

    readMatrix(matrix, n);

    printf("\nOriginal Matrix:\n");
    displayMatrix(matrix, n);

    transposeMatrix(matrix, trans, n);

    printf("\nTranspose of the Matrix:\n");
    displayMatrix(trans, n);

    return 0;
}
```
16. ## Given a matrix of size NxN, find it’s Transpose.
```
#include <stdio.h>

#define MAX 10  // Maximum allowed size

// Function to read NxN matrix
void readMatrix(int matrix[MAX][MAX], int n) {
    printf("Enter elements of %dx%d matrix:\n", n, n);
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            printf("Element [%d][%d]: ", i, j);
            scanf("%d", &matrix[i][j]);
        }
    }
}

// Function to display matrix
void displayMatrix(int matrix[MAX][MAX], int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            printf("%d\t", matrix[i][j]);
        }
        printf("\n");
    }
}

// Function to find transpose
void transposeMatrix(int matrix[MAX][MAX], int trans[MAX][MAX], int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            trans[j][i] = matrix[i][j];
        }
    }
}

int main() {
    int matrix[MAX][MAX], trans[MAX][MAX];
    int n;

    printf("Enter the size of the square matrix (N): ");
    scanf("%d", &n);

    if (n > MAX || n <= 0) {
        printf("Invalid size. Please enter 1 to %d.\n", MAX);
        return 1;
    }

    readMatrix(matrix, n);

    printf("\nOriginal Matrix:\n");
    displayMatrix(matrix, n);

    transposeMatrix(matrix, trans, n);

    printf("\nTranspose of the Matrix:\n");
    displayMatrix(trans, n);

    return 0;
}
```
Output
```
Enter the size of the square matrix (N): 2
Enter elements of 2x2 matrix:
Element [0][0]: 1
Element [0][1]: 2
Element [1][0]: 3
Element [1][1]: 4

Original Matrix:
1	2	
3	4	

Transpose of the Matrix:
1	3	
2	4	
```








