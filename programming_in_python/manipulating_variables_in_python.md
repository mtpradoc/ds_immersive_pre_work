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
## Cool Things to Do With Lists

```python
>>> animal_types = ['bird', 'giraffe', 'whale']
>>> len(animal_types)
3
>>> animal_types[0]
'bird'
>>> animal_types[2]
'whale'
>>> animal_types[0] = 'cat'
>>> print(animal_types)
['cat', 'giraffe', 'whate']
```

## More Cool Things to Do With Lists: Append and Pop

There will be times when we want to do more than just learn how long a list is or which item comes third.

What if we want to add or remove items from a list? That's where our dear friends append() and pop() help out.

append() adds an item to the end of a list.

```python
animal_types = ['cat', 'giraffe', 'whale']
animal_types.append('turkey')
```

After evaluating both lines, *animal_types* now contains four elements: ['cat', 'giraffe', 'whale','turkey'].

But what if we decide we don't like turkey turkey after all?

*pop()* removes an element from a list. You can provide it the specific index to remove, or else it will default to removing the last element from the list.

```python
animal_types = ['cat', 'giraffe', 'whale', 'turkey']
animal_types.pop()
```

*animal_types* now contains the original three elements ['cat', 'giraffe', 'whale'].

## Knowledge Check
Suppose *birds == ['parrot', 'crow', 'owl']*. What is *birds[2]*?

Select the best answer.
[ ] 'parrot'
[ ] 'crow'
[ ] 'owl'
[ ] IndexError: list index out of range

## Next Up: Tuples
Tuples are similar to lists in that you can store multiple values. However, there's one huge difference: Tuples are *inmmutable* - you can't alter a tuple elemet once it's been created.

In other words , we can't do as many cool things with tuples as we can do with lists. Methods like append() and pop() won't work.

To define a new tuple, use parenthesis instead of brackets:

```python
days_of_week = ('Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday')
```

## Why Use a Tuple When We Have Lists?
Tuples are ued for information that won't change: the days of the week, the months in a year, the configuration settings of an application, the fixed options in a dropdown menu on a form, and more.

