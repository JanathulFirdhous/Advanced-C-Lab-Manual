

EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display stack elements using linked list.

Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
Program:

//type your code here
#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node* next;
};

struct Node* head = NULL;

void display() {
    struct Node* p = head;
    if (p == NULL) {
        printf("Stack is empty.\n");
        return;
    }
    while (p != NULL) {
        printf("%d ", p->data);
        p = p->next;
    }
    printf("\n");
}

int main() {
    struct Node* newNode;

   
    newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = 10;
    newNode->next = head;
    head = newNode;

    newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = 20;
    newNode->next = head;
    head = newNode;

    newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = 30;
    newNode->next = head;
    head = newNode;

    printf("Stack elements: ");
    display();

    return 0;
}

Output:

//paste your output here
<img width="272" alt="image" src="https://github.com/user-attachments/assets/d5605afa-e283-4419-a28b-ed6667109652" />


Result:
Thus, the program to display stack elements using linked list is verified successfully. 



EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING 
LINKED LIST.
Aim:
To write a C program to pop an element from the given stack using liked list.

Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
Program:

//type your code here
#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node* next;
};

struct Node* head = NULL;

void pop() {
    if (head == NULL) {
        printf("Stack is empty.\n");
        return;
    }

    struct Node* temp = head;
    head = head->next;
    printf("Popped element: %d\n", temp->data);
    free(temp);
}

int main() {
    struct Node* newNode;

    
    newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = 10;
    newNode->next = head;
    head = newNode;

    newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = 20;
    newNode->next = head;
    head = newNode;

    newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = 30;
    newNode->next = head;
    head = newNode;

    pop();
    pop();
    pop();
    pop();

    return 0;
}

Output:

//paste your output here

<img width="254" alt="image" src="https://github.com/user-attachments/assets/c8b338cc-fdd7-46a1-b916-bbce41d92d19" />


Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display queue elements using linked list.
Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
Program:

//type your code here
#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node* next;
};

struct Node* front = NULL;
struct Node* rear = NULL;

void display() {
    if (front == NULL) {
        printf("Queue is empty.\n");
        return;
    }

    struct Node* temp = front;
    while (temp != NULL) {
        printf("%d ", temp->data);
        temp = temp->next;
    }
    printf("\n");
}

int main() {
    struct Node* newNode;

    // Adding elements to queue
    newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = 10;
    newNode->next = NULL;
    if (rear == NULL) {
        front = rear = newNode;
    } else {
        rear->next = newNode;
        rear = newNode;
    }

    newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = 20;
    newNode->next = NULL;
    rear->next = newNode;
    rear = newNode;

    newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = 30;
    newNode->next = NULL;
    rear->next = newNode;
    rear = newNode;

    printf("Queue elements: ");
    display();

    return 0;
}

Output:

//paste your output here
<img width="244" alt="image" src="https://github.com/user-attachments/assets/42ec9234-f6d9-41a6-900e-fc1a26c06b68" />

Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim:
To write a C program to insert elements in queue using linked list

Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
Program:

//type your code here
#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node* next;
};

struct Node* front = NULL;
struct Node* rear = NULL;

void enqueue(int value) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = value;
    newNode->next = NULL;

    if (rear == NULL) {
        front = rear = newNode;
    } else {
        rear->next = newNode;
        rear = newNode;
    }

    printf("%d enqueued to the queue.\n", value);
}

int main() {
    enqueue(10);
    enqueue(20);
    enqueue(30);

    
    struct Node* temp = front;
    printf("Queue elements: ");
    while (temp != NULL) {
        printf("%d ", temp->data);
        temp = temp->next;
    }
    printf("\n");

    return 0;
}

Output:

//paste your output here
<img width="248" alt="image" src="https://github.com/user-attachments/assets/8fcd8835-611c-4c9d-aa74-add0c1a2a709" />

Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:

//type your code here
#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node* next;
};

struct Node* front = NULL;
struct Node* rear = NULL;

int peek() {
    if (front == NULL) {
        printf("Queue is empty.\n");
        return -1; 
        }
    return front->data;
}

void enqueue(int value) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = value;
    newNode->next = NULL;

    if (rear == NULL) {
        front = rear = newNode;
    } else {
        rear->next = newNode;
        rear = newNode;
    }
}

int main() {
    enqueue(10);
    enqueue(20);
    enqueue(30);

    printf("Peek of the queue: %d\n", peek());

    return 0;
}

Output:

//paste your output here

<img width="247" alt="image" src="https://github.com/user-attachments/assets/ab9b2307-2757-450d-a62d-5168e3ef4dbb" />


Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


