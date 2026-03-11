# Advanced-C-Lab-Manual
## NAME : Iniya E
## REG NO: 212224230096
## EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

## Aim: 
To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

## Algorithm:

Declare structure eligible with age (integer) and n (character array)

Declare variable e of type eligible

Input age and name using scanf, store in e

If e.age <= 6

Print "Vaccine Eligibility: No" Else

Print "Vaccine Eligibility: Yes"

Print details (e.age, e.n)

Return 0

## Program:
```
#include <stdio.h>

struct eligible
{
    int age;
    char n[50];
};

int main()
{
    struct eligible e[10];
    int i, num;

    printf("Enter number of persons: ");
    scanf("%d", &num);

    for(i = 0; i < num; i++)
    {
        printf("\nEnter Name: ");
        scanf("%s", e[i].n);

        printf("Enter Age: ");
        scanf("%d", &e[i].age);
    }

    printf("\n--- Vaccine Eligibility ---\n");

    for(i = 0; i < num; i++)
    {
        printf("\nName: %s", e[i].n);
        printf("\nAge: %d", e[i].age);

        if(e[i].age <= 6)
        {
            printf("\nVaccine Eligibility: No\n");
        }
        else
        {
            printf("\nVaccine Eligibility: Yes\n");
        }
    }

    return 0;
}
```


## Output:

<img width="1436" height="1007" alt="Screenshot 2026-03-11 134825" src="https://github.com/user-attachments/assets/7eedc340-79ce-4205-843f-d4722b8f2403" />


## Result:
Thus, the program is verified successfully.

## EXP NO:2 C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND RETURNING A STRUCTURE FROM A FUNCTION 
## Aim:
To write a C program for passing structure as function and returning a structure from a function

## Algorithm:

Define structure numbers with members a and b.

Declare variable n of type numbers.

Prompt the user to enter values for a and b.

Input values for a and b into n using scanf.

Call the add function with n as an argument.

Print the result returned by the add function.

Return 0

## Program:
```
#include <stdio.h>

struct student
{
    int rollno;
    char name[50];
    float marks;
};

struct student getData();
void display(struct student s);

int main()
{
    struct student s1;

    s1 = getData();      // receiving structure from function
    display(s1);         // passing structure to function

    return 0;
}

struct student getData()
{
    struct student s;

    printf("Enter Roll Number: ");
    scanf("%d", &s.rollno);

    printf("Enter Name: ");
    scanf("%s", s.name);

    printf("Enter Marks: ");
    scanf("%f", &s.marks);

    return s;           // returning structure
}

void display(struct student s)
{
    printf("\nStudent Details:\n");
    printf("Roll Number: %d\n", s.rollno);
    printf("Name: %s\n", s.name);
    printf("Marks: %.2f\n", s.marks);
}
```


## Output:

<img width="1565" height="1003" alt="image" src="https://github.com/user-attachments/assets/8a84378f-688a-4da2-b150-cc6d46103864" />


## Result:
Thus, the program is verified successfully

## EXP.NO:3 C PROGRAM TO READ A FILE NAME FROM USER AND WRITE THAT FILE USING FOPEN()

## Aim: To write a C program to read a file name from user

## Algorithm:

Include the necessary header file stdio.h.

Begin the main function.

Declare a file pointer p. Declare a character array name to store the file name.

Prompt the user to enter a file name. Use scanf to input the file name into the name array.

Print a message indicating that the file with the specified name has been created successfully.

Use fopen to open a file with the name provided by the user in write mode ("w").

If successful, continue to the next step.

If unsuccessful, print an error message and exit the program with a non-zero status.

Print a message indicating that the file has been opened successfully.

Use fclose to close the file.

Print a message indicating that the file has been closed.

End the main function.

Return 0 to indicate successful program execution.

