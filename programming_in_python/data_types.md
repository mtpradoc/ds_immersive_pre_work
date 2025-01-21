# Python's Data Types
First, it is better to start exploring "primitive data types".

![image](https://github.com/user-attachments/assets/0bca3250-f1ce-46c5-b4f1-28a489e1e9ef)

## What Do We Do With Numbers?
In Python, programmers perform equations with data by using numerical operators, which include +, - , *, /, //, %.

<img width="793" alt="image" src="https://github.com/user-attachments/assets/6d2ab97b-bf1b-401c-8706-5f27b4a17f56" />

## Booleans
The next data type is Boolean, which holds the distinguished title of "most fun data type to say out loud".

Boolean variables have one of two possible values: True or False. Appropriately, they're also often called flags, as they flag whether or not something is present.

Internally, they are stored as integers: 1 if True or 0 if False.

<img width="631" alt="image" src="https://github.com/user-attachments/assets/ac7a5f8b-3cd5-4363-8265-62327c48d604" />

## Strings
Strings are collections of letters and symbols known as "characters". They are typically used to store text for people to read.
- first_name = 'Charles'
- org_city = 'Singapore'
- diner_name = "Sandy's"

## Can We Use Numerical Operators on Strings?
The operator *+* concatenates, or combines, two strings together to make one big string.
So, 'a' + 'b' evaluates to 'ab'.
Or 'hello'*3 wil give "hellohellohello"

<img width="324" alt="image" src="https://github.com/user-attachments/assets/026806a2-28d2-4191-b14e-3eef80b9ac0b" />

## Escape Characters
*Escape characters* are characters with special meanings, and they're represented by a backslash followed by a character.
<img width="793" alt="image" src="https://github.com/user-attachments/assets/c1eafe19-0d2d-401d-bb0b-cb0629e76533" />

To write a backslash we use \\.

## None
The last of the primitive data types is *none*. This data type represents a null value, or the absence of data, and it is not interchangeable with 0. Let's see why.

Say you have a dataset that contains the names of pets at a veterinary practice, along with their weights and ages. If there is no record of a pet's weight, then this would be represented by *none*, not 0, becuase Kevin the Chihuahua doesn't weight zero pounds.

## Data Types Summary
<img width="796" alt="image" src="https://github.com/user-attachments/assets/3967b436-7f76-4240-b126-1d12d71c2ec5" />

## Data Type Conversions
To do this, use built-in functions like the following:
- float()
- int()
- str()

Let's see it in action. 
Say the data stores the number "1" as a string. To convert it to an integer, it is necessary to write:
``
int('1')
``
