# Python Basics

## Presentation and code

Presentations available at: https://karuga.eu/courses-presentations

Code available at: https://github.com/marko-knoebl/courses-code

## Your Trainer

Marko Knöbl

- Frontend Web-Development
  - JavaScript
  - React, Angular
- Programming
  - Python, JavaScript

## Introduction of Participants

- Name
- Company
- Current Projects
- Prior Knowledge
- Expectations

## Organizational

- Duration
- Breaks
- Materials
- Questions, Feedback?

# Python: Overview

## Python

- dynamic programming language
- simple syntax, relatively easy to learn
- useful in many areas (science, web development, GUI programming)
- big standard library, many additional packages

## Python development and versions

- Python 3.7 (current)
- Python 3.2 (first useful version of Python 3): 2011
- Python 2.7 (last version of Python 2): 2010, supported until 2020

## Code examples

```py
# this is a comment

a = 3
b = 4
print(a * b)

if a * b > 10:
    print('hello')
```

# Python Installation

## Python Installation

on Windows: Download from https://python.org (Windows x86-64 web-based installer)

check the option "Add Python 3.7 to PATH"

<!--
Python zu path hinzufügen

program "environment variables" / "Umgebungsvariablen für dieses Konto bearbeiten"
zu PATH hinzufügen:

für Anaconda:
C:\Users\Marko\Anaconda3
C:\Users\Marko\Anaconda3\Scripts
-->

## Python Installation

installation includes:

- Python _runtime_ for executing Python code
- interactive Python console
- IDLE: simple development environment
- PIP: package manager for installing extensions
- Python documentation

# The interactive Python console

## The interactive Python console

launching the Python console / shell:

- command `python` in the command prompt
- from the start menu (e.g. _Python 3.7 (64-bit)_)

# Variables

## Variables

Data can be labeled with a name in Python - this is called a _variable_

```py
birth_year = 1970
current_year = 2019
age = current_year - birth_year
```

Names of variables are usually written in lower case, separating words by underscores

Variable names may only consist of letters, digits and underscores

## Variables

Overwriting (reassigning) variables:

```py
name = "John"
name = "Jane"
a = 3
a = a + 1
```

# Basic data types

## Basic data types

- `int` (integer)
- `float` (floating point number)
- `str` (string): text
- `bool` (boolean): yes / no
- none: missing / unknown value

## int & float

```py
(7 - 3) * 0.5 / 3.5
```

## str

A _string_ represents text

Strings can be enclosed in single or double quotes

```py
greeting = "Hello"
name = 'Tom'
```

## Building strings

```py
name = "Tom"
```

Inserting a variable (f-strings):

```py
message1 = f"Hello, {name}!"
```

Joining strings:

```py
message2 = "Hello, " + name + "!"
```

## Strings - escape sequences

Problem: how do we include characters like `"` in a string?

this is invalid:

```py
text = "He said: "hi!""
```

## Strings - escape sequences

solution:

```py
text = "He said: \"hi!\""
```

Python treats the sequence `\"` like a single `"`

## Strings - escape sequences

Line break: `\n`

```py
a = 'line 1\nline 2'
```

single Backslash: `\\`

```py
b = 'C:\\docs'
```

## bool

boolean value: yes/no

In Python: `True` or `False`

Note: capitalization is crucial!

## None

None represents a value that is unknown or missing

```py
first_name = "Mike"
middle_name = None
last_name = "Jones"
```

# Types and type conversions

## Types

Determining the type of a variable via `type`:

```py
a = 4 / 2

type(a)
```

## Type conversions

Objects may be converted to other types `int()`, `float()`, `str()`, `bool()`, ...

```py
pi = 3.1415
pi_int = int(pi)
message = "Pi is approximately " + str(pi_int)
```

# Composite types: dict, list

## dict

Dicts (_dictionaries_) are mappings that contain "named" entries with associated values

