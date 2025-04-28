Name : LAAVANYA.R

Register Number : 242224230135

EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER Aim: To write a C program print the lowercase English word corresponding to the number Algorithm:

Start
Initialize an integer variable n.
Input Validation
Switch Statement cases.
Case 5: Print "seventy one"
Case 6: Print "seventy two"
Case 13: Print "seventy three"
...
Case 13: Print "seventy nine"
Default: Print "Greater than 13"
Exit the program.
Program:
```
#include <stdio.h>

int main() {
    int n;

    printf("Enter a number: ");
    scanf("%d", &n);

    switch(n) {
        case 71:
            printf("seventy one\n");
            break;
        case 72:
            printf("seventy two\n");
            break;
        case 73:
            printf("seventy three\n");
            break;
        case 74:
            printf("seventy four\n");
            break;
        case 75:
            printf("seventy five\n");
            break;
        case 76:
            printf("seventy six\n");
            break;
        case 77:
            printf("seventy seven\n");
            break;
        case 78:
            printf("seventy eight\n");
            break;
        case 79:
            printf("seventy nine\n");
            break;
        default:
            printf("Greater than 13\n");
            break;
    }

    return 0;
}
```
Output:

![Screenshot 2025-04-28 064121](https://github.com/user-attachments/assets/da5896bc-66af-4347-af33-091ca08f9b21)


Result: Thus, the program is verified successfully

EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS IN A SINGLE LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 . Aim: To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3. Algorithm:

Start
Declare char array a[50] outer loop for each digit from 0 to 3
Initialize counter c to 0
For each character in the string print count c for current digit, followed by a space
Increment h to move to the next digit
End
Program:
```
#include <stdio.h>

int main() {
    char a[50];
    int count[4] = {0};

    printf("Enter a string of digits: ");
    scanf("%s", a);

    for (int i = 0; a[i] != '\0'; i++) {
        if (a[i] >= '0' && a[i] <= '3') {
            count[a[i] - '0']++;
        }
    }

    for (int i = 0; i <= 3; i++) {
        printf("%d ", count[i]);
    }

    printf("\n");

    return 0;
}
```
Output:

![Screenshot 2025-04-28 064244](https://github.com/user-attachments/assets/aca29c56-37b4-4292-842b-531e2688c13f)


Result: Thus, the program is verified successfully

EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER. Aim: To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:

Start

Declare variables s (pointer to an array of strings) and n (number of strings)

Memory Allocation Dynamically allocate memory for s to store an array of strings

Input Read the number of strings n from the user Dynamically allocate memory for each string in s

Permutation Generation Loop

Memory Deallocation Free the memory allocated for each string in s Free the memory allocated for s

End

Program:
```
#include <stdio.h>
#include <string.h>
#include <stdlib.h>

#define MAX 10
#define LEN 100

void swap(char arr[MAX][LEN], int i, int j) {
    char temp[LEN];
    strcpy(temp, arr[i]);
    strcpy(arr[i], arr[j]);
    strcpy(arr[j], temp);
}

int next_permutation(char arr[MAX][LEN], int n) {
    int i = n - 2;
    while (i >= 0 && strcmp(arr[i], arr[i + 1]) >= 0) i--;
    if (i < 0) return 0;
    int j = n - 1;
    while (strcmp(arr[i], arr[j]) >= 0) j--;
    swap(arr, i, j);
    int left = i + 1, right = n - 1;
    while (left < right) swap(arr, left++, right--);
    return 1;
}

int cmp(const void *a, const void *b) {
    return strcmp((char *)a, (char *)b);
}

int main() {
    int n;
    scanf("%d", &n);
    char arr[MAX][LEN];
    for (int i = 0; i < n; i++) scanf("%s", arr[i]);
    qsort(arr, n, LEN, cmp);
    do {
        for (int i = 0; i < n; i++) printf("%s ", arr[i]);
        printf("\n");
    } while (next_permutation(arr, n));
    return 0;
}
```
Output:

![Screenshot 2025-04-28 064331](https://github.com/user-attachments/assets/a8608861-bc3e-41e1-a268-495555cb743d)


Result: Thus, the program is verified successfully

EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS SHOWN BELOW. Aim: To write a C program to print a pattern of numbers from 1 to n as shown below. Algorithm:

Start
Declare integer variables n, i, j, min
Read the value of n from the user
Calculate the length of the side of the square matrix: len = n * 2 - 1
Matrix Generation Loop
Calculate min as the minimum distance to the borders
End
Program:
```
#include<stdio.h>
int main()
{
    int n,len,min,i,j;
    scanf("%d",&n);
    len=2*n-1;
    for(i=0;i<len;i++)
    {
        for(j=0;j<len;j++)
        {
            if(i<j)
            min=i;
            else
            min=j;
            if(min>=len-i-1)
            min=len-i-1;
            if(min>=len-j-1)
            min=len-j-1;
            printf("%d ",n-min);
        }
        printf("\n");
    }
}
```
Output:

![Screenshot 2025-04-28 064414](https://github.com/user-attachments/assets/3400cd4f-570c-47c7-b857-e9c214297dce)


Result: Thus, the program is verified successfully

EXP NO:10 C PROGRAM TO FIND A SQUARE OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

Algorithm:

Start.
Define a function square() with no parameters. This function will return an integer value.
Inside the function: o Declare an integer variable to store the number. o Ask the user to input a number. o Calculate the square of the number (multiply the number by itself). o Return the squared value.
In the main function: o Call the square() function and display the result.
End.
Program:
```
#include <stdio.h>

int square() {
    int num;
    printf("Enter a number: ");
    scanf("%d", &num);
    return num * num;
}

int main() {
    int result = square();
    printf("The square of the number is: %d\n", result);
    return 0;
}
```
Output:

![Screenshot 2025-04-28 064534](https://github.com/user-attachments/assets/96706faa-3b6d-4db3-908a-47a1dc52acde)


Result: Thus, the program is verified successfully
