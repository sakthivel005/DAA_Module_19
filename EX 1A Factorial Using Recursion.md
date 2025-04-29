# EX 1A Factorial Using Recursion

## DATE:

## AIM:

To write a program to create a factorial of a number recursively.

## Algorithm:

1. Input a number num from the user.

2. Check if num is less than 0:

2.1. If yes, print "Factorial is not defined for negative numbers."

2.2. If no, proceed to step 4.

3. Define a function factorial(n):

3.1 If n is 0 or 1, return 1.

3.2 Else, return n * factorial(n - 1) (i.e., call the function recursively).

4. Call the factorial(num) function.

5. Print the result as "Factorial of number {num} = {result}".
   

## Program:

```
Developed by: SAKTHIVEL R
Register Number: 212222100044
```

```py
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n - 1)

# Taking user input
num = int(input())
if num < 0:
    print("Factorial is not defined for negative numbers.")
else:
    print(f"Factorial of number {num} = {factorial(num)}")
```

## Output:


![op19a](https://github.com/user-attachments/assets/d1c87fee-cb32-46c3-a1de-369a26012546)


# Result:

The program successfully created a factorial of a number using recursion. When the user provides an input number, the output displays the factorial of the number.
