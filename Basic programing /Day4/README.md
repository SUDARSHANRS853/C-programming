1. ## Write a program to store and print the roll no., name, age and marks of 10 students using structures.
```
#include <stdio.h>

// Define structure for Student
struct Student {
    int roll_no;
    char name[50];
    int age;
    float marks;
};

int main() {
    struct Student students[10];  // Array of 10 students
    int i;

    // Input details for 10 students
    printf("Enter details of 10 students:\n");
    for (i = 0; i < 10; i++) {
        printf("\nStudent %d:\n", i + 1);
        
        printf("Roll Number: ");
        scanf("%d", &students[i].roll_no);

        printf("Name: ");
        scanf(" %[^\n]", students[i].name); // Reads full name with spaces

        printf("Age: ");
        scanf("%d", &students[i].age);

        printf("Marks: ");
        scanf("%f", &students[i].marks);
    }

    // Print the student details
    printf("\n--- Student Details ---\n");
    for (i = 0; i < 10; i++) {
        printf("\nStudent %d:\n", i + 1);
        printf("Roll Number: %d\n", students[i].roll_no);
        printf("Name: %s\n", students[i].name);
        printf("Age: %d\n", students[i].age);
        printf("Marks: %.2f\n", students[i].marks);
    }
```
Output
```
Enter details of 5 students:

Student 1:
Roll Number: 1
Name: s
Age: 22
Marks: 100

Student 2:
Roll Number: 2
Name: h
Age: 22
Marks: 90

Student 3:
Roll Number: 3
Name: k
Age: 22
Marks: 80

Student 4:
Roll Number: 4
Name: l
Age: 22
Marks: 80

Student 5:
Roll Number: 5
Name: w
Age: 22
Marks: 60

--- Student Details ---

Student 1:
Roll Number: 1
Name: s
Age: 22
Marks: 100.00

Student 2:
Roll Number: 2
Name: h
Age: 22
Marks: 90.00

Student 3:
Roll Number: 3
Name: k
Age: 22
Marks: 80.00

Student 4:
Roll Number: 4
Name: l
Age: 22
Marks: 80.00

Student 5:
Roll Number: 5
Name: w
Age: 22
Marks: 60.00


=== Code Execution Successful ===
```
2. ## Write a program to add, subtract and multiply two complex numbers using structures.
```
#include <stdio.h>

// Define structure for Complex Number
struct Complex {
    float real;
    float imag;
};

// Function to add two complex numbers
struct Complex add(struct Complex a, struct Complex b) {
    struct Complex result;
    result.real = a.real + b.real;
    result.imag = a.imag + b.imag;
    return result;
}

// Function to subtract two complex numbers
struct Complex subtract(struct Complex a, struct Complex b) {
    struct Complex result;
    result.real = a.real - b.real;
    result.imag = a.imag - b.imag;
    return result;
}

// Function to multiply two complex numbers
struct Complex multiply(struct Complex a, struct Complex b) {
    struct Complex result;
    result.real = a.real * b.real - a.imag * b.imag;
    result.imag = a.real * b.imag + a.imag * b.real;
    return result;
}

// Function to print a complex number
void printComplex(struct Complex c) {
    if (c.imag >= 0)
        printf("%.2f + %.2fi\n", c.real, c.imag);
    else
        printf("%.2f - %.2fi\n", c.real, -c.imag);
}

int main() {
    struct Complex num1, num2, sum, diff, prod;

    // Input
    printf("Enter first complex number (real and imaginary part): ");
    scanf("%f %f", &num1.real, &num1.imag);

    printf("Enter second complex number (real and imaginary part): ");
    scanf("%f %f", &num2.real, &num2.imag);

    // Operations
    sum = add(num1, num2);
    diff = subtract(num1, num2);
    prod = multiply(num1, num2);

    // Output
    printf("\n--- Results ---\n");
    printf("Sum = ");
    printComplex(sum);

    printf("Difference = ");
    printComplex(diff);

    printf("Product = ");
    printComplex(prod);

    return 0;
}
    return 0;
}
```
Output
```
Enter first complex number (real and imaginary part): 3 2
Enter second complex number (real and imaginary part): 4 1

--- Results ---
Sum = 7.00 + 3.00i
Difference = -1.00 + 1.00i
Product = 10.00 + 11.00i
```