```py
person = {
    "first_name": "John",
    "last_name": "Doe",
    "nationality": "Canada",
    "birth_year": 1980
}
```

## dict

Retrieving and setting elements:

```py
person["first_name"]
```

```py
person["first_name"] = "Jane"
```

## list

A list represents a sequence of objects

```py
primes = [2, 3, 5, 7, 11]

users = ["Alice", "Bob", "Charlie"]
```

## list

Retrieving list elements via their index (starting at 0):

```py
users = ["Alice", "Bob", "Charlie"]

users[0]
users[1]
users[2]
```

## list

Overwriting a list element

```py
users[0] = "Andrew"
```

## list

Appending an element

```py
users.append("Dora")
```

## list

Removing the last element:

```py
users.pop()
```

Removing by index:

```py
users.pop(0)
```

## list

Determining the length

```py
len(users)
```

## Data types - exercises

We start out with an empty _dict_ - we want to create a data structure that represents a person

```py
person = {}
```

the desired result could look like this:

```py
{
    "first_name": "Kofi",
    "last_name": "Annan",
    "birth_year": 1938,
    "children": ["Ama", "Kojo"]
}
```

## Data types - exercises

create and modify data structures that represent the following:

- data of a country (inhabitants, capital, neighboring countries)
- a transaction on a bank account
- a set of transactions on a bank account

# Object references and mutations

## Object references and mutations

What will be the value of `a` at the end of this code?

```py
a = [1, 2, 3]
b = a
b.append(4)
```

## Object references and mutations

An assignment (e.g. `b = a`) assigns a new (additional) name to an object.

The object in the background is the same.

## Object references and mutations

If the original should remain intact it may be copied or a mutated version can be newly created based on it:

```py
a = [1, 2, 3]
# creating a new copy
b = a.copy()
# modifying b
b.append(4)
```

```py
a = [1, 2, 3]
# creating a new object b based on a
b = a + [4]
```

## Mutations

Some objects can be mutated (changed) directly - e.g. via `.append()`, `.push()`, ...

Examples: `list`, `dict`

Many simple objects are immutable after they have been created. However, they can be replaced by other objects.

Examples: `int`, `float`, `str`, `bool`, `tuple`

## Mutations

Changing a list directly:

```py
primes = [2, 3, 5, 7]
primes.append(11)
```

Creating a new string based on an existing string (but assigning it to the same name as before):

```py
greeting = "Hello"
greeting = greeting + "!"
```

# Help and documentation

## Help and documentation

Interactive help on objects in the Python console:

```py
help(list)
```

(navigate through long outputs via _Enter_, exit via _Q_)

## Help and documentation

Documentation on built-ins and the standard library:

https://docs.python.org/3/library/index.html

Similar to the `help` Function, but often with more detailed descriptions

# Python programs

## Python programs

For writing entire Python programs we'll use an editor or development environment

## Installing VS Code

https://code.visualstudio.com/

## VS Code: Setup for Python

- Open a folder, create and open a file with the filename extension `.py`, e.g. `demo.py`
- Install the VS Code extension named _Python_ (via the popup at the bottom right)
- Install the Python Package named _pylint_ (via the popup at the bottom right)
- Configure the _Python_ extension:
  - press `F1`
  - Search for "Python: select interpreter"
  - Enter
  - wait...
  - choose Python 3.7

## VS Code: Running Python programs

green "Play" button in the editor view

or

_Debug_ - _Start Without Debugging (Ctrl + F5)_

# VS Code

## VS Code

https://code.visualstudio.com

open source IDE

independent of _Visual Studio_ itself

## VS Code: open folder

via _File_ - _Open Folder_

## VS Code: File explorer, split editor

## VS Code: Terminal

