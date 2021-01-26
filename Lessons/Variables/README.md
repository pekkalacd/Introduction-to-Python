# Variables
<br>

Variables are programmer-named storage locations that hold specific **data-types**. In Python, you do not need to
*declare* a variable, but it **must be initialized** in the same line. In order to initialize a variable, we use the assignment operator = . The variable resides to the left of
the assignment operator, while the value to be stored within the variable is to the right of the assignment operator.<br><br>

```
    myVariable = 22
```
<br>

### Literals in Variables

In an earlier lesson, we mentioned that *literals* are values that can be contained within a variable. Each literal has a specific data-type. Some examples of literals are 22, "dog",
and 32.3333, these are integer, string, and float literals respectively. Each of these could be put into a variable.<br>

```
    a = 22
    b = "dog"
    c = 32.3333
```
<br>

The data-type of the literal **is** the data-type of the variable to the left of the assigment operator.<br>

```
    type(22) == type(a)
    # output => True
    
    type("dog") == type(b)
    # output => True
    
    type(32.3333) == type(c)
    # output => True
```
We can check the data-type of an object by using the built-in function **type**. When used by itself, the type function will return the data-type of the object we check in
the form ```<class '{type}'>```. For example, ```type(22)  # output => <class 'int'>```.<br><br>

### Data Structures in Variables

In addition to literals, a variable can also store basic **data structures**. A data-structure is an object that can be used to store various amounts and types of data.<br>

In Python, a **List** is a built-in data type and its a data structure. A List *dynamically* allocates memory. This means that there is no set-size to a List. Programmers can
add items to and remove them from a List as they please and it will automatically adjust. This is just one example of a structure that could be stored in a variable, others
include: dictionaries, sets, queues, tuples, strings, and more.<br>

To make a list, we use square brackets **[ ... ]**. Inside of the square brackets, we separate objects by commas. For example, below we've created a list called "myList" which
contains 3 elements: a string, an integer, and a float.<br>

```
    myList = ["dog", 32, 15.4]
    type(myList)
    # output => <class 'list'>
```
<br>
Just as before, we can verify that the type of the value to the right of the assignment operator matches the type of the variable.<br>

```
    type(myList) == type(["dog", 32, 15.4])
    # output => True
```


### Type Rules

Each data-type has a set of rules which denote the operations that can be performed on it. A variable containing data of some type \
must abide by the rules of that data-type. A variable's behavior aligns with that of the type of the data it stores.<br>

For example, strings can "concatenate" with the addition operator, but cannot subtract with the subtraction operator.<br>

```
    "hello" + " world!"
    # output => 'hello world!'
    
    "hello" - " world!"
    # output => TypeError: unsupported operand type(s) for -: 'str' and 'str'

```
<br>
If we put these strings into variables and attempt to do the same operations, we'll get the same results.<br>

```
    str1 = "hello"
    str2 = " world!"
    str1 + str2
    # output => 'hello world!'
    
    str1 - str2
    # output => TypeError: unsupported operand type(s) for -: 'str' and 'str'
```
<br>

Consider that I wanted a string added to an integer. Then according to our understanding of types and variables thus far, it should be that types of "int" and "str"
should be able to work together without error. Otherwise, this cannot be done.<br>

```
    myStr = "My favorite number is: "
    myNum = 42
    myStr + myNum
    # output => TypeError: unsupported operand type(s) for +: 'str' and 'int'
```
<br>
This did not work because a data-type of "str" (short for string) is unable to be *concatenated* with an integer using the addition operator. From the previous example, we
did see that we could add two strings together though. So, now, let's try it again but this time converting "myNum" to a string.<br>

```
    myStr = "My favorite number is: "
    myNum = 42
    myNum = str(myNum)
    myStr + myNum
    # output => 'My favorite number is: 42'
```
<br>

Generally, the rules that a variable must abide by will vary depending on the type. Each data-type has its own set of rules for what it can and cannot do and what operators
or methods may or may not apply to it. We'll learn more about this in a later section.<br>


### Data Consumption

Along with data-types comes the concept of memory and storage. We said that a variable is a named storage location. If it's a "storage" location, then it must have a size. The size
of the space allocated in memory to store the value contained within a variable is dependant on the variable's data-type.<br>

#### In Python, everything is an object. 

This is a topic that will come up in object oriented programming more. For this reason, the size of the data-types might seem conflicting
with a language like C++. In Python, each data type is a *class*. The definition of each of those classes are full-fledged and contain special functionality in attributes
and methods. These features of Python's data types add bytes onto each type's total amount of data consumed.<br>

