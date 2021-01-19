# Basic Overview
<br>

**The World Needs Computers**

Today, the world runs on computers. Everything, from businesses needing to handle their internal data and customer
records, to finance personnel completing transactions on the stock market, to massive tech companies innovating and
building consumer products that are shaping the way we see life, relies heavily on the presence of computers.

<br>

**What is a computer?**

A computer is a machine that can be instructed to carry out sequences of arithmetic and logical operations via
computer programs.

<br>

**What is a computer program?**

A computer program is a sequence of arithmetic and logical statements that generate specific instructions for
a computer to perform a specific task. In order to write a program, ***programmers*** (like you) use a ***programming language***
to communicate these instructions over to the computer. Computers do not understand the language at face-value however.
Instead, computers acknowledge what is known as ***machine language*** or streams of binary digits (*bits*) of 1's and 0's.
These streams of binary are abstractions from what is actually going on within the computer physically. A 1 can be thought of as
an "on" switch, while a 0 is an "off" switch for a set of voltages passing through a series of transistors. 

<br>

Typically, application programmers do not consider much of what is physically happening within the machine. Instead,
they reside on the ***high-level*** of programming. Whereas, programmers who focus closer to the hardware such as
embedded systems programmers reside on the ***low-level*** of programming. The idea of high versus low is generally with respect
to how closely work is being done to the hardware. 

<br>

**From programming language to machine language**

Programming languages are tools to make it easier for humans to communicate instructions to computers. But since computers do not understand the languages, and
instead understand machine language, there needs to be intermediary steps taken to get the instructions into a computable form. This process
is complex, varies by language, and is often comprised of multiple software tools. 

<br>

An assortment of languages are *compiled*. Compiled languages require a piece of software called a *compiler* to translate the
***source code*** (another name for programming language) into machine language. For example, in languages like C and C++, the compiler is one
of three required pieces of software in order to take a text-file and make it an executable file: ***preprocessor***, ***compiler***, and ***linker***. 

<br>

1. The **preprocessor** is a piece of software which processes a set of command known as ***directives***. These directives perform purely textual manipulation
such as including libraries and defining constants. When the preprocessor has finished processing these commands, the directives are then removed, and a
file of source code is sent to the compiler in the form of a ***modified source code*** file. 

2. The **compiler** looks at the source code and utilizes an ***assembler***, another piece of software which
moves the source code into several intermediate languages collectively known as ***assembly***, and then from there translates the assembly into
machine language. However, for source code which may be created by using functionality proposed from the directives (in the previous stage), the compiler
leaves a ***hole***. For this reason, the compiler then sends a non-executable binary file called an ***object code*** file to the linker.

3. The **linker** looks at the binary contained within the object code file, along with the previously accounted for textual manipulations from the
preprocessor, and *fills the holes* with the appropriate logic. Once filled, the linker creates an ***exectuable file***. 

<br>

Today, many programmers use something known as an ***Integrated Development Environment*** (IDE), to do their work. For a compiled language,
that entire 3 step process is typically done with a single click of a button!

<br>

<u>**What is Python?**</u>

Python is a general purpose object-oriented programming language. Though, traditionally it has been thought of as a ***scripting language***, Python has grown into
a stand alone language in many applications. Unlike C and C++, Python is not a compiled language. It is an ***interpreted language***, though compilation is a step. Python's execution process differs from the 3 step process above.
It's also a ***dynamically*** and ***strongly*** typed language. As opposed to C and C++ being ***statically*** and ***weakly*** typed languages. We'll get into each of these below.

1. **Interpreted Language**<br>
Python can be written in python files using the .py extension or directly into an interactive interpreter like **IDLE**. When a program in a Python file is executed, as part of its compilation process and
differently than C or C++'s translation into machine language, Python creates a bytecode file (.pyc or .pyo). This bytecode is a set of low-level instructions that is executable by the interpreter.
While a compiler will require that an entire program, free of compile-time errors, be produced before it's able to execute, an interpreter, allows one-line to be ran at a time. 

2. **Static vs Dynamic Typing**<br>
Languages like C and C++ are *statically typed* languages. This means that once a data-type is declared for a particular object, that object cannot change the type of data it stores at-will. The object must be casted
to the corresponding data type of the data it'd like to store, before it can store the new data. Unlike those languages, Python is a *dynamically typed* language. This means that objects data types automatically change to
reflect the type of data that it stores. 

