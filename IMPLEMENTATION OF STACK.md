# Exp.No:31  
## IMPLEMENTATION OF STACK

### AIM  
Write a Python program to implement stack using List and its built-in methods (append() and pop() ) in Python. Get five items from the user and save them in stack, then pop two items from stack and display the stack before and after popped.


### ALGORITHM

1. Start the program.
2. Initialize an empty list called stack.
3. Repeat 5 times (for i = 1 to 5):
4. Take input from the user.
5. Append the input to the stack using append().
6. Display "Stack before elements are popped".
7. Print the current contents of stack.
8. Repeat 2 times (for i = 1 to 2):
9. Remove the last element from the stack using pop().
10. Display "Stack after elements are popped".
11. Print the updated contents of stack.
10. End the program.


### PROGRAM

```
Reg.no: 212222060126
Name: kristipati shivani

stack = []
for i in range (5):
    a=input()
    stack.append(a)
print("Stack before elements are popped")
print(stack)
print()
for i in range(2):
    stack.pop()
print('Stack after elements are popped:')
print(stack)
```
## output
<img width="1519" height="700" alt="image" src="https://github.com/user-attachments/assets/6cf1f6f9-4922-446b-b8be-1d3f657e93a2" />

# Result
Successfully implemented a stack using Python list. Items were added using append() and removed using pop(), demonstrating LIFO (Last In First Out) behavior of stack.
