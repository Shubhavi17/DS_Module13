# Ex4 Evaluation of prefix expression

## AIM:
To write a C function to evaluate the given prefix expression using stack and print the output of the given prefix expression from the stack inside the function . 

## Algorithm
1. Start 
2. Initialize an empty stack s with a variable top for tracking the stack index.
3. Define a push() function to add an element to the stack.
4. Define a pop() function to remove and return the top element from the stack.
5. In evalprefix(), loop through the given prefix expression from right to left.
6. For each character, if it’s an operator (+, *), pop two operands from the stack, perform the operation, and push the result.
7. If it's a digit, convert it to an integer and push it onto the stack; finally, print the result after the loop ends.
8. End 

## Program:
```
/*
Program to evaluate the given prefix expression
Developed by: SHUBHAVI M
RegisterNumber: 212223040199 
*/
#include<stdio.h>
#include<string.h>
#include<ctype.h>

int s[50];
int top=0;

void push(int ch)
{
	top++;
	s[top]=ch;
}

int pop()
{
	int ch;
	ch=s[top];
	top=top-1;
	return(ch);
}

void evalprefix(char p[50])
{
   int i;
   for(i=strlen(p)-1;i>=0;i--)
   {
       if(isdigit(p[i]))
       {
           push(p[i]-'0');
       }
       else if(p[i]=='+'||p[i]=='*')
       {
           int operand1=pop();
           int operand2=pop();
           int result;
           
           if(p[i]=='+')
              result=operand1+operand2;
           else
              result=operand1*operand2;
           push(result);      
       }
   }
   printf("%d\n",pop());
}



```

## Output:

![Screenshot 2025-04-29 092301](https://github.com/user-attachments/assets/60f84f1f-54fe-49f4-b1db-454c913e0064)



## Result:
Thus, the C program to evaluate the prefix expression using stack and print the output of the given prefix expression from the stack inside the function is implemented successfully.
