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

### String
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
```
print("Hello world") # print hello world to screen
```
* List of comma-separated strings will be concatenated with space in between by 'print'
```
print('hello', "world", 'i am ', 10, 'years old')

# output => hello worlld i am 10 years old
```

## First Program
* Python is a scripting language. This means that Python codes could be executed in Python shell without **main** function/class as in C++/Java 
```
print("hello world") # output => hello world
```
- Or execution with **main.py** Python file
	- define **main.py**
	```
	def main():
		print('hello world')

	if __name__ == '__main__':
		main()

	```

	- execute in shell
	```
	>> python3 main.py

	# output => hellow world
	```
