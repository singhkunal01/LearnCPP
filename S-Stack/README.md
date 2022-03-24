# Table of Contents:
- [Stack](#stack)
- [Infix to postfix conversion](#infix-to-postfix-conversion)
- [Parenthesis Checker](#parenthesis-checker)

## STACK 

- A linear-data structure that follows LIFO (Last In First Out) principle.
- It is useful when we need to store data in a particular order like... function calls during recursion
- It can be implemented using Array or Linked List. (Each has its own pros and cons. Try thinking yourself)
- Implementation of the basic operations like push, pop, peek etc  provided [here](StacksWithoutSTL.cpp). 

![stack](https://user-images.githubusercontent.com/60391776/155890360-c291d4d6-1427-47f7-abb6-9246ea64e2fd.png)


## Algorithm:
1. PUSH:

if(top==MAX-1)
    std::cout<<"\nStack is full."<<std::endl;
else
    top++;
    stk[top]=num;

This will add element in Stack

2. POP:

if(top==-1)
    std::cout<<"\nStack is empty."<<std::endl;
else
    num=stk[top];
    top--;

This will remove element from Stack
        
## Properties:
Time Complexity: O(N)\
Space Complexity: O(N)

## Advantage:
It is more time efficient than Dynamic Implementation.

## Disadvantage:
In this static implementation , lots of effort are there to add or remove the value . 

Applications of stack :

1. Parenthesis Balancing
2. Infix to prefix or postfix conversion
3. To reverse a word or a string
4. _Call stack_ : To store list of functions that are either executing or waiting to be executed during runtime. ( stored in stack in memory)
5. Practical application : (<-)Back button present in a browser pushes the URLs of the visited sites on a stack.

## Infix to postfix conversion

- The conventational method of representing an arithmatic is known as infix
- Postfix expression: if the operater is placed after the operand then this notation is called postfix or reverse polish notation .
- Infix A+B
- Postfix AB+

Need of postfix Notation :
Although  this notation is not very reable by humans , but proved very useful for compiler designers in generating machine language  code for evaluating arithmetic expression .

Algorithm
```
- Time Complexity O(n) , where n is length of expression .
1. Using cpp built stack , For stack operation .
2. check each character of Infix expression one by one from left to right.
3. If the character is an operand, add to output. 
4. Else If the character is ‘(‘, push in stack. 
5. Else If the character is ‘)’, pop the stack and output the string upto character '(' .
6. Else, it is a operator , check precedence and push or pop accordingly 
      1.  If the precedence of the checked operator is greater than the precedence of the operator in the stack(or the stack is empty or the stack contains a ‘(‘ ), push it. 
      2. Else, Pop all the operators from the stack which are greater than or equal to in precedence than that of the checked operator. After doing that Push the checked operator to the stack. (If thjere is a parenthesis while popping then stop there and push the checked operator in the stack.)   
7. Repeat steps 3-6 upto the end of Infix expression. 
8. pop the remaining expression from the stack until stack is empty
9. print the result string that is the postfix notation.
```
- Its implementation is [here](InfixToPostfix.cpp)
- 
![Infix to postfix conversion](https://prepinsta.com/wp-content/uploads/2020/06/Infix-to-Posting-Conversion-in-C-using-Stacks-2048x1453.png)

- For more information about infix to postfix conversion [click here](https://prepinsta.com/data-structures/infix-to-postfix-conversion/)

## Parenthesis Checker

A parentheses is said to be balanced if each left parenthesis has its respective right parenthesis to match its pair in a well-nested format.

In computer science, valid parentheses(balanced parentheses) are a notation used to simplify expressions written in an operator-precedence parser by allowing the programmer to explicitly mark the operator precedence and associativity of a given expression. 

Note that an input string is valid if:

1.Open brackets must be closed by the same type of brackets
2.Open brackets must be closed in the correct order.

## How To check parenthesis using Stack ?
```
1. Declare stack S.
2. Now traverse the string expression using a pointer. 
    if the current pointer is at opening bracket ('(' or '{' or '[') then push it to stack S.
    else the current pointer is at closing bracket (')' or '}' or ']') then pop from the stack 
        if the popped bracket is the matching opening bracket then brackets are valid 
        else brackets are not valid.

After complete traversal, if there is some starting bracket left in the stack then "not valid"
```
![image](https://user-images.githubusercontent.com/91210199/159122082-2a5e98d2-bdd4-4f9d-9131-1d2048a5f60f.png)
 

