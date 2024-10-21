# AIM

To study and implement stack functionality using arrays.

## Problem Statement

1. Write a C++ program to implement a stack.

## Theory

Stacks are a type of container adaptor that operate on a LIFO (Last In, First Out) principle. In a stack, a new element is added at one end (the top), and elements can only be removed from that same end. A stack typically uses an encapsulated object, such as a vector or deque (by default), or a list (sequential container class) as its underlying container. It provides a specific set of member functions to access and manipulate its elements.

## Program Code
```javascript
//Mukesh Rothe 23070123089
#include <iostream>
using namespace std;
#define size 5
#define ERROR -9999
class Stack{
    int top, ar[size];
    public:
    Stack()
    {
        top=-1;
        ar[0]=0;
    }
    void push(int);
    int pop();
    int peak();
    void disp();
};
void Stack::push(int num)
{
    if (top==size-1)
    {
        cout<<"STACK OVERFLOW: Stack is full"<<endl;
        return;
    }
    else
    {
        ar[++top]=num;
    }
}
int Stack::pop()
{
    int val;
    if(top==-1)
    {
        cout<<"STACK UNDERFLOW: STACK IS EMPTY"<<endl;
        return ERROR;
    }
    else{
         val=ar[top--];
         return val;
    }
}
int Stack::peak()
{
    if(top==-1)
    {
        cout<<"STACK UNDERFLOW: stack is empty"<<endl;
        return ERROR;
    }
    else
    {
        return ar[top];
    }
}
void Stack::disp()
{
    if(top==-1)
    {
       cout<<"STACK UNDERFLOW: stack is empty"<<endl;
        return ;
    }
    else
    {
        int i=0;
        while(i!=(top+1))
        {
            cout<<ar[i]<<"  ";
            i++;
        }
    }
}
int main()
{
    Stack s1;
    s1.push(7);
    s1.push(10);
    s1.push(4);
    int val=s1.pop();
    cout<<val;
    int top=s1.peak();
    cout<<top;
    s1.disp();
    return 0;
}
```

## Output

![Screenshot 2024-10-21 194734](https://github.com/user-attachments/assets/72c3e939-bbc4-4d57-aeaf-55f7bff203bf)

## Conclusion

We learned how to implement a stack in C++.