Because they're immutable, they can't accidentally be overwritten. Additionally, because tuples have fixed sizes (determined when they're assigned initial values), they're more memory-efficient than a list, which needs additional memory allocated to it.

If you won't be changing your data, a tuple may be a better choice.

## Moving On: Sets
A *set* is a collection of unordered, *unique* elements. For example, we've traveled to different places around the world. The data we're trying to capture is where we each went - the sequential order doesn't matter.

```python
my_places_traveled = {'Riyadh', 'Jeddah', 'Bahrain'}
your_places_traveled = {'Singapore', 'Riyadh'}
```

The particular order inside the set doesn't matter, as each place was either visited or not.

## But We Have Lists and Tuples. Why Set?
Lists and tuples are the bee's knees, but sets have their charm too. For one thing, computers can more efficiently check to see if an element is in a set. We call this "membership lookup". It takes a lot more energy to search lists in the same way.

Taking advantage of sets means your program runs faster and uses less memory. If you don't have duplicates and you don't need order, use a set.

To check whether an element is in a set, we use the *in* operator.

```python
'Riyadh' in my_places_traveled
True
```

## Knowledge Check
You're writing a program that provides restaurant suggestions to users based on survey results. Users are asked to indicate their preference on a variety of flavors and textures by selecting the options "Love it!," "Meh, it's OK," and "No way!"

Which complex data type should you use to store the answer options? Select the best answer.

[ ] List
[x] Tuple
[ ]

## Knowledge Check
Suppose you're implementing a spell checker. You want to test whether or not a word is contained inside a collection of known words.

Which data structure should you use to store the words? Why?

Select the best answer.

[ ] A list, becuase the words are all the same data type and have an alphabetical order.
[ ] A list, because the index of each word is important.
[x] A set, because the word order is not important for a spell checker, and checking to see if an element is in a set is more efficient than doing the same for a list.
[ ] A string, because weach word is a string and storing the words in a simpler data type is fast

## And Now, Dictionaries
Think about a dictionary in real life (not programming life). It's a bit old book - or website - with words and definitions that are paired together and easily searchable.

Dictionaries in programming work just like that. They hold *keys* (words) and *values* (their definitions). This means a term can be stored with specific attributes.

For example:
- Names could be paired with ages
- Months could be paired with the nuber of days in a month
- Book titles could be paired with authors

Let's look at how create dictionaries, as well as some common use cases.

## How Key-Value Pairs Work in Dictionaries
As with sets, a dictionary is defined using curly braces. However, each element of a dictionary consists of a *key*, followed by a *colon*, then by a *value*.

Check out this example of a dictionary that pairs book titles with their authors:

```python
book_authors = {'Moby Dick': 'Herman Melville', 'The Lorax': 'Dr. Seuss', 'The Hobbit': 'J.R.R. Tolkien'}
```

This is a container of what we call *key-value pairs*. Thus, if we asked Python how many items were in the *book_authors* dictionary using *len(book_authors)*, it would return 3, as there are three key-value pairs.

Pro-Tip: To create an empty set, use the built-in *set()* function (e.g., untasty_fruits = set()). Why? Because in Python, curly braces are used for both sets and dicitonaries. Empty braces {} indicate an empty dictionary.

## Cool Things We Can Do With Dictionaries
To make any changes to an existing dictionar, you need to work with the key. This is the sae as in a ohysical dictionary  - we use a word to look up its definition, not the other way around.

To create a new key-value pair, we would write:

```python
book_authors['Beloved'] = 'Toni Morrison'
```

If *['Beloved']* already exists as a key in our dicitonary, the above would update the value to 'Toni Morrison'.

To access the value of a particular key, we would write:

```python
book_authors['The Lorax']
```

... which would return *Dr. Seuss*.

## Review: Container Data Types
The handy chart below summarizesthe properties of the data tupes we just covered: the built-in containes available in Python.

<img width="785" alt="image" src="https://github.com/user-attachments/assets/79fee3ca-628e-40fa-844f-3994680b5ad8" />

## Knowledge Check
1. Change the starter code an empty list called *packing_list*.
2. Insert the string shirt into packing_list. Then, save packing_list to a new variable called packing_list_2.
3. Insert the string pants into packing_list_2. Also, save the result as a new variable called packing_list_3.
4. Insert the string socks into packing_list.
5. Print each list on a new line. If you’ve done this exercise correctly, their values should all be identical.

```python
packing_list = []
packing_list.append("shirt")
packing_list_2 = packing_list
packing_list_2.append("pants")
packing_list_3=packing_list_2
packing_list.append("socks")
print(packing_list)
print(packing_list_2)
print(packing_list_3)

Output
['shirt', 'pants', 'socks']
['shirt', 'pants', 'socks']
['shirt', 'pants', 'socks']
```

## Knowledge Check
Suppose we have a set containing categories of houses. How might we determine the number of unique categories?

For example:

```python
house_categories = {'Single-Family Home', 'Condo', 'Duplex'}
```

[ ] house_categories.count()
[ ] len(list(house_categories))
[ ] set(house_categories)
[x] len(house_categories)

Sets only contain unique values, so finding the number of unique items in a set is as easy as computing the length of the set.

## Knowledge Check
What would be the result of evaluating the following code?

```python
len({3,2,9,5,3,6,2}) + len([3,2,9,5,3,6,2])
```

Select the best answer.

[ ] 7
[ ] 10
[x] 12
A set does not contain duplicate values. Therefore, the set contains a total of five unique values, while the list contains a total of seven values. Sumed together, this equals 12.
[ ] 14

## Manipulating Variables in Python
We use variables to temporarily store and remember things so we can reference them later. To use a variable, we give it a name and assign a value to it using the assignment operator.

When we have multiple values we want to assign to variables, we use the more complex data types: lists, tuples, sets, and dictionaries.

<img width="786" alt="image" src="https://github.com/user-attachments/assets/30b6f1a1-c9dd-4f67-a42d-7c1fbaa70aec" />
