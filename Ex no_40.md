## Given an array of strings sorted in lexicographical order, print all of its permutations in strict lexicographical order. If two permutations look the same, only print one of them. See the 'note' below for an example.

Complete the function next_permutation which generates the permutations in the described order.

## For example, s=[ab,bc,cd]. The six permutations in correct order are:

ab bc cd
ab cd bc
bc ab cd
bc cd ab
cd ab bc
cd bc ab
Note: There may be two or more of the same string as elements of .
## For example, s=[ab,bc,cd]. Only one instance of a permutation where all elements match should be printed. In other words, if s[0]==s[1], then print either s[0]  or s[1] but not both.

A three element array having three distinct elements has six permutations as shown above. In this case, there are three matching pairs of permutations where ab and ba are switched. We only print the three visibly unique permutations:

ab ab bc
ab bc ab
bc ab ab
## Input Format

The first line of each test file contains a single integer , the length of the string array .

Each of the next  lines contains a string .

Constraints

 contains only lowercase English letters.
Output Format

Print each permutation as a list of space-separated strings on a single line.

## Sample Input 0

2
ab
cd
## Sample Output 0

ab cd
cd ab
## Sample Input 1

3
a
bc
bc
## Sample Output 1

a bc bc
bc a bc
bc bc a

## AIM:
To generate and print all unique permutations of a given array of strings in strict lexicographical order.

## Algorithm:
1. Start.
2. Read the number of strings and the strings themselves into an array.
3. Sort the array lexicographically.
4. Print the current permutation.
5. Use next_permutation() logic to generate the next lexicographical arrangement.
6. Repeat until all unique permutations are printed.
7. End.
   
## Program:
```
#include<stdio.h>
#include<string.h>
void swap(char s[][11], int i, int j) {
    char tmp[11];
    strcpy(tmp, s[i]);
    strcpy(s[i], s[j]);
    strcpy(s[j], tmp);
}
void reverse(char s[][11], int start, int end) {
    while (start < end) {
        swap(s, start++, end--);
    }
}
int next_permutation(int n, char s[][11]) {
    for (int i = n - 2; i >= 0; i--) {
        if (strcmp(s[i + 1], s[i]) > 0) {
            for (int j = n - 1; j > i; j--) {
                if (strcmp(s[j], s[i]) > 0) {
                    swap(s, i, j);
                    reverse(s, i + 1, n - 1);
                    return 1;
                }
            }
        }
    }
    return 0;
}

int main() {
    int n;
    char s[10][11];
    scanf("%d", &n);
    for (int i = 0; i < n; i++) {
        scanf("%s", s[i]);
    }
    do {
        for (int i = 0; i < n; i++) {
            printf("%s%c", s[i], i == n - 1 ? '\n' : ' ');
        }
    }
     while (next_permutation(n, s));
    return 0;
}

```
# output:
![Screenshot 2025-05-07 170822](https://github.com/user-attachments/assets/556d742d-0e6b-49af-9bba-9e5277169515)

# Result:
Thus the program was executed and the output was verified successfully.
