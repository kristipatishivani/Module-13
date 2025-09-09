# Exp.No:32  
## CONVERSION OF INFIX TO POSTFIX

### AIM  
To write a Python program to convert a given Infix expression to Postfix expression by following the precedence and associative rules. The input expression contains only Division, Subtraction, and Bitwise AND operators. A dictionary is used to set the priority for operators, and a set is used to hold the operators used in the given expression.

### ALGORITHM

1. **Start the program.**
2. **Initialize an empty stack** and an empty output string.
3. **Iterate through each character** in the infix expression:
   - If the character is **not an operator**, append it directly to the output string.
   - If the character is an **open parenthesis '('**, push it onto the stack.
   - If the character is a **close parenthesis ')'**, pop from the stack and append to the output until encountering a left parenthesis '('.
   - If the character is an **operator**, handle it based on precedence:
     - While there’s an operator at the top of the stack with higher or equal precedence, pop the stack and append those operators to the output.
     - Push the current operator onto the stack.
4. **Use a priority dictionary** to define operator precedence, ensuring higher precedence operators are placed before lower precedence ones.
5. Once the expression is fully processed, continue popping any remaining operators from the stack and append them to the output.
6. **Return the final postfix expression.**
7. **Print the result.**
8. **End the program.**


### PROGRAM

```
Reg.No: 212222060126
Name: kristipati shivani

Operators = set(['-', '*', '+','(',')']) # collection of Operators
Priority = {'-':1,'*':2,'+':3}  
 
def infixToPostfix(expression): 
    stack = [] # initialization of empty stack
    output = '' 
    
    for character in expression:
        if character not in Operators:  # if an operand append in postfix expression
            output+= character
        elif character=='(':  # else Operators push onto stack
            stack.append('(')
        elif character==')':
            while stack and stack[-1]!= '(':
                output+=stack.pop()
            stack.pop()
        else: 
            while stack and stack[-1]!='(' and Priority[character]<=Priority[stack[-1]]:
                output+=stack.pop()
            stack.append(character)
    while stack:
        output+=stack.pop()
    return output
expression = input()
print('infix notation: ',expression)
print('postfix notation: ',infixToPostfix(expression))
```

### OUTPUT
<img width="1103" height="254" alt="image" src="https://github.com/user-attachments/assets/48e94803-39a4-4a1d-a0ac-b7dc730a68b8" />

### RESULT
Successfully converted an infix expression with subtraction and multiplication into postfix notation using a dictionary for precedence and a set for operator validation.