Open / close the terminal view via _ctrl_ + _`_

Open an additional terminal via the _+_ Symbol

Terminals will run in the currently open folder

## VS Code: Configuration

Via _File - Preferences - Settings_

Is split in _User Settings_ and _Workspace Settings_

## VS Code: Configuration options

Recommendations:

- Accept Suggestions on Commit Character (Autocomplete on other keys than _Enter_): _deactivate_
- Auto Save: _afterDelay_
- Tab Size: _2_ or _4_

Further Options:

- Word Wrap
- EOL
- Workbench: Color Theme

## VS Code: Shortcuts

- _F1_ or _Ctrl_ + _Shift_ + _P_: command palette

<!-- list separator -->

- _Ctrl_ + _F_: Search in File
- _Alt_ + _Shift_ + _F_: Auto-format file contents
- _Ctrl_ + _#_: comment / uncomment
- _F12_: Go to definition
- _Shift_ + _F12_: Peek definition
- _F2_: rename variables
- _Alt_ + mouse click: Activate multiple text cursors

# Our first Python program

## Our first Python program

We'll create a file called `greeting.py`

Our program will ask the user their name and greet them.

## Input and output of text

Output: via `print()`:

```py
print("Hello. What is your name?")
```

Print is a so-called _function_.

## Input and output of text

Input: via `input()`:

```py
name = input()
```

`input` will always return a string

## Input and output of text

writing the greeting

```py
print("Nice to meet you, " + name)
```

## Executing programs

on the command line via `python greeting.py`

In VS Code via _F5_

## Exercise: age from birth year

Write a program called `age.py` which will ask the user for their birth year and will respond with the user's age in the year 2019.

## Exercise: length of the name

Write a program which asks the user for their name. It should respond with the number of letters in the user's name.

For this purpose use the function `len(...)` to determine the length of a string.

## Comments

Comments are a useful tool for developers to describe what the code is doing. They don't influence the program itself.

A comment starts with a `#` and extends to the line end.

Usually comments are placed _above_ the code they describe

```py
# determine the length of the name
name_length = len(name)
```

# Builtins, Standard library

## Builtins, Standard library

- _Builtins_: functions and objects that are used frequently and available at all times
- _Standard library_: collections of more functions etc that can be imported

documentation: https://docs.python.org/3/library/index.html

## Builtins

amongst others:

- `print()`
- `input()`
- `len()`
- `max()`
- `min()`
- `open()`
- `range()`
- `round()`
- `sorted()`
- `sum()`
- `type()`

## Standard library

Modules contain additional objects that can be imported

e.g.:

```py
import math

print(math.floor(3.6))
```

or

```py
from math import floor

print(floor(3.6))
```

## Standard library

modules of interest:

- `pprint` (pretty printing)
- `random`
- `math`
- `datetime`
- `os` (operating system, file system)
- `sys` (python environment)
- `urllib.request` (HTTP queries)

## print and pprint

Printing multiple elements:

```py
print(1, 2, 3, sep=", ", end="\n\n")
```

```bash
1, 2, 3


```

## print and pprint

```py
import pprint

pprint.pprint(['Mercuy', 'Venus', 'Earth', 'Mars', 'Jupiter',
               'Saturn', 'Uranus', 'Neptune', 'Pluto'])
```

```
['Mercuy',
 'Venus',
 'Earth',
 'Mars',
 'Jupiter',
 'Saturn',
 'Uranus',
 'Neptune',
 'Pluto']
```

## random

```py
import random

print(random.randint(1, 6))
print(random.choice(["heads", "tails"]))
```

## sys

Command line arguments can be read via `sys.argv`

```py
# hello.py
import sys
print(sys.argv)
```

```bash
python hello.py one two three
```

```bash
['hello.py', 'one', 'two', 'three']
```

## urllib.request

Qerying web contents

```py
from urllib.request import urlopen

content = urlopen("https://google.com").read()
print(content)
print(len(content))
```

# Control structures

## Control structures

By using control structures we can execute some code repeatedly or only under certain circumstances.

## Control structures

The two most essential control structures in every programming language are:

