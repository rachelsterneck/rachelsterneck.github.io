---
title: "Intro to Python: Number Guesser Game"
---

This post introduces python fundamentals to provide the building blocks for coding a number guessing game played in the command line. In this game, the python program generates a random number, and the user guesses what the number is. If the user's guess is correct, the program will tell them that they won and quit out. Otherwise, the program will tell them whether the guess is too high or low. The code can be found [here](https://github.com/rachelsterneck/CAPEC-Information-Retrieval).

# Topics Skills:
* Data types
* Variables
* Comparison operations
* Random function
* Input/output
* Conditionals
* Loops
* Binary search (optional)

# Data Types
* In programming languages, we can think about data in terms of different categories. For example, we consider words and sentences ("hi friend!") to be different from integers (100), or even decimal numbers (1.2345)
* Some common data types are **booleans**, **integers**, and **strings**
  - **Booleans** are True or False values. They are used to represent truth values, and they're the basis of computing!
  - **Integers** are whole numbers. They can be positive or negative, but cannot be followed by a decimal point. Examples of integers include 1, 2, 5, 1000, -586003, 7575757575
  - **Strings** are sequences of characters. When using strings, we always put quotes around the word/sentence. Examples of strings include, "code", "hello world", "i love my dog"
 - [More on python data types](https://realpython.com/python-data-types/)

# Variables
* Variables are used to store data values, so we can use them later.
* Declaring a boolean variable
```
isRainingToday = False
```
* Declaring an integer variable
``` 
my_lucky_number = 15
```

* Declaring a string variable
```
my_name = "Rachel"
 ```
* Note: in some programming languages, when you define a variable, you must also declare what data type it will store. Python is dynamically typed, which means we don't have to declare what type each variable is.
* [More on python variables](https://realpython.com/python-variables/)

# Python Comparison Operators
* We can compare variables using comparison operators, including **==**, **!=**, **is**, **>**, **<**, **>=**, **<=**
* These operators return True or False values

```
"hello" == "hello" // returns True
"hello" is "hello" // returns True
"hello" is "Hello" // returns False

number1 = 5
number2 = 5
number3 = 100

number1 == number2 // returns True
number1 is number2 // returns True
number1 != number3 // returns True
number2 >= number3 // returns False
number3 > number2 // returns True
```

# Random function
* A function is a block of code that runs when it is called. You can also pass data, known as parameters, into a function.
* You can write your own functions, use python built-in functions, or even use functions that other people have written! If we want to use code that's not built-in, we must **import** the module/library (see below)
* The random function is a special function that generates a random number. For example
```
import random
print random.randint(1, 5) # returns a random number between 1 and 5
```

# Input/output
* Since this game is run through the command line, we can store user input and print back to the command line
* In the example below:
  - Input: the user is prompted to type in their name on the command line. We store their name in a **user_name** variable
  - Output: we print the variable **user_name** back to the command line
````
user_name = input("Enter your name : ") // On the command line, the user will be prompted to enter their name
print(user_name) // We store their name 
````

# Conditionals
* Conditionals allow us to add control structure to our code. We can say "run this block of code if condition x is met, otherwise run this block of code." This is why boolean values, or comparison operators are powerful - they provide the True/False values that determine whether we should run certain blocks of code
````
  x = 10 // define variable x
  y = 5 // define variable y
  
  if x>y:
    print("x is greater than y")
   else:
    print("x is not greater than y")
````
Printed output:
````
x is greater than y
````
[More on conditionals](http://www.openbookproject.net/books/bpp4awd/ch04.html)

# Loops 
* Loops allow us to run code over and over again, instead of rewriting it many times. Typically, we run loops over a specified number of times ("run this block of code 10 times"), or while a certain truth statement is met ("while number < 5")
* There are two main kinds: **for loops** and **while loops** 
* In python, for loops iterate over a sequence ( a list, tuple, dictionary, set, string), meaning it executes for each element in a particular sequence. For example:
````
  for letter in "happy":
    print("woohoo!")
````
Printed output ("woohoo!" is printed 5 times since there are 5 letters in happy):
````
  woohoo!
  woohoo!
  woohoo!
  woohoo!
  woohoo!
````
* We can also use the **range** function if we want to run a loop for a specified number of time. [Range](https://www.w3schools.com/python/ref_func_range.asp) creates a sequence of numbers that we can iterate over. For example:
````
for x in range(5, 10):
  print(x)
````
Printed output:
````
5
6
7
8
9
````
* Alternatively, we can give a **while loop** a condition, and the loop will run until the condition is met. For example
````
i = 5
while i > 0:
  print(i)
  i = i-1
````
Printed output:
````
5
4
3
2
1
````
[More on loops](http://www.openbookproject.net/books/bpp4awd/ch04.html)

# Try it yourself! 
Now that we have covered all the python fundamentals for programming a number guesser name, try coding it yourself! The game should include the following componenets:
* A variable storing a random number
* A boolean ``is_guessed`` initialized to ``False`` and a while loop checking whether or not ``is_guessed`` equals ``True`` (the value of ``is_guessed`` should be set to ``True`` when the user guesses the number)
* Logic for comparing the user inputted guess with the random number
* A way of printing to the command line whether the guess is higher or lower than the random number
* If you get stuck, check out the sample solution [here](https://github.com/rachelsterneck/number_guesser_python/blob/master/number_guesser.py)!


# Optional: Binary Search
* Is there a way we can speed up how quickly we guess the number? 
* Binary search is an efficient algorithm for searching for numbers
* [Learn more about binary search](https://www.youtube.com/watch?v=EXtkCmRXfMo)