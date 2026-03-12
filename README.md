## REG NO: 212224230096
## EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER 
## Aim:
To write a C program print the lowercase English word corresponding to the number
## Algorithm:

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

## Program:
```
#include <stdio.h>

int main() {
    int n;

    printf("Enter a number (1-10): ");
    scanf("%d", &n);

    switch(n) {
        case 1: printf("one"); break;
        case 2: printf("two"); break;
        case 3: printf("three"); break;
        case 4: printf("four"); break;
        case 5: printf("five"); break;
        case 6: printf("six"); break;
        case 7: printf("seven"); break;
        case 8: printf("eight"); break;
        case 9: printf("nine"); break;
        case 10: printf("ten"); break;
        default: printf("Number out of range");
    }

    return 0;
}
```
## Output:

<img width="1318" height="742" alt="image" src="https://github.com/user-attachments/assets/a4ced95b-72b8-4ae0-b100-2c06393c5c5e" />


## Result:
Thus, the program is verified successfully


## EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS IN A SINGLE LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 . 
## Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
## Algorithm:

Start

Declare char array a[50] outer loop for each digit from 0 to 3

Initialize counter c to 0

For each character in the string print count c for current digit, followed by a space

Increment h to move to the next digit

End

## Program:
```
#include <stdio.h>

int main() {
    char num[1000];
    int freq[10] = {0};

    printf("Enter a number: ");
    scanf("%s", num);

    for(int i = 0; num[i] != '\0'; i++) {
        if(num[i] >= '0' && num[i] <= '9') {
            freq[num[i] - '0']++;
        }
    }

    for(int i = 0; i < 10; i++) {
        printf("%d ", freq[i]);
    }

    return 0;
}
```


## Output:

<img width="1235" height="692" alt="image" src="https://github.com/user-attachments/assets/26c81914-9e16-4563-abdc-ad326ac05c2b" />


## Result: 
Thus, the program is verified successfully


## EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER. 
## Aim:
To write a C program to print all of its permutations in strict lexicographical order.

## Algorithm:

Start

Declare variables s (pointer to an array of strings) and n (number of strings)

Memory Allocation Dynamically allocate memory for s to store an array of strings

Input Read the number of strings n from the user Dynamically allocate memory for each string in s

Permutation Generation Loop

Memory Deallocation Free the memory allocated for each string in s Free the memory allocated for s

End

## Program:
```
#include <stdio.h>
#include <string.h>

void permute(char *a, int l, int r) {
    int i;
    char temp;

    if (l == r)
        printf("%s\n", a);
    else {
        for (i = l; i <= r; i++) {
            temp = a[l];
            a[l] = a[i];
            a[i] = temp;

            permute(a, l + 1, r);

            temp = a[l];
            a[l] = a[i];
            a[i] = temp;
        }
    }
}

int main() {
    char str[100];
    int n;

    printf("Enter a string: ");
    scanf("%s", str);

    n = strlen(str);
    permute(str, 0, n - 1);

    return 0;
}
```


## Output:

<img width="1321" height="904" alt="image" src="https://github.com/user-attachments/assets/0fb96863-9b47-471c-ac9f-956e74228ead" />


## Result:
Thus, the program is verified successfully

## EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS SHOWN BELOW. 
## Aim: 
To write a C program to print a pattern of numbers from 1 to n as shown below. 
## Algorithm:

Start

Declare integer variables n, i, j, min

Read the value of n from the user

Calculate the length of the side of the square matrix: len = n * 2 - 1

Matrix Generation Loop

Calculate min as the minimum distance to the borders

End

## Program:
```
#include <stdio.h>

int main() {
    int n, i, j;

    scanf("%d", &n);

    for(i = 1; i <= n; i++) {
        for(j = 1; j <= i; j++) {
            printf("%d ", j);
        }
        printf("\n");
    }

    return 0;
}
```


## Output:

<img width="1101" height="645" alt="image" src="https://github.com/user-attachments/assets/13bfce8f-ecbd-4212-a16a-e131a50ae6a8" />


## Result:
Thus, the program is verified successfully


## EXP NO:10 C PROGRAM TO FIND A SQUARE OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

## Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

## Algorithm:

Start.

Define a function square() with no parameters. This function will return an integer value.

Inside the function: o Declare an integer variable to store the number. o Ask the user to input a number. o Calculate the square of the number (multiply the number by itself). o Return the squared value.

In the main function: o Call the square() function and display the result.

End.

## Program:
```
#include <stdio.h>

int square() {
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);
    return n * n;
}

int main() {
    int result;
    result = square();
    printf("Square = %d", result);
    return 0;
}
```


## Output:

<img width="1176" height="530" alt="image" src="https://github.com/user-attachments/assets/2d4a3c2f-7c4a-46cc-87e9-832b1067a6fa" />


## Result:
Thus, the program is verified successfully