- if/else
- loops

## if / elif / else

example: guess the number

# If

## Comparisons

In order to use if and while we have to be able to compare values:

```py
a = 2
b = 5

print(a == b) # a is equal to b
print(a != b) # a not equal to b
print(a < b)  # a is smaller than b
print(a > b)
print(a <= b) # a is smaller than or equal to b
print(a >= b)
```

## If / else

example:

```py
age = 30
age_seconds = age * 365 * 24 * 60 * 60

if age_seconds < 1000000000:
    print("You are less than 1 billion seconds old")
else:
    print("You are older than 1 billion seconds")
```


## If / elif / else

```py
if age_seconds < 100000000:
    print("You are les than 100 million seconds old")
elif age_seconds < 1000000000:
    print("You are less than 1 billion seconds old")
elif age_seconds < 2000000000:
    print("You are less than 2 billion seconds old")
else:
    print("You are older than 2 billion seconds")
```

## Code blocks

code block = a group of lines that belong together - for example the code that gets executed when an if condition is true

In Python the line before the code block ends with a `:` and the code block is indented (usually by 4 spaces)

# While loops

## While loops

An if clause will execute a code block _once_ if a criterion holds

A while clause will execute a code blok _as long as_ a criterion holds

example:

```py
a = 1

while a < 2000:
    print(a)
    a = a * 2
```

## While loops

examples:

- guess the number with multiple attempts
- a loop that prints the numbers 1 to 10
- a loop that prints the numbers 7, 14, 21, ..., 70
- exercise program for simple calculations

## While loops

Exercise: shopping list

Example interaction:

```
enter an item or "x" to quit:
milk
enter an item or "x" to quit:
bread
enter an item or "x" to quit:
apples
enter an item or "x" to quit:
x
your shopping list is:
["milk", "bread", "apples"]
```

## Continue & break

The keywords `continue` and `break` may be used to end the current iteration or the entire loop respectively.

In nested loops they refer to the innermost loop.

## Continue & break

example:

```py
a = 1

while True:
    a = a * 2
    print(a)
    if (a > 1000):
        break
```

# Combining comparisons

## Combining comparisons

- combining with `and`, `or`, `not`
- chaining comparisons

## Combining with and, or, not

Examples:

```py
if age >= 18 and country == "de":
    print("may drink alcohol")

if temperature < -10 or temperature > 30:
    print("extreme weather")

if not value > 10:
    print("value not greater than 10")
```

## Chaining comparisons

`a` and `b` are both `0`

```py
a == b == 0
```

`b` is between 4 and 10

```py
4 < b < 10
```

# For loops

## For loops

With for loops we can iterate over the contents of lists (and similar objects).

In other programming languages this construct is called _for-each_

## For loops

```py
names = ["Alice", "Bob", "Charlie"]

for name in names:
    print("Hello, " + name + "!")
```

## Example: login system

```py
users = [
    {"name": "Alice", "password": "1234"},
    {"name": "Bob", "password", "password"},
    {"name": "Charlie", "password": "paris41"}
]
```

## Example: login system

example program run:

```
Enter your username:
lice
No such user.
Enter your username:
Alice
Enter your password:
123
Wrong password
Enter your password:
1234
Logged in as Alice!
```

# Counting loops

## Counting loops

This is how we can count from 0 to 9 in Python:

```py
for i in range(10):
    print(i)
```

The function call `range(10)` creates an Object that behaves like the list `[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]`.

## Counting loops

exercise: creating a "multiplication table"

```
1 x 7 = 7
2 x 7 = 14
3 x 7 = 21
4 x 7 = 28
...
```

# constituent parts of programs

## constituent parts of programs

- programs
  - code blocks
    - statements
      - expressions

## statements across multiple lines

If a statement should encompass multiple lines it is usually written in parentheses:

```py
a = (2 + 3 + 4 + 5 + 6 +
     7 + 8 + 9 + 10)
```

