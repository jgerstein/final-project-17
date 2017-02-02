# Python Quick Reference

## Mathematical Operators

Used for doing math. These are pretty standard among programming languages. Common ones include:

| symbol | meaning |
|--------|---------|
| + | addition |
| - | subtraction |
| * | multiplication |
| / | division |
| ** | exponent |
| % | remainder |

## Assignment Statements
Assign a value to a variable using ```=```. Remember that you always have the variable being assigned to on the left, and the value being assigned on the right.

```python
# Assign the value 5 to the variable x
x = 5

# Assign a list to the variable my_list
my_list = [1, 2, 3, 4, 5]

# Assign multiple things in one statement
# After this, a has the value 10, and b has the value cat
a, b = 10, 'cat'
```

You also use extended assignment operators as a shorthand for assigning a variable its own value modified by a mathematical operation

```python
# Assign the variable y its current value times 2
y *= 2
```

## User Input

You can get user input with the ```input()``` function.

```python
# Creates a prompt saying "Who are you? " at the command line and waits for user input.
# Assigns the input to the variable name
name = input('Who are you? ')

# Does the same thing, with a blank prompt (and assigning to n instead of name)
n = input()
```

## If/Else/Elif

Very common types of conditional statements. ```if``` is the simplest and is used most frequently. ```if``` can be used without ```elif``` or ```else```. ```elif``` and ```else``` can be used independently of each other, but not without ```if```.

Python will evaluate ```if``` first. If the logical test is true, the block of code associated with the ```if``` statement will run. Otherwise, it will check first for ```elif``` and will evaluate any ```elif``` statements in order. If no true ```elif``` statements were found, Python will check for an ```else``` statement and if it finds one, will run the block of code associated with it.

```python
# Simple example for an if statement
# If the value of x is 5, "That was a true statement. x is 5" will be printed
# Remember that for comparisons, you need ==, not just =
if x == 5:
    print("That was a true statement. x is 5")

```

```python
guess = input("Pick a number: ")

if guess == 42:
    print("Congratulations, you were right! 42 is the answer.")
elif guess > 42:
    print("Sorry, your guess was too high.")
else:
    print("Sorry, your guess was too low.")
```

## For Loops

For loops iterate through a sequence. Three common things you might iterate through are a string, a list, or a range()

```python
my_list = ['cat', 'dog', 'elephant', 'squid']

# print out each animal in the list
for animal in my_list:
    print(animal)
```

```python
# Print numbers from 0 to 99, with a step of 5 (i.e. 0, 5, 10, 15, 20, ... , 90, 95)
for n in range(0, 100, 5):
    print(n)
```

## Functions

Functions allow you to create reusable pieces of code. They must be *defined* before they can be *called*. Functions can have parameters, which are variables that are part of the definition. When you call the function, you provide values as *arguments*

```python
# simple function with no parameters
def say_hello():
"""prints "Hello" """
    print("Hello")

# The line below will call the say_hello() function.
say_hello() 
```

```python
# function with a single parameter
def say_hello_to(name):
"""prints "Hello [name]" """
    print("Hello %s" % name)

# The line below will call the say_hello_to() function and cause it to print "Hello Mathieson"
say_hello_to('Mathieson')
```

Many functions will *return* a value. A function that returns a value will carry out the code specified, and will then be treated as equivalent to the value it returns by the rest of the program. An example is the ```input()``` function, which returns a string: you can use it as the string it returns.

```python
def five():
"""This function will return the value 5. It's largely useless, but is an example"""
    return 5

# five() returns the value 5. You could do math with it!
# The line below will print the value 10
print(five() * 2)
```

A function can have multiple parameters. As an example, here's one that takes three values and returns their sum.

```python
def addition(a, b, c):
"""Returns the sum of its three arguments"""
    result = a + b + c
    return result

# The line below will print 42
print(addition(20, 15, 7))
```
