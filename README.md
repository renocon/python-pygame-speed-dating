# python-refresh
Quick crash course over basic Python 3 language features in preparation for
ClickToStart's Programming course. You should take some time and go over the 
official Python tutorial https://docs.python.org/3/tutorial/, this is just to
quickly go through core features you should be familiar with. These notes were
greatly inspired by [University of Edinburgh Informatics lab
notes](http://www.inf.ed.ac.uk/teaching/courses/inf2a/tutorials/2016_inf2a_P01_exercises.pdf).

The code we are writing here would work on all of Python 3 versions (and the 
vast majority on Python 2 as well) But you should use version 3.6 as it's the 
latest and greatest at the time of writing.

# Interpreted or Compiled?
Python is a programming language, a formal language specification designed to 
give instructions to a computer. The Python language has many implementations: 
* CPython: the reference implementation for Python, and the one you probably
installed from the main website. CPython is an interpreter, but it first
compiles the Python source code to an intermediary byte code. The byte code is
what's interpreted.
* PyPy: a Python interpreter built with Python itself (a subset of Python to be
technical). It does [Just-in-Time
Compilation](https://en.wikipedia.org/wiki/Just-in-time_compilation) and is 
known to be quicker than CPython in many cases.
* Jython: Python which runs on the JVM
* IronPython: Python which runs on .NET framework and Mono

# Mind Your Space
Whitespace is important in Python. If you come from a language background with
brackets and the like, welcome to The Light! Indentation determines scope. For
indentation we'll be use 4 spaces as guided by
[PEP-8](https://www.python.org/dev/peps/pep-0008/).

# Numbers
The usual operators you've seen in Java/C/etc are all here as well:
+, -, *, /, %. Run Python on your shell `python3` and type the following:

```python    
5 + 3 # = 8
2 * 8 # = 16
3 / 2 # = 1.5
10 - 9 # = 1
13 % 3 # = 1

# You also figured that comments begin with # and go till the end of the line
# Note the division in of 3/2 returns 1.5. If you used Python 2 that division
# would return 1 as the numbers weren't explicitly floats. No need to worry 
# about that in version 3 :)

# To get that division that also floors the result do like the following
3 // 2 # = 1

# In Python, exponents use **
2**5 # = 32
```

# Strings

# Booleans
Python has two boolean values: True and False. Booleans inherit from integers,
so you can add and multiply them like numbers. True is 1 and False is 0

```python
True + True # = 2
True * 7 # = 7
False - 5 # 0
```

## Conditions
Well Booleans aren't fun for additions and other mathematical operators. We use
them to test for truthfullness. Or truthiness. Truth. We can write expressions
which evaluate to True or False:

```python
True and True # = True, using and is much easier than && right?
True or False # = True, more English words please
not True # = False
```

We can do comparisons on other Data Types as well

```python
8 == 2 * 4 # = True, == test equality, strings can be tested as well
'hi' == "  hi\t".strip() # strip function removes whitespace characters

2**7 != 64 # = True, test inequality

# Greater than or less than
4 > 2
19 < 19.5

# Greater/less than or equal to
23 >= 23
-42 <= -37

# Python also has "is". People use it interchangeably with == but that's not
# entirely correct. The is keyword checks if the two things being compared 
# points to the same object. == checks if two values being referenced have the
# same value
1000 is 10**3
1000  == 10**3

```

# Lists

## Fun with Indices

# Tuples

# Dictionaries

# If-Elif-Else

# For loop

# While loop

# List Comprehensions

# Lambda, Map and Filter

# Functions

# Classes and Objects