Alternative: _escaping_ newlines with `\`

```py
a = 2 + 3 + 4 + 5 + 6 + \
    7 + 8 + 9 + 10
```

# control structures - examples

## control structures - examples

- leap year
- guess the number with multiple tries
- loop that prints the numbers 1 to 10
- loop that prints the sequence 7, 14, 21, ...
- guess the number with random numbers
- math trainer with random tasks
- babylonian method (for finding the square root)

## leap year

example: leap year

- a year is a leap year if it's divisible by for
- exception: it's _not_ a leap year if it's also divisible by 100
- exception from the exception: it _is_ a leap year if it's divisible by 400

Hint: "x is divisible by y" in Python: `x % y == 0`

## example: babylonian method

method for computing the square root of a number which was already in use 4000 years ago in mesopotamia

## example: babylonian method

```
wanted: square root of 12345

n = 12345

Start with two approximations, e.g. a=1 and b=n

repeat the following until a nd b are almost equal:
new a = average of old a and old b
new b = n / a

=> a and b will approach the square root
```

## babylonian method: solution

```py
n = 12345
a = 1
b = n
for i in range(10):
    a = (a + b) / 2
    b = n / a
print(b)
```

# Functions

## Functions

We already know some predefined functions, like `len()`, `range()` or `print()`

## Parameters and return values

functions can receive parameters and return a value

example: `len([1, 1, 1])` → `3`

parameter: `[1, 1, 1]`

return value: `3`

## Positional parameters and keyword parameters

Calling `open`:

with positional parameters:

```py
f = open("myfile.txt", "w", -1, "utf-8")
```

with keyword parameters:

```py
f = open("myfile.txt", encoding="utf-8", mode="w")
```

We can names of keyword parameters in the documentation (e.g. via `help(open)`)

## Optional parameters and default parameters

Some parameters of functions can be optional (they have a default value)

Example: For `open` only the first parameter is required, the others are optional

The values of default parameters can be looked up in the documentation

# Defining functions

## Defining functions

example:

```py
def average(a, b):
    m = (a + b) / 2
    return m
```

## Optional parameters and default parameters

This is how we define default values for parameters:

```py
def shout(phrase, end="!"):
    print(phrase.upper() + end)

shout("hello") # HELLO!
shout("hi", ".") # HI.
```

## Scope

A function definition creates a new _scope_, an area where variables are valid

In the following example there are two distinct variables named `m`:

```py
m = "Hello, world"

def average(a, b):
    m = (a + b) / 2
    return m
x = average(1, 2)

print(m)
```

## Scope

Inside a function, outer variables may be read but not overwritten

In other programming languages constructs like `if` or `for` usually also open a new scope - this is not the case in Python

## Exercise: function lottery()

Write a function named `lottery` which creates a list of lottery numbers

`lottery()` → `[2, 35, 19, 27, 10]`

## Exercise: isprime()

Write a function named `isprime` which tests whether a number is prime

`isprime(59)` → `True`

## Aufgabe: ask_yes_no()

Write a function named `ask_yes_no`, which asks the user a yes/no question and returns either `True` or `False`

# Functions: Exercises

## Exercises

- function that verifies a credit card number / ISBN / IBAN
- prime numbers within an interval
- fibonacci numbers

For ISBN / primes: use the % operator

## Luhn algorithm (checksum)

The Luhn algorithm is used to prevent errors in identification numbers, such as credit card numbers

The last digit of these numbers is a check digit which is computed from the other digits

Example: the sequence `7992739871` has a check digit of `3`, so the entire number would be `79927398713`

## Luhn algorithm

Computing the check digit:

starting from the right, replace every _other_ digit based on this schema:

0 → 0, 1 → 2, 2 → 4, 3 → 6, 4 → 8,  
5 → 1, 6 → 3, 7 → 5, 8 → 7, 9 → 9

(For example `7992739871` will become `7994769772`)

sum all digits

(For example `7994769772` will sum to 67)

the check digit is the number that's missing from the next full 10

(in this case, it's 3)

## ISBN

International Standard Book Number = 10-digit book number with a check digit at its end

computing the check digit:

(1st digit + 2 \* 2nd digit + 3 \* 3rd digit ... + 9 \* 9th digit) modulo 11

task:

```py
check_isbn("3826604237") # True or False
```

## ISBN

```py
isbn = "3826604237"
expected = 7

