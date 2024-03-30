# 0x19. C - Stacks, Queues - LIFO, FIFO

## Resources
1. [Difference Between Stack and Queue Data Structures](https://www.scaler.com/topics/difference-between-stack-and-queue/)
2. [Stack in Data Structure](https://www.scaler.com/topics/data-structures/stack-in-data-structure/)
3. [Stack data structure](https://www.tutorialspoint.com/data_structures_algorithms/stack_algorithm.htm)
4. [Stack in Data Structure](https://www.youtube.com/watch?v=bxRVz8zklWM&list=PLdo5W4Nhv31bbKJzrsKfMpo_grxuLl8LU&index=28)
5. [Stacks and Queues in C – Master the Concepts of LIFO & FIFO](https://data-flair.training/blogs/stacks-and-queues-in-c/#google_vignette)
6. [How To Implement a Stack in C Programming](https://www.digitalocean.com/community/tutorials/stack-in-c)
7. []()
8. []()
9. []()
10. []()

## Summary

##### A. Stacks
Linear data strcuture, uses LIFO rule, can only store elements of same type and insertion and deletion happens from one point.
Implementation of stacks using arrays
```
#include <stdio.h>
int MAXSIZE = 8;
int stack[8];
int top = -1;

/* Check if the stack is empty */
int isempty()
{
  if(top == -1)
      return (1);
  else
      return (0);
}

/* Check if the stack is full */
int isfull()
{
  if(top == MAXSIZE)
    return (1);
  else
    return (0);
}

/* Function to return the topmost element in the stack */
int peek()
{
  return stack[top];
}

/* Function to delete from the stack */
int pop()
{
  int data;
  if(!isempty())
  {
    data = stack[top];
    top = top - 1;
    return (data);
  }
  else
  {
    printf("Could not retrieve data, Stack is empty.\n");
  }
}

/* Function to insert into the stack */
int push(int data)
{
  if(!isfull())
  {
    top = top + 1;
    stack[top] = data;
  }
  else
  {
    printf("Could not insert data, Stack is full.\n");
  }
}

/* Main function */
int main()
{
  push(44);
  push(10);
  push(62);
  push(123);
  push(15);
  printf("Element at top of the stack: %d\n" ,peek());
  printf("Elements: \n");
  // print stack data
  while(!isempty())
  {
    int data = pop();
    printf("%d\n",data);
  }
  printf("Stack full: %s\n" , isfull()?"true":"false");
  printf("Stack empty: %s\n" , isempty()?"true":"false");
  return (0);
}
```
Implementation of stacks using linked lists
```
```