3. **Weak vs Strong typing**<br>
C and C++ are also *weakly typed* languages, which means that the rules guiding the use of each data type are held weakly when interacting with other types via operations. This could
result, for example, in the addition of a character and an integer with no error. Whereas, Python is *strongly typed*, meaning that the rules guiding the use of each data type are well defined and held in consideration
in each type's interaction with other types. For example, the addition of a single character and an integer in Python would throw a TypeError.

<br>

All pieces considered, Python is a great language to get started with for beginners. It's simple syntax and plethora of built-in functions make it easy to understand and effective.

<br>

**A Brief History of Python**

In 1989, Guido Van Rossum, a developer for ABC, an imperative general purpose programming language aimed at teaching and prototyping, started a new scripting language aimed at appealing to the ABC and UNIX/C hacker community
as a side project.  A fan of Monty Python's Flying Circus, he gave it the name "Python". 

A decade later, Van Rossum submitted a "Computer Programming for Everyone" proposal to DARPA where he defined the following goals:

- An easy open source intuitive language just as powerful as major competitors
- Open source, so that any one can contribute to it's development
- Code that is as understandable as plain English
- Suitability for everyday tasks, allowing for short development times

Since 2004, Python has been among the 10 most popular programming languages every year. In the past 3, Python has been a member of the top three most-used languages on GitHub.

<br>


**Why learn Python?**

Python is everywhere! Google, Twitter, Facebook, and more companies use Python at some level. It's applications are endless. 

Arguably, it's most notable one is in the ***data analysis*** space where ***libraries*** such as [**pandas**](https://pandas.pydata.org/), [**seaborn**](https://seaborn.pydata.org/), [**numpy**](https://numpy.org/),
[**matplotlib**](https://matplotlib.org/), [**tensorflow**](https://www.tensorflow.org/guide/data), [**pytorch**](https://pytorch.org/), and [**more**](https://www.geeksforgeeks.org/top-10-python-libraries-for-data-science-in-2020/) reside.

Python has a space in web development as well. A popular tool for the back-end of web applications, Python can be used to handle server-side requests, working with databases, and authentication. Frameworks such as
[**Flask**](https://flask.palletsprojects.com/en/1.1.x/) and [**Django**](https://www.djangoproject.com/) can be used to build light-weight or traffic-heavy applications and sites. Companies like Instagram, Mozilla, Pinterest,
and National Geographic are known Django users. For Flask, companies like Red Hat, Rackspace, Airbnb, Netflix, Lyft, and Reddit, use it. 

Beyond it's readability and simple effectiveness, Python boasts more than 250,000 open source packages allowing for extended functionality. These can be used for an assortment of tasks such as building games, websites, web apps,
data analysis, data visualization, machine learning, security, and [**more**](https://pypi.org/).

<br>

**How do you get Python?**

Python can be downloaded from the python website available at: [**https://www.python.org/downloads/**](https://www.python.org/downloads/). Download the latest version of Python, 3.9.1. This tutorial will work for versions 3.8.0 or later.

As mentioned previously, an *Integrated Development Environment* (IDE) is a common tool used by many programmers. When Python is installed on your computer, it will come with an interpreter called **IDLE** built-in. If you
would like to use a different IDE, some notable ones are: [**Visual Studio Code**](https://code.visualstudio.com/), [**PyCharm**](https://www.jetbrains.com/pycharm/), [**Spyder**](https://www.spyder-ide.org/), and [**Jupyter**](https://jupyter.org/install). 

Another commonly used tool is called a ***package manager***. This tool is responsible for downloading packages for extended functionality. If Python later than 3.4 is installed, you should already have **pip** installed.
This is Python's built-in package manager. If you'd like to use a different one, a notable alternative is: [**conda**](https://docs.conda.io/projects/conda/en/latest/user-guide/install/windows.html). 

<br>

### For more information on Python installation see EXAMPLES.md in the Basic Overview folder or click [here](https://github.com/pekkalacd/Introduction-to-Python/blob/master/Lessons/Basic%20Overview/EXAMPLES.md)



 

