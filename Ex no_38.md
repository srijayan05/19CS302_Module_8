## Task - Hackerrank Problem

Given a positive integer denoting , do the following:
If  41<=n <=49 print the lowercase English word corresponding to the number (e.g., forty one for 41 , forty two for 42 etc.).
If n>49 print Greater than 49.

## Sample Input
41
## Sample Output
forty one
## AIM:
To write a C program that prints the lowercase English word for numbers between 41 and 49, and prints "Greater than 49" if the number is more than 49.
## ALGORITHM:
1. Start.
2. Read an integer n from the user.
3. If 41 <= n <= 49, print "forty" and the corresponding word for the unit digit.
4. Else if n > 49, print "Greater than 49"
5. End.
## PROGRAM:
```
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);

    if (n >= 41 && n <= 49)
  {
        printf("forty ");
        switch(n)
       {
            case 41: printf("one\n"); break;
            case 42: printf("two\n"); break;
            case 43: printf("three\n"); break;
            case 44: printf("four\n"); break;
            case 45: printf("five\n"); break;
            case 46: printf("six\n"); break;
            case 47: printf("seven\n"); break;
            case 48: printf("eight\n"); break;
            case 49: printf("nine\n"); break;
        }
    }
    else if (n > 49)
    {
        printf("Greater than 49\n");
    }
    return 0;
}
```

## OUTPUT
![Screenshot 2025-05-07 170211](https://github.com/user-attachments/assets/33978d5a-990a-458e-9905-5bcfae6f7acf)


## RESULT:
Thus, the program is executed and verified successfully.
