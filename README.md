## EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
## Aim: 
To write a C program to display stack elements using linked list.

## Algorithm:

Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.

Declare a global variable head representing the starting node of the linked list.

Define a function display to print the elements of the linked list.

Declare a pointer p and initialize it with the head of the linked list.

Use a while loop to traverse the linked list:

Print the data of the current node.

Move to the next node using the next pointer.

## Program:
```
#include <stdio.h>
#include <stdlib.h>

struct node
{
    int data;
    struct node *next;
};

struct node *top = NULL;

// Function to push element into stack
void push(int x)
{
    struct node *temp;
    temp = (struct node*)malloc(sizeof(struct node));

    temp->data = x;
    temp->next = top;
    top = temp;
}

// Function to display stack elements
void display()
{
    struct node *temp;

    if(top == NULL)
    {
        printf("Stack is empty\n");
    }
    else
    {
        temp = top;
        printf("Stack elements:\n");
        while(temp != NULL)
        {
            printf("%d\n", temp->data);
            temp = temp->next;
        }
    }
}

int main()
{
    push(10);
    push(20);
    push(30);
    push(40);

    display();

    return 0;
}
```


## Output:

<img width="1234" height="829" alt="image" src="https://github.com/user-attachments/assets/268f4a26-7773-433d-878b-76f6c0d28770" />


## Result: 
Thus, the program to display stack elements using linked list is verified successfully.

## EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST. 
## Aim: 
To write a C program to pop an element from the given stack using liked list.

## Algorithm:

Check for Empty Stack

If head is equal to NULL, Print "Stack is empty."

Else Proceed to the next step.

Set head to point to the next node in the stack.

## Program:
```
#include <stdio.h>
#include <stdlib.h>

struct node
{
    int data;
    struct node *next;
};

struct node *top = NULL;

// Function to push element
void push(int x)
{
    struct node *temp;
    temp = (struct node*)malloc(sizeof(struct node));

    temp->data = x;
    temp->next = top;
    top = temp;
}

// Function to pop element
void pop()
{
    struct node *temp;

    if(top == NULL)
    {
        printf("Stack is empty\n");
    }
    else
    {
        temp = top;
        printf("Popped element: %d\n", top->data);
        top = top->next;
        free(temp);
    }
}

// Function to display stack
void display()
{
    struct node *temp = top;

    if(top == NULL)
    {
        printf("Stack is empty\n");
    }
    else
    {
        printf("Stack elements:\n");
        while(temp != NULL)
        {
            printf("%d\n", temp->data);
            temp = temp->next;
        }
    }
}

int main()
{
    push(10);
    push(20);
    push(30);

    display();

    pop();

    printf("After pop:\n");
    display();

    return 0;
}
```


## Output:

<img width="1253" height="892" alt="image" src="https://github.com/user-attachments/assets/2a1fd39a-912e-499a-8fdd-741975f32e2c" />


## Result: 
Thus, the program to pop an element from the given stack using liked list is verified successfully.

## EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST. 
## Aim:
To write a C program to display queue elements using linked list.
## Algorithm:

Check if Queue is Empty

Display Queue Elements

Print the data of the current node pointed to by front

Update front to point to the next node.

End the display function.

## Program:
```
#include <stdio.h>
#include <stdlib.h>

struct node
{
    int data;
    struct node *next;
};

struct node *front = NULL;
struct node *rear = NULL;

// Function to insert element into queue (enqueue)
void enqueue(int x)
{
    struct node *temp;
    temp = (struct node*)malloc(sizeof(struct node));

    temp->data = x;
    temp->next = NULL;

    if(front == NULL && rear == NULL)
    {
        front = rear = temp;
    }
    else
    {
        rear->next = temp;
        rear = temp;
    }
}

// Function to display queue elements
void display()
{
    struct node *temp;

    if(front == NULL)
    {
        printf("Queue is empty\n");
    }
    else
    {
        temp = front;
        printf("Queue elements:\n");
        while(temp != NULL)
        {
            printf("%d\n", temp->data);
            temp = temp->next;
        }
    }
}

int main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);
    enqueue(40);

    display();

    return 0;
}
```


## Output:

<img width="1305" height="895" alt="image" src="https://github.com/user-attachments/assets/68b18424-b7ee-4bdc-baf5-dc79aeb1ae74" />


## Result: 
Thus, the program to display queue elements using linked list is verified successfully.

## EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

## Aim: 
To write a C program to insert elements in queue using linked list

## Algorithm:

Allocate Memory for New Node

Set Data and Next Pointer

Check if Queue is Empty

Set both front and rear to point to the new node p.

Set the next pointer of the current rear to point to the new node p.

End of Enqueue Operation

## Program:
```
#include <stdio.h>
#include <stdlib.h>

struct node
{
    int data;
    struct node *next;
};

struct node *front = NULL;
struct node *rear = NULL;

// Function to insert element into queue
void enqueue(int x)
{
    struct node *temp;
    temp = (struct node*)malloc(sizeof(struct node));

    temp->data = x;
    temp->next = NULL;

    if(front == NULL)
    {
        front = rear = temp;
    }
    else
    {
        rear->next = temp;
        rear = temp;
    }

    printf("%d inserted into queue\n", x);
}

void display()
{
    struct node *temp;

    if(front == NULL)
    {
        printf("Queue is empty\n");
    }
    else
    {
        temp = front;
        printf("Queue elements:\n");
        while(temp != NULL)
        {
            printf("%d\n", temp->data);
            temp = temp->next;
        }
    }
}

int main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);
    enqueue(40);

    display();

    return 0;
}
```


## Output:

<img width="1298" height="899" alt="image" src="https://github.com/user-attachments/assets/36e96079-8237-403b-ba37-989131302ac4" />


## Result: 
Thus, the program to insert elements in queue using linked list is verified successfully.

## EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.

## Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

## Algorithm:

Check if the queue is empty: o If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.

Access the front element: o If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

## Program:
```
#include <stdio.h>
#include <stdlib.h>

struct node
{
    int data;
    struct node *next;
};

struct node *front = NULL;
struct node *rear = NULL;

void enqueue(int x)
{
    struct node *temp;
    temp = (struct node*)malloc(sizeof(struct node));

    temp->data = x;
    temp->next = NULL;

    if(front == NULL)
        front = rear = temp;
    else
    {
        rear->next = temp;
        rear = temp;
    }
}

void peek()
{
    if(front == NULL)
        printf("Queue is empty\n");
    else
        printf("Peek element: %d\n", front->data);
}

int main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);

    peek();

    return 0;
}
```


## Output:

<img width="1206" height="871" alt="image" src="https://github.com/user-attachments/assets/2a11b8f8-bdb9-42dc-85e0-e849d4fc7e60" />


## Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.