def check_isbn(isbn, checksum):
    return isbn_checksum(isbn) == checksum


def isbn_checksum(isbn):
    sum = 0
    for i in range(9):
        sum += int(isbn[i]) * (i + 1)

    return sum % 11

print(check_isbn(isbn, expected))
```

## IBAN

# Code quality and linting

## Code quality and linting

aspects:

- general linting
- style conventions (PEP8)
- docstrings

## general linting: Pylint

Finding and displaying general errors

VS Code configuration via `python.linting.pylintEnabled` and `python.linting.pylintUseMinimalCheckers`

## PEP8

standard styleguide for Python code

official document: https://www.python.org/dev/peps/pep-0008/

cheatsheet: https://gist.github.com/RichardBronosky/454964087739a449da04

## PEP8 & code formatting tools

- autopep8
- yapf
- _black_

In VS Code config: `"python.formatting.provider": "black"`

## PEP8 & code formatting tools

```py
# input:
a='hello'; b="bye";

# autopep8:
a = 'hello'
b = "bye"

# yapf:
a = 'hello'
b = "bye"

# black:
a = "hello"
b = "bye"
```

## PEP8 and code formatting tools

```py
# input:
a[0+3:1]

# autopep8:
a[0+3:1]

# yapf:
a[0 + 3:1]

# black:
a[0 + 3 : 1]
```

## Docstrings

Documentation that describes a function / class / module in more detail

## Docstrings

example:

```py
def fib(n):
    """Compute the n-th fibonacci number.

    n must be a nonnegative integer
    """
    ...
```

## displaying docstrings

```bash
python -m pydoc math
python -m pydoc math.floor
```

## Docstring structure

PEP 257: https://www.python.org/dev/peps/pep-0257/

## Docstrig structure

docstring of a module: description, list of exported functions with single-line summaries

docstring of a class: description, ist of its methods

docstring of a function: description, list of its parameters

## Pydocstyle

linter for validating docstrings

## Python philosophy, Zen of Python

Quotes from the _zen of Python_ (full text via `import this`):

- _Explicit is better than implicit._
- _Readability counts._
- _Special cases aren't special enough to break the rules._
- _There should be one-- and preferably only one --obvious way to do it._

# Debugging

## Debugging

Breakpoints can be set to pause execution at a certain point.

Possibilities to set breakpoints:

- directly in Python Code via `breakpoint()` (since Python 3.7)
- in VS Code: click next to the line number

## Debugging

Continuing manually:

- proceed until the next breakpoint:
  - `c` for _continue_ in the Python debugger
  - _Continue_ in VS Code
- end debugging:
  - `q` for _quit_ in the Python debugger
  - _Stop_ in VS Code

## Debugging

Continuing manually:

- proceed to the next line:
  - `n` for _next_ in the Python debugger
  - _Step Over_ in VS Code
- proceed to the next line - following function calls
  - `s` for _step_ in the Python debugger
  - _Step Into_ in VS Code
- run the current function to its end:
  - `r` for _return_ in the Python debugger
  - _Step Out_ in VS Code

## Debugging

Printing values in the Python debugger via `p`:

```py
p mylist
p mylist[0]
```

Examining values in VS Code:

- local variables in the _variables_ widget
- watch custom expressions in the _watch_ widget

# Cheatsheet

https://ehmatthes.github.io/pcc/cheatsheets/README.html

(missing topics: break, None, comments)

