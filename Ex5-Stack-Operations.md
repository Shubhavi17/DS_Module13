# Ex5 Stack Operations
## DATE:
## AIM:
To write a C function to perform push and pop operation of the stack in the infix to postfix conversion.

## Algorithm
1. Initialize top as -1 and declare stack as a character array. 
2. To push, increment top and assign the character to stack[top].
3. To pop, check if top is -1 and return -1 if true.
4. If not, return stack[top] and decrement top. 

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: SHUBHAVI M
RegisterNumber: 212223040199
*/
#include<stdio.h>

char stack[100];
int top = -1;

void push(char x)
{
   stack[++top]=x;
}

char pop()
{
  return stack[top--];
}
```

## Output:

![Screenshot 2025-04-29 092555](https://github.com/user-attachments/assets/e8431a2d-a056-4482-9e0c-f7158c7d73f7)


## Result:
Thus the C program to perform push and pop operation of the stack in the infix to postfix conversion is implemented successfully.
