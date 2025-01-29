# Error Handling in Python

## Introduction
There are many different types of errors and exceptions in Python. The good news is, their names (for the most part) provide insight into the reason why the code failed to run/

Throughout the lesson, we'll cover a few of the most common errors, what each means, and how to troubleshoot each.

## Learning Objectives
By the end of this lesson, you'' be able to : 

- Troubleshoot the three most common Python programming errors.
- Determine when to use the`try-except` exception to bypass errors.
- Explain why you might use the `raise` keyword.

## How Do I know There is an Error?
First things first, before we learn about individual errors, we need to know how Python communicates with us about said errors.

It will communicate with us in whatever we're using to run our code. e.g. iPython or your terminal.

```python
In [1]: hello
---------------------------------------------------------------------------
NameError                                 Traceback (most recent call last)
<ipython-input-1-b1946ac92492> in <module>()
----> 1 hello
NameError: name 'hello' is not defined
```

## NameError

One basic type of error is a *NameError*. A *NameError* is thrown when the variable that's referred to doesn't exist in the namespace - in other words, when we try to access a variable that we haven't defined yet.

```
In [1]: hello
---------------------------------------------------------------------------
NameError                                 Traceback (most recent call last)
<ipython-input-1-b1946ac92492> in <module>()
----> 1 hello
NameError: name 'hello' is not defined
```

We can fix this by declaring a variable named *hello*, which would allow us to avoud the error:

```python
In [2]: hello = True

In [3]: hello
Out[3]: True
```

## SyntaxError
*SyntaxError* quite possibly the most common type of error.

A *SyntaxError* indicates that something you wrote doesn't follow the proper syntax of Python. A *SyntaxError* means we've mistyped something and as a result, Python doesn't understand.

For example, if we failed to place a colon after an *if* statement condition, we'd see something like this:

```python
In [4]: if hello print('hello exists')
 File "<ipython-input-4-3bd228f97f89>", line 1
  if hello print('hello exists')
               ^
SyntaxError: invalid syntax
```

Python even tries to help us troubleshoot! An arrow (^) under the offering section of code indicates where the problem occurred.

The fix? Simply put the colon in its proper place:

```python
In [6]: if hello: print ('hello exists')
hello exists
```

## TypeError
*TypeError* occurs when we try to do manipulate data types in a way that python does not permit. Like adding a tring and an integer or trying to get the length of an integer.

```python
In [7]: 12.0 + 'twelve'
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-7-0525c126347b> in <module>()
----> 1 12.0 + 'twelve'

TypeError: unsupported operand type(s) for +: 'float' and 'str'
```

The *TypeError* already tells us that the error is related to Python data types. In this case, the message is clear (although it does contain a fair amount of jargon). Basically, this error message is telling us "hey, you can't use the operand *+* with a floating and a string."

## Knowledge Check
Consider the following code:

```python
for i in 1 to 10:
  print(i)
```

Which of the following error types will occur?

Select the best answer.

[ ] TypeError

[x] SyntaxError

Correct: *1 to 10* is not a valid syntax in Python and will result in a SyntaxError.

[ ] NameError

[ ] ValueError

## Error Types Summary


| Error Name | What does it mean? | How can I fix it? |
|:-----------|:-------------------|:------------------|
| NameError | We're trying to access a variable that we haven't defined yet. | Double check the variable you're trying to access is correct. If it is, make sure you've defined that variable prior to accessing it. 
| SyntaxError | We've written something that doesn't follow the proper syntax of Python | Double check the syntax in the line(s) that Python suggests there is an error. This is indicated by the arrow (^). |
| TypeError | We're trying to do manipulate data types in a way that python does not permit. | Read the helper text Python included with the TypeError and double check what you're asking python to do. |

# Break the Shackles!
What if we want to do something throws an error in Python? We can actually write logic that tells Python what to do in the case of an error.

Exceptions are our ticket to breaking free from the handcuffs of Python errors ... a little drama goes a long way.

## For Example

In the example below, we'd want to convert the list of strings into floats.

Normally, the program would get to the *,* in *7,5* and stop running entirely with an error - Python can't convert certain characters like commas into floats.

However, we can get around this writing a function that loops through a string checking to see if each character has a comma, dollar sign, or percentage. If it is, then that character is marked as corrupted.

