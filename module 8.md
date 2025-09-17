EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER

Aim:

To write a C program print the lowercase English word corresponding to the number

Algorithm:

1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
Program:

```
#include <stdio.h>
int main()
{
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);

    switch(n)
   {
        case 5:  printf("seventy one\n"); break;
        case 6:  printf("seventy two\n"); break;
        case 7:  printf("seventy three\n"); break;
        case 8:  printf("seventy four\n"); break;
        case 9:  printf("seventy five\n"); break;
        case 10: printf("seventy six\n"); break;
        case 11: printf("seventy seven\n"); break;
        case 12: printf("seventy eight\n"); break;
        case 13: printf("seventy nine\n"); break;
        default: printf("Greater than 13\n");
    }

    return 0;
}
```



Output:


<img width="257" height="85" alt="Screenshot 2025-09-17 151204" src="https://github.com/user-attachments/assets/6ea9f884-1c41-4480-8cac-1ed6ba840229" />






Result:

Thus, the program is verified successfully
 
EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .

Aim:

To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.

Algorithm:

1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:

```
#include <stdio.h>
#include <string.h>

int main()
{
    char a[50];
    int i, j, c;

    printf("Enter a string of digits: ");
    scanf("%s", a);
    for (i = 0; i <= 3; i++)
    {
        c = 0;
        for (j = 0; j < strlen(a); j++)
       {
            if (a[j] == (i + '0'))
            {
                c++;
            }
        }
        printf("%d ", c);
    }

    for (i = 4; i <= 9; i++)
    {
        printf("0 ");
    }

    return 0;
}
```


Output:

<img width="426" height="82" alt="image" src="https://github.com/user-attachments/assets/a5098e43-84d9-4bff-ae42-8fd65f76bc56" />




Result:

Thus, the program is verified successfully

EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.

Aim:

To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:

1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
Program:

```
#include <stdio.h>
#include <string.h>
#include <stdbool.h>

void swap(char *x, char *y) {
    char temp = *x;
    *x = *y;
    *y = temp;
}

void reverse(char str[], int l, int r) {
    while (l < r) {
        swap(&str[l], &str[r]);
        l++;
        r--;
    }
}

bool next_permutation(char str[], int n) {
    int i = n - 2;
    while (i >= 0 && str[i] >= str[i + 1]) {
        i--;
    }
    if (i < 0) return false;
    int j = n - 1;
    while (str[j] <= str[i]) {
        j--;
    }
    swap(&str[i], &str[j]);
    reverse(str, i + 1, n - 1);
    return true;
}

int main() {
    char str[50];
    scanf("%s", str);
    int n = strlen(str);
    for (int i = 0; i < n - 1; i++) {
        for (int j = i + 1; j < n; j++) {
            if (str[i] > str[j]) {
                swap(&str[i], &str[j]);
            }
        }
    }
    do {
        printf("%s\n", str);
    } while (next_permutation(str, n));
    return 0;
}
```




Output:

<img width="151" height="185" alt="image" src="https://github.com/user-attachments/assets/dbc013c7-b843-44a0-b346-386cc3a0145a" />



Result:

Thus, the program is verified successfully
 
EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.

Aim:

To write a C program to print a pattern of numbers from 1 to n as shown below.

Algorithm:

1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
Program:

```
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);

    int len = n * 2 - 1;

    for (int i = 0; i < len; i++) {
        for (int j = 0; j < len; j++) {
            int min = i < j ? i : j;
            if (len - i - 1 < min) min = len - i - 1;
            if (len - j - 1 < min) min = len - j - 1;
            printf("%d ", n - min);
        }
        printf("\n");
    }

    return 0;
}
```




Output:

<img width="305" height="207" alt="image" src="https://github.com/user-attachments/assets/672b4441-1a9b-4666-9ed4-0d6a19956210" />





Result:

Thus, the program is verified successfully

EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

Program:

```
#include <stdio.h>

int square() {
    int num;
    scanf("%d", &num);
    return num * num;
}

int main() {
    int result = square();
    printf("Square = %d\n", result);
    return 0;
}
```



Output:

<img width="172" height="76" alt="image" src="https://github.com/user-attachments/assets/7ec06680-b6ba-4a43-a304-11db80959b70" />





Result:

Thus, the program is verified successfully



























