## Hackerrank problem - 2

Your task is to take two numbers of int data type, two numbers of float data type as input and output their sum:
Declare 4 variables: two of type int and two of type float.
Read 2 lines of input from stdin (according to the sequence given in the 'Input Format' section below) and initialize your variables.
Use the + and - operator to perform the following operations:
Print the sum and difference of two int variable on a new line.
Print the sum and difference of two float variable rounded to one decimal place on a new line.

## AIM:
To write a C program to find the sum and difference of two integers and two float numbers entered by the user.
## ALGORITHM:
1. Start.
2. Declare two int and two float variables.
3. Read two integers from the user.
4. Read two float numbers from the user.
5. Calculate and print the sum and difference of the integers.
6. Calculate and print the sum and difference of the floats.
7. End.
## PROGRAM:
```
#include <stdio.h>
int main()
{
    int a, b;
    float x, y;
    printf("Enter two integers: ");
    scanf("%d %d", &a, &b);
    printf("Enter two floats: ");
    scanf("%f %f", &x, &y);
    printf("%d %d\n", a + b, a - b);
    printf("%.1f %.1f\n", x + y, x - y);
    return 0;
}
```
## OUTPUT:
![Screenshot 2025-05-07 164549](https://github.com/user-attachments/assets/2e2af757-bc2a-4f45-a06b-c3def8a4236d)

## RESULT:
Thus, the program is executed and verified successfully.
