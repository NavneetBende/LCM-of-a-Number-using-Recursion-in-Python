# LCM-of-a-Number-using-Recursion-in-Python

LCM of a Number using Recursion
On this page we will learn to create a python program to find LCM of a Number using Recursion.

LCM – Lowest common multiple of two or more number. Is Smallest number that it is completely divisible by all the numbers for which we are finding LCM. 

Example :

Input : first = 23, second = 69
Output : HCF of 23 and 69 is 69
Explanation : No other number less then 69 can be divide by both 23 and 69 completely. That’s why 69 is LCM of 23 & 69
HCF of a number in Python
Method 1 : Using Recursion
Algorithm
Start by making a function and passing both number to it as a and b
Return a multiplied divided by the value returned by another function which takes a and b
If b is equals to zero return a
Else return recursive call for the function with values b and remainder when a is divided by b respectively
Python Program to find LCM of a Number
To Learn more about Recursion   click here
Python Code
Run
def hcf(a, b):
    if b == 0:
        return a
    else:
        return hcf(b, a % b)


def lcm(a, b):
    return (a * b) // hcf(a, b)


first = 23
second = 69

print("Lcm of", first, "and", second, "is", lcm(first, second))
Output :

Lcm of 23 and 69 is 69
Method 2: Using Loop
Algorithm
Start by making a function and passing both number to it as a and b
Return a multiplied by b divided by the value returned by another function which takes a and b
If maximum between a & b is divided by minimum between a & b gives remainder zero return minimum between a & b
Iterate using for loop between range one more then half of minimum between a & b to 0 in reverse order using variable i
For each iteration check if  a divided by i and b divided by i both are equals to 0 then return i
Python Code
Run
def hcf(a, b):
    if max(a, b) % min(a, b) == 0:
        return min(a, b)
    for i in range(1 + min(a, b) // 2, 0, -1):
        if a % i == b % i == 0:
            return i


def lcm(a, b):
    return (a * b) // hcf(a, b)


first = 23
second = 69

print('LCM of', first, 'and', second, 'is', lcm(first, second))
Output :

Lcm of 23 and 69 is 69