Much like C++, however, individual literals of data types carry known byte amounts. For example, a signed integer in C++ is 4 bytes as is the same in Python. The general
equation for the amount of bytes consumed by a data type in Python is as follows:<br>

      # of bytes consumed =  (# of bytes consumed by instance of data-type ) + (# of bytes consumed by literal)

Below are tables denoting the differences between each of these.

<p align="center">
  <img src="https://user-images.githubusercontent.com/34849400/105893964-5dbad780-5fd9-11eb-833b-d3ecf836428c.png"\>
  <img src="https://user-images.githubusercontent.com/34849400/105893680-0157b800-5fd9-11eb-88dc-9cb1c3be4b8e.png"\>
</p>
<br>

For example, consider the snippet below.<br>
```
    import sys
    a = 150
    type(a)
    # output => <class 'int'>
    
    sys.getsizeof(a)
    # output => 28
```
<br>
This example illustrates the relationship disclosed in the table. The variable "a" is an integer. It is an instance of the "int()" class. So, there it consumes 24 bytes. In addition,
the variable "a" stores an integer-literal which is another 4 bytes. Total consumption = 24 bytes + 4 bytes = 28 bytes.<br><br>

That 28 bytes is the amount of memory or space that must be allocated in RAM for the variable "a" to store the value 150.<br>

The amount of memory consumed by a data-type is used to allocate a block of memory in RAM.<br>

### Memory

Early we noted that a variable is a programmer-named storage location within the computer. Let's think of this in an analogous situation. Picture a neighborhood. Inside of the
neighborhood, there are many houses. Each of these houses have a specific address which denotes exactly where inside the neighborhood each establishment resides.<br>

<p align="center">
  <img src="https://user-images.githubusercontent.com/34849400/105895683-6d3b2000-5fdb-11eb-96ea-bb5061a8e759.png"/>
</p>

A computer's **RAM** is very similar. There are **blocks** of memory that are allocated for objects being used in a program. These objects - depending on the data type - will
vary in terms of how much memory is allocated. But each one will also have it's own unique **memory address** which is the location of where that block is in memory.<br>

<p align="center">
  <img src="https://user-images.githubusercontent.com/34849400/105896671-b770d100-5fdc-11eb-9487-3816a9378dfb.png"/>
</p>

**When a variable is created 2 things happen:**
1. a unique memory address is generated
2. a block of memory is allocated in RAM that is proportional to the amount of bytes consumed by the variable

<p align="center">
  <img src="https://user-images.githubusercontent.com/34849400/105873337-fe50cd80-5fc0-11eb-91bd-784b6e3d1099.png"/>
</p>

**In this light, we can see variables as tools that can be used to shift blocks of memory around in a manner that the computer can understand.**

<br>

To illustrate this concept a little more, let's build a neighborhood of variables.<br>

```
    from sys import getsizeof
    
    # creating houses
    house1 = "bill's house"
    house2 = "dan's house"
    house3 = "melinda's house"
    
    print("Welcome to the neighborhood!\n\n")
    
    # house 1 info
    print("Name: ", house1)
    print("Address:", hex(id(house1)))
    print("Bytes:", getsizeof(house1))
    
    # house 2 info
    print("\nName:", house2)
    print("Address:", hex(id(house2)))
    print("Bytes:", getsizeof(house2))
    
    # house 3 info
    print("\nName:", house3)
    print("Address:", hex(id(house3)))
    print("Bytes:", getsizeof(house3))
    
    
    # output => Welcome to the neighborhood!
    
                Name: bill's house
                Address: 0x252f8ef2af0
                Bytes: 61
                
                Name: dan's house
                Address: 0x252f8ee2bb0
                Bytes: 60
                
                Name: melinda's house
                Address: 0x252f8ea2cf0
                Bytes: 64
```

<br>

**Things to notice here:**
- Each house is it's own variable
- Each house has a unique address
- Each house name is of different length
- Each house consumes a different amount of bytes
- All house variables are of type str

The address of where the house is located is where the computer is putting the variable in memory. The bytes amount can be thought of the square footage of the home, these
are homes of varying size. But in actuality, this is the amount of memory that the computer is allocating to store the variable. The variable names home1, home2, home3 are for us - the programmers - to keep track of.

<br>

**This concludes the lesson about variables. We'll continue using variables moving forward in every lesson moving forward.**

<br><br>

### Move to [Examples](https://github.com/pekkalacd/Introduction-to-Python/blob/master/Lessons/Variables/EXAMPLES.md) or [Exercises](https://github.com/pekkalacd/Introduction-to-Python/blob/master/Lessons/Variables/EXERCISES.md)