Then, we convert all the characters that are not corrupted to floats and add them to a list. If the character is corrupted, we add *None*. We used logic to get around the error!

```python
str_to_float = ['2.1', '2.3', '7,5', '$12.12', '8.9', '5%', '33.1']
```

```python
floats = []
bad_characters = ',$%'
for number in str_to_float:
  corrupted = False
  for bad_character in bad_characters:
    if bad_character  in number:
      corrupted = True
  if corrupted:
    floats.append(None)
  else: floats.append(float(number))
```

Once we've execured the code block, *floats* should be [2.1, 2.3, None, None, 8.9, None, 33.1].

# But What if ...

But what if instead of just seven strings like in the previous example, we had millions of different string that we wanted to convert? What if some of them had characters other than just commas, dollar signs and percentages that could break the *float* function?

It would be impossible to look through every element in a program and come up with the logic to ensure the process doesn't throw an error. And even if it were possible, our code could quickly become bloated with condition after condition that needed to be met.

## Let's Use Try-Except This Time

Luckily, we can wait for *float* to break and then take action. The basic syntax for handling exceptions uses the keywords *try* and *except*.

Here's how we can use them given the previous example:

```python
floats = []
for s in str_to_float:
  try:
    floats.append(float(s))
  except:
    floats.append(None)
```

The code above simply catches any exception that could occur in the *try* statement.

Just like before, we initialize an empty list to hold the converted numbers. Now, as we iterate through the *str_to_float* list, we use the *try* and *except* syntax to handle errors. First, *try* attempts the code inside of its block. If that code successfully runs, *except* is skipped. Alternatively, if the code in the *try* block throws an exception, the code inside of the *except* block will run instead.

There are many exceptions - see the full list - for now, we'll stick with the most common.

## Getting Specific

It may be more useful to be specific about the type of error on which you want to act.

Fortunately, we can chain multiple *except* statements together and write out the specific type of exception we want each *except* statement to target (hence the keyword *target*).

```python
try
  # Code
except TypeError as target:
  # Code to run on TypeError.
except (NameError, ValueError) as target:
  # Code to run if NameError or ValueError is thrown.
except:
  # All other exceptions.
```

Splitting the *except* statement into multiple sections delineated by error type improves the flexibility of your code in the face of uncertain errors.

## Pro Tip

As you begin to use Python packages outside of its built-in functionality, you will notice that some of them have their own custom error types and exceptions.

Like for most things in life, as you're learning Python and additional packages, Google will be your best friend.

*What does the ___ error in Python mean?*

## Raise

Exceptions let us circumvent errors in python. *Raise* lets us throw errors that wouldn't normally occur! So in a way, they're kind of opposites.

The *raise* keyword can be used to alert a user of a specific error type. As an example, we can write a function that will raise an error if *4* is entered but will otherwise print the number:

```python
def no_four(number):
  if number == 4:
    raise ValueError('No fours allowed!!')
  else:
    print('Number:', number)
```

When the error is raised, the string entered as an argument to *ValueError* is the message that's returned to the user:

```python
In [20]: no_four(4)
---------------------------------------------------------------------------
ValueError                                Traceback (most recent call last)
<ipython-input-20-a01fa7d42066> in <module>()
----> 1 no_four(4)

<ipython-input-19-7adc614ec34c> in no_four(number)
      1 def no_four(number):
      2      if number == 4:
----> 3         raise ValueError('No fours allowed!!')
      4     else:
      5         print 'Number:', number

ValueError: No fours allowed!!

In [21]: no_four(2)
Number: 2
```

## Knowledge Check

What code should be placed in the *else* statement to give a *ValueError*?

Select the best answer.

[ ] throw ValueError

[x] raise ValueError
Correct: To throw an error to a user, include the *raise* keyword followed by the error type.

[ ] return ValueError

[ ] except ValueError

## Error Handling in Python

This introduction to error handling should help you debug your own code and understand Python's error messages, and help you write your own exception logic.

We've only scratched the surface when it comes to the types of exceptions that can occur; there are many built-in types for a wide range of scenarios and problems.

For a full list of the built-in exception types and their explanations, consult the Python 3 official documentation.

Topics

Troubleshooting Common Errors

Using the Try-Except Code to Handle Errors

Raisin Errors in Your Own Code
