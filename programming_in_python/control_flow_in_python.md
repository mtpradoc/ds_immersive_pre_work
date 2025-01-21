## Control Flow in Python

### How Do Computers Know Which Decisions to Make?
To tell the computer how to "decide" what to do, we use *comparison* statements. Comparison statements always boil down to a single boolean value: *true* or *false*.

To write these statements in programming, we use what are called *comparison operators*.
<img width="784" alt="image" src="https://github.com/user-attachments/assets/86ecaab3-3924-4d52-a806-2f93b570c31e" />

## Conditional Statements
The real power in comparisons lies in their use in *conditional statements* to control what, when, and how things happen in your program.

<img width="576" alt="image" src="https://github.com/user-attachments/assets/d1f7bae2-3032-4811-9096-1541283304e8" />

## Writing Conditional Statements in Python

Every *if* statement ust beign the line with *if*, followed by *any expression*, followed by *a colon*, then oen or more intended lines of code:

<img width="791" alt="image" src="https://github.com/user-attachments/assets/6cd7670b-846d-4dd9-954d-8df7c88bc70e" />

We evaluate the indented lines of code only if the expression (converted to a *bool*) is *True*. You can thingk of this as, "if the expression is *True*, then evaluate the indented code."

NOTE: According to PEP8, lines hsould be indented using four spaces.

## A weather-Related Example
Example: If the chance of rain is greater than 50 percent, then I'll wear a raincoat.

```python
if chance_of_rain > 0.5:      #if <expression>:
    print("wear a raincoat")  # <indented line of code>
```
This code is evaluated line by line, from top to bottom. If chance_of_rain > 0.5 evaluates to True, then the indented lines will run. If the statement is False, we skip the indented lines of code.

## Combining Conditional Statements
Conditional statements are powerful, but we can dial up the power by combining conditional statements using *logical operators*.

<img width="786" alt="image" src="https://github.com/user-attachments/assets/e10fcce0-3bbc-4618-8533-b1af1281eadd" />

## The else Condition
Sometimes, we want to evaluate one block of code if the expression is True and another block of code it it's False.

This is called an if-else statement:
<img width="782" alt="image" src="https://github.com/user-attachments/assets/105c7217-6449-4373-9a35-a1b0690b549c" />

## Back to our Weather-Related Example
```python
if chance_of_rain > 0.5:      # if <expression>
    print("wear a raincoat")  # <indented line of code>
else:
  print("wear a cardigan")    # the else statement
```
If chance_of_rain > 0.5 evaluates to True, then the first indented line will run. If the statement is False, we skip the first indented line and evaluate the second line of indented code.

## Conditions on Conditions on Conditions
f you need a conditional to check for more than two possibilities, you can add more comparisons to create an if ... else if ... else chain, as shown below. This is called an elif statement.

*elif* statements tell Python, "if something is True, do this, if not, check the next condition in the chain."
The first conditional that turns out to be true is executed, and the rest of the chain is skipped entirely.
<img width="783" alt="image" src="https://github.com/user-attachments/assets/74c54f92-d837-4806-9750-07f166780e0c" />

## These Can Get Long
elif statements always have one if, as many elifs as you want, and ero to one else.

Recall that in an elif chain, once the computer finds a true condition, it skips the rest of the chain.

```python
if grade >= 90:
    print("You got an A.")
elif grade >= 80:
    print("You got a B.")
elif grade >= 70:
    print("You got a C.")
elif grade >= 60:
    print("You got a D.")
else:
  print("You failed, sorry".)
```

## Introducing Loops
Whenever you want a program to repeat a conditional process, you can create a loop. A loop will continue to execute as long as certain codition is met.

We'll cover two kinds of loops: for loops and while loops. They both get the job done, there are certain situations that make the most sense for each kind.

## The for Loop
*for* loops are generally used when you want a process to repeat *for* a fixed number of times.

The *for* loop always requires the following structure:
<img width="791" alt="image" src="https://github.com/user-attachments/assets/81d2dfbd-ce7a-48dc-b63f-8fd67171302f" />

- The *variable_name* can be anything as long as it isn't another one of your variables names.
- The *colleciton* is any element that can be iterated over. For example, lists, strings, tuples, dictionaries (the keys), and sets (in no particular order).

Reminder: Notice how a colon always indicates that at least the next line of code will be indented.

## for Loop Example
In this example, we're asking Python to sum the integers in the list:

```python
total = 0                    # Line 1

for num in [0,1,2,3,4,5]:    # Line 2
  total += num               # Line 3

print(total)                 # Line 4
```

Pro Tip: Python's built-in sum() function accomplishes the same objective as the for loop above.

## Knowledge Check
Let's look at one more example of a for loop.

```python
primes = [2,3,5]              # Line 1

for prime_number in primes:   # Line 3
    print(prime_number)       # Line 4

print('Done!')
```

## Home on the range() Function
What if we wanted to sum a list of 100 integers?
We use a python built-in function range().

```python
total = 0

for num in range(6):  # the easy way
    total += num

print(total)
```

## More range()
The range() function takes three arguments: range([start,] stop [,step]). The only required argument is the stopping value.

Something like this as an example range(5, 15, 2)

## The while Loop
Let's meet the simpler, cleaner cousin of the *for* loop: the *while* loop.

A *while* loop is generally used in Python when we don't know when the looping will sotp or how many iterations the loop will require.

<img width="784" alt="image" src="https://github.com/user-attachments/assets/18bd647d-990e-4a05-beb9-023385f19733" />

That's right, there's just one part of a *while* loop: the conditional. As long as the conditional is true, the loop will keep going forever, and ever, and ever ...

## Playing With User Input
Let's make *while* statements even more fun.

Meet input(), another exciting built-in Python function.

Example:
```python
name = input('What is your name?')
```

## The while Loop With User Input
Here's an example of the *while* loop in action:

```python
print('Type "yes" to continue.')      # Line 1

while input('Do you want to quit the loop?') != 'yes':    # Line 2: While the user does not enter 'yes', repeat.
  print('Please type 'yes' so we can exit this loop.')    # Line 3

print('Thank you for typing "yes."')
```

## knowledge Check
Which of the following would be a good use of the *while* loop when we don't know the number of iterations in advance?

[x] Loop while less than 33 miliseconds have elapsed, then continue.
[x] Loop while we have not received the entire downloaded file
[x] Loop a new random number between 0 and 1 is greater than 0.9
[ ] Loop through each element of a Python list.

## Knowledge Check
```python
counter = 0

while counter < 10:
    print('counter is currently', counter)
    counter += 1

print("We're out of the loop. The value of counter is", counter)
```

## Knowledge Check

What is stored in *x* after evaluating the following code?

```python
x = 1

while x < 10:
    x = x * 2
```

In each iteration, *x* is doubled, and we only exit the *while* loop if *x* is at least *10*. Therefore, when we exit the loop, *x* will equal 16.


## Control Flow in Python
We can write more advanced programs by asking the computer to make decisions.

We're basically communicating with computers when we write conditional statements and loops. "Hey, if this conditions is met, do this. If not, do this other thing."

<img width="790" alt="image" src="https://github.com/user-attachments/assets/87051738-76f9-4464-8275-de8954618f04" />

### *if* Statement
```
if <expression>:
    <indented line of code>
```

### *if* With an *else* Clause
```
if <expression>:
    <indented line of code>
else
    <indented line of code>
```

### *for* Loop
```
for <variable name> in <sequence>:
  <indented line of code>
      ...
```

### *while* Loop
```
while <variable_name> condition:
    <indented line of code>
```
