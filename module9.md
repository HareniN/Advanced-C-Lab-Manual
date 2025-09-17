EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:

To write a C program to display stack elements using an array.

Algorithm:

1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:

```
#include <stdio.h>
#define MAX 5

int stack[MAX];
int top = -1;

void push(int x) {
    if (top == MAX - 1) {
        printf("Stack Overflow\n");
    } else {
        stack[++top] = x;
        printf("%d pushed to stack\n", x);
    }
}

void pop() {
    if (top == -1) {
        printf("Stack Underflow\n");
    } else {
        printf("%d popped from stack\n", stack[top--]);
    }
}

void display() {
    if (top == -1) {
        printf("Stack is empty\n");
    } else {
        printf("Stack elements: ");
        for (int i = top; i >= 0; i--) {
            printf("%d ", stack[i]);
        }
        printf("\n");
    }
}

int main() {
    push(10);
    push(20);
    push(30);
    display();
    pop();
    display();
    return 0;
}

```
Output:

<img width="336" height="161" alt="image" src="https://github.com/user-attachments/assets/96d4872f-f008-4ef1-a64e-4e9be584d7f6" />


Result:

Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.

Aim:

To create a C program to push the given element in to a stack using array.

Algorithm:

1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:

```
#include <stdio.h>
#define MAX 5   

float stack[MAX];
int top = -1;

void push(float x) {
    if (top == MAX - 1) {
        printf("Stack Overflow\n");
    } else {
        stack[++top] = x;
        printf("%.2f pushed into stack\n", x);
    }
}

int main() {
    push(10.5);
    push(20.3);
    push(30.9);
    push(40.0);
    push(50.1);
    push(60.2); 
    return 0;
}
```

Output:

<img width="322" height="140" alt="image" src="https://github.com/user-attachments/assets/75706165-72c2-4488-a8b1-f48a1b13fe14" />



Result:

Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.

Aim:

To write a C program to display queue elements using array

Algorithm:

1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:

```
#include <stdio.h>
#define MAX 5

int queue[MAX];
int front = -1, rear = -1;

void enqueue(int x) {
    if (rear == MAX - 1) {
        printf("Queue Overflow\n");
    } else {
        if (front == -1) front = 0;
        queue[++rear] = x;
        printf("%d enqueued into queue\n", x);
    }
}

void dequeue() {
    if (front == -1 || front > rear) {
        printf("Queue Underflow\n");
    } else {
        printf("%d dequeued from queue\n", queue[front++]);
    }
}

void display() {
    if (front == -1 || front > rear) {
        printf("Queue is empty\n");
    } else {
        printf("Queue elements: ");
        for (int i = front; i <= rear; i++) {
            printf("%d ", queue[i]);
        }
        printf("\n");
    }
}

int main() {
    enqueue(10);
    enqueue(20);
    enqueue(30);
    display();
    dequeue();
    display();
    return 0;
}
```

Output:

<img width="305" height="147" alt="image" src="https://github.com/user-attachments/assets/bd5a9ad4-3f54-4d8f-923a-b8543d084a38" />



Result:

Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.

Aim:

To write a C program to insert elements in queue using array.

Algorithm:

1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:

```
#include <stdio.h>
#define MAX 5

float queue[MAX];
int front = -1, rear = -1;

void enqueue(float x) {
    if (rear == MAX - 1) {
        printf("Queue Overflow\n");
    } else {
        if (front == -1) front = 0;
        queue[++rear] = x;
        printf("%.2f inserted into queue\n", x);
    }
}

int main() {
    enqueue(10.5);
    enqueue(20.3);
    enqueue(30.9);
    enqueue(40.0);
    enqueue(50.7);
    enqueue(60.1);  
    return 0;
}
```

Output:

<img width="355" height="146" alt="image" src="https://github.com/user-attachments/assets/8614ce00-3c8a-48da-b623-ede32a8ff032" />


Result:

Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY

Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:

```
#include <stdio.h>
#define MAX 5

int queue[MAX];
int front = -1, rear = -1;

void enqueue(int x) {
    if (rear == MAX - 1) {
        printf("Queue Overflow\n");
    } else {
        if (front == -1) front = 0;
        queue[++rear] = x;
        printf("%d inserted into queue\n", x);
    }
}

void dequeue() {
    if (front == -1) {
        printf("Queue is empty\n");
    } else {
        printf("%d deleted from queue\n", queue[front]);
        front++;
        if (front > rear) {
            front = rear = -1;
        }
    }
}

void display() {
    if (front == -1) {
        printf("Queue is empty\n");
    } else {
        printf("Queue elements: ");
        for (int i = front; i <= rear; i++) {
            printf("%d ", queue[i]);
        }
        printf("\n");
    }
}

int main() {
    enqueue(10);
    enqueue(20);
    enqueue(30);
    display();
    dequeue();
    display();
    dequeue();
    dequeue();
    dequeue(); // Deleting from empty queue
    return 0;
}
```


Output:

<img width="310" height="152" alt="image" src="https://github.com/user-attachments/assets/bab1e9da-80c8-45c5-b1db-1c7ca30a46f5" />


Result:

Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
