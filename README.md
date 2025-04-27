NAME: LAAVANYA.R


REG NO: 212224230135


EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim: To write a C program to display stack elements using an array. Algorithm:

Include Necessary Header Files
Declare Global Variables
Define the Display Function
Main Function (or Other Relevant Code)
Initialize the stack and top as needed.
Perform stack operations (push, pop, etc.).
Use the display function to visualize the stack's contents
Program:

```
float stack[100];
int size=3,top=-1,i;
void push (float data)
{
    if(top==size-1){
        printf("stack is full\n");
    }
    else{
        top+=1;
        stack[top]=data;
    }
}
void display()
{
     for(i=top;i>=0;i--)
    {
        printf("%.2f ",stack[i]);
    }
    if(top==-1)
    {
        printf("stack is empty\n");
    }
}
void pop ()
{
    if(top==-1)
    {
        printf("stack is empty");
    }
    else
    {
        top=top-1;
    }
}
void peek()
{
       printf("%.2f ",stack[top]);
}

```
Output:


![Screenshot 2025-04-27 192553](https://github.com/user-attachments/assets/126295f8-c810-4741-adf5-4b75502daa9b)

Result: Thus, the program to display stack elements using an array is verified successfully.

EXP NO:12 PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY. Aim: To create a C program to push the given element in to a stack using array. Algorithm:

Declare global variables for the stack size, top index, and the stack itself.
Define the push function to add a floating-point number to the stack.
Initialize the stack size, top index, and the stack itself.
Call the push function as needed.
Program:
```

int size=3,top=-1;
float stack[100];
void push (float data)
{
    if(top==size-1)
    {
        printf("stack is full\n");
    }
    else
    {
        top=top+1;
        stack[top]=data;
    }
}
```
Output:

![Screenshot 2025-04-27 192646](https://github.com/user-attachments/assets/d314858f-d0cc-4f49-8cc9-8d1b38961fc9)


Result: Thus, the program to push the given element in to a stack using array is verified successfully

EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY. Aim: To write a C program to display queue elements using array

Algorithm:

Declare global variables for the queue, rear, front, and iteration.
Define the display function to print the elements of the queue.
Initialize the queue, rear, and front as needed.
Call the display function and perform other queue operations as needed.
Program:

```
int front,rear;
char queue[100];
void display(){
    if(front==-1||front>rear){
        printf("No elements to display");
    }
    else{
        for(int i=front;i<=rear;i++){
            printf("%c\n",queue[i]);
        }
    }
}
```
Output: 

![Screenshot 2025-04-27 192721](https://github.com/user-attachments/assets/8f8754bc-9d68-4427-b19d-2164dc6b16b5)


Result: Thus, the program to display queue elements using array is verified successfully.

EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY. Aim: To write a C program to insert elements in queue using array.

Algorithm:

Declare global variables for the size, rear, front, and the queue itself.
Define the enqueue function to add a float to the queue.
Initialize the rear, front, and size of the queue as needed.
Call the enqueue function as needed.
Program:
```
int rear,front,size=3;
int queue[50];
void enqueue(int data) 
{
    if (rear<size)
    {
        if(front==-1)
        front++;
        rear++;
        queue[rear]=data;
    }
 
}
```
Output:

![Screenshot 2025-04-27 192751](https://github.com/user-attachments/assets/fcdde1f9-18b7-4ef4-9d30-75db3b867288)


Result: Thus, the program to insert elements in queue using array is verified successfully.

EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY

Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

Check if the Queue is Empty o If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
Delete the Front Element o If the queue is not empty, the element at the front index is deleted. o Increment the front pointer by 1 to remove the element and point to the next element in the queue.
Check if the Queue Becomes Empty After Deletion: o After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
End the Function.
Program:
```
int front, rear;
void dequeue()
{
    if(front==-1||front>rear){
        printf("No elements to display");
    }
    else{
        front++;
    }
}
```
Output:

![Screenshot 2025-04-27 192825](https://github.com/user-attachments/assets/8a1557a0-a2e9-4731-8f4d-70d4b9886545)


Result: Thus, the function that deletes an element from a queue implemented using an array is verified successfully.

