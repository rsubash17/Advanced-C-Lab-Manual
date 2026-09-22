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

int main()
{
    int stack[10], n, i;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    printf("Enter the elements:\n");
    for(i = 0; i < n; i++)
        scanf("%d", &stack[i]);

    printf("\nStack elements are:\n");
    for(i = n - 1; i >= 0; i--)
        printf("%d\n", stack[i]);

    return 0;
}
```

Output:

```
Enter the number of elements: 5
Enter the elements:
10
20
30
40
50

Stack elements are:
50
40
30
20
10
```


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

int main()
{
    int stack[MAX], top = -1;
    int element;

    printf("Enter element to push: ");
    scanf("%d", &element);

    if (top == MAX - 1)
        printf("Stack Overflow");
    else
    {
        top++;
        stack[top] = element;
        printf("%d pushed into stack\n", element);

        printf("Stack elements: ");
        for (int i = top; i >= 0; i--)
            printf("%d ", stack[i]);
    }

    return 0;
}
```


Output:
```
Enter element to push: 25
25 pushed into stack
Stack elements: 25
```




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

int main()
{
    int queue[MAX], front = 0, rear = 4;
    int i;

    printf("Enter 5 queue elements:\n");

    for(i = 0; i < MAX; i++)
        scanf("%d", &queue[i]);

    printf("Queue elements are: ");

    for(i = front; i <= rear; i++)
        printf("%d ", queue[i]);

    return 0;
}
```

Output:

```
Enter 5 queue elements:
10
20
30
40
50

Queue elements are: 10 20 30 40 50
```


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

int main()
{
    int queue[MAX], rear = -1;
    int n, i;

    printf("Enter number of elements: ");
    scanf("%d", &n);

    for(i = 0; i < n; i++)
    {
        if(rear == MAX - 1)
        {
            printf("Queue Overflow");
            break;
        }

        printf("Enter element: ");
        scanf("%d", &queue[++rear]);
    }

    printf("Queue elements are: ");
    for(i = 0; i <= rear; i++)
        printf("%d ", queue[i]);

    return 0;
}
```


Output:

```
Enter number of elements: 4
Enter element: 10
Enter element: 20
Enter element: 30
Enter element: 40

Queue elements are: 10 20 30 40
```

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

int queue[MAX], front = 0, rear = 4;

void delete()
{
    if (front > rear)
        printf("Queue Underflow");
    else
    {
        printf("Deleted element: %d\n", queue[front]);
        front++;
    }
}

int main()
{
    int i;

    printf("Enter 5 queue elements:\n");
    for(i = 0; i < MAX; i++)
        scanf("%d", &queue[i]);

    delete();

    printf("Queue after deletion: ");
    for(i = front; i <= rear; i++)
        printf("%d ", queue[i]);

    return 0;
}
```

Output:
```
Enter 5 queue elements:
10
20
30
40
50

Deleted element: 10
Queue after deletion: 20 30 40 50
```
Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
