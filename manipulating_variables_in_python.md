# Manipulating Variables in Python

## Learning Objectives

- Declare and use variables in Python.
- Define lists, tuples, sets, and variables along with their common methods.
- Distinguish between the complex data types.

## Variables: What Are They and Why Do We Care?
In Python, a *variable* gives you a way to label and remember different data values for quicker, neater programming.

Creating a variable in Python - which is simple to do, by the way - is like making these announcements to your computer:

```python
print(num_students)
14
print(teacher_pet)
'hamster'
```

## How Do Create a Variable in Python
In Python, you don't have to isue a command to create a variable. You just need to equals sign (the *assignment operator*). The equal sign assigns the value to each variable.

<img width="789" alt="image" src="https://github.com/user-attachments/assets/708d6d31-d0d8-4273-a694-5a99928a0990" />

## To the Right, to the Right

When building variables, Python always evaluates the data on the *right-hand side*  of the equal symbo and associates the name on the *left-hand side* withe the result.

```
num_cookies = 3
```

It's crucial when want to do something, such as:
```
num_cookies = 3
num_cookies = num_cookies + 1
```

## Wait, but Why? Using Variables in Python
Now that we've declared a variable, we can use it as many times as we want wherever we want in a given program. We could use num_cookies in line 7 of our program and again in line 301, and it will produce the same value we asigned it at the start.

## Hark! A Quick Tip on Naming Your Variables
Use prefixes, without prefixes, variables names like appt and blue aren't particular clear. Adding preixes has_apt and is_blue - make it clear that the value options are either True or False.

## Knowledge Check
Create variables
```python
volume = 3.2
greeting = "hello"
is_learning = True
```

## But What If You Have a Lot of Similar Data Types
Suppose we have three different types of animals that each need their own variable. Based on what we currently know, we'd need to create these separate variables:

```
variable_type1 = 'bird'
variable_type2 = 'giraffe'
variable_type3 = 'whale'
```
What if we needed a variable for every type of animal on Earth?

Python's complex data types help us solve this problem
<img width="358" alt="image" src="https://github.com/user-attachments/assets/d4ca4aba-0fac-467d-ba29-d77e8c1550b5" />

## Features of Lists
First on our list is ... lists!

Lists are:
- Ordered: Their elements have a particular order that will never change.
- Heterogeneous: Different data types can be stored for each element in the list. For example, ['cat', 10, 0.4].
- Mutable: When you alter a list, you don't create a new element - the original element is just modified.

We can tell Python we're creating a list by wrapping the items in square brackets:

```python
animal_types = ['bird', 'giraffe', 'whale']
```