## Program:
```
#include <stdio.h>

int main()
{
    FILE *fp;
    char filename[50];
    char text[100];

    printf("Enter file name: ");
    scanf("%s", filename);

    fp = fopen(filename, "w");

    if(fp == NULL)
    {
        printf("File cannot be opened");
        return 1;
    }

    printf("Enter text to write into the file: ");
    scanf(" %[^\n]", text);

    fprintf(fp, "%s", text);

    fclose(fp);

    printf("Data written to file successfully.");

    return 0;
}
```


## Output:


<img width="1505" height="1003" alt="Screenshot 2026-03-11 135706" src="https://github.com/user-attachments/assets/4cdd9c90-90da-4ebd-a490-1ff0735efbd3" />

## Result: 
Thus, the program is verified successfully

## EXP NO:4 PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT IN TO THAT FILE 
## Aim:
To write a C program to read, a file and insert text in that file

## Algorithm:

Include the necessary header file stdio.h.

Begin the main function.

Declare a file pointer p. Declare character arrays name and text. Declare an integer variable num.

Prompt the user to enter a file name and the number of strings. Use scanf to input the file name into the name array and the number of strings into the num variable.

Use fopen to open a file with the name provided by the user in write mode ("w").

If successful, continue to the next step.

If unsuccessful, print an error message and exit the program with a non-zero status.

Print a message indicating that the file has been opened successfully.

Use a loop to input strings from the user and write them to the file using fputs.

Use fclose to close the file.

Print a message indicating that data has been added successfully.

End the main function.

Return 0 to indicate successful program execution.

## Program:
```
#include <stdio.h>

int main()
{
    FILE *fp;
    char filename[50];
    char text[200];

    printf("Enter the file name: ");
    scanf("%s", filename);

    fp = fopen(filename, "w");

    if(fp == NULL)
    {
        printf("Error opening file");
        return 1;
    }

    printf("Enter text to insert into the file: ");
    scanf(" %[^\n]", text);

    fprintf(fp, "%s", text);

    fclose(fp);

    printf("Text inserted successfully into the file.");

    return 0;
}
```

## Output:

<img width="1520" height="991" alt="image" src="https://github.com/user-attachments/assets/bb4abb1a-4461-4270-8e45-97c118031b91" />


## Result: 
Thus, the program is verified successfully

## Ex No 5 : C PROGRAM TO DISPLAY STUDENT DETAILS USING STRUCTURE

## Aim: 
The aim of this program is to dynamically allocate memory to store information about multiple subjects (name and marks), input the details for each subject, and then display the stored information. Finally, it frees the allocated memory to prevent memory leaks.

## Algorithm:
1.Input the number of subjects.

2.Read the integer value n from the user, which represents the number of subjects.

3.Dynamically allocate memory:

4.Use malloc to allocate memory for n subjects. Each subject has a name (array of characters) and marks (integer).

5.If memory allocation fails (i.e., the pointer s is NULL), display an error message and exit the program.

6.Input the details of each subject

7.Use a for loop to read the name and marks of each subject using scanf. For each subject, store the name as a string and marks as an integer in the dynamically allocated memory.

8.Display the details of each subject

9.Use another for loop to print the name and marks of each subject.

10.Free the allocated memory

11.After all operations are done, call free(s) to release the dynamically allocated memory.

12.Return from the main function

13.End the program by returning 0.

## Program:
```
#include <stdio.h>

struct student
{
    int rollno;
    char name[50];
    float marks;
};

int main()
{
    struct student s;

    printf("Enter Student Name: ");
    scanf("%s", s.name);

    printf("Enter Roll Number: ");
    scanf("%d", &s.rollno);

    printf("Enter Marks: ");
    scanf("%f", &s.marks);

    printf("\nStudent Details\n");
    printf("Name: %s\n", s.name);
    printf("Roll Number: %d\n", s.rollno);
    printf("Marks: %.2f\n", s.marks);

    return 0;
}
```


## Output:

<img width="1566" height="992" alt="image" src="https://github.com/user-attachments/assets/826d0ba9-fd56-4ab8-907f-622d0d5646f2" />


## Result:
Thus, the program is verified successfully
