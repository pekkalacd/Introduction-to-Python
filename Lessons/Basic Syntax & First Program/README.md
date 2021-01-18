# Basic Syntax & First Program

## Basic Syntax

### Comments
* Comment blocks are wrapped around **"""content"""**
```
"""
Author: George Washingthon
Date: 07/04/1776
"""
```
* In-line comment starts with **#**
```
# My first inline-comment
print("hello world") # inline-comment always goes after statements or goes byself in a line
```

### string
* Wrapped either in _a single-quote pair_ **'string'** or _a double-quote pair_ **"string"**
```
print('hello 1')
print("hello 2")

# output => hello
# output => world
``` 

### 'print' function
* 'print' function is to print output to screen and move cursor in screne to the next line
*  output is **a mix of string/integer/float** because Python implicitly converts all inputs to string in 'print' functiono
"""
print("Hello world") # print hello world to screen
```
* List of comma-separated strings will be concatenated with space in between by 'print'
```
print('hello', "world", 'i am ', 10, 'years old')

# output => hello worlld i am 10 years old
```
