<br><br>

# Basic Syntax Overview

One of Python's greatest strengths is its simple syntax. In other languages, the use of curly braces, semi-colons, data-types, backslashes, arrays, and double-quotes might be used to denote scope, end statements, declare variables, make comments, create strings and denote their values respectively. While it's not too difficult to abide by these rules, these syntatical requirements can make even simple code look complicated. 

Thankfully, Python's syntax is much simpler. There are no curly braces, semi-colons, variable declarations, backslashes for comments, nor arrays for strings required. Spacing and indentation replaces curly braces' appeal to scope, hitting the enter key replaces the need for semi-colons to end statements, dynamic typing takes care of needing to declare variable types, comments are made with **#** symbol for single line and doc-strings for multi-line, and strings are a basic built-in data type denoted with both double quotes **" "** and single **' '**. 

While Python's easy syntax allows beginners to progress quickly through the language, it can be easy to overlook subtle syntactical arrangements. For instances, ignoring indentation or variable naming conventions can result in SyntaxErrors being thrown by the interpreter and existing code being broken. Mastering Python syntax will result in less errors, cleaner code, and more control of your programs.

The topics discussed in this lesson, along with the examples, will be revisited in later lessons in more depth.

<br><br>


## Indentation & Scoping

A standout piece of Python's syntax is its use of **Indentation** as the scoping delimeter. We haven't spoke about ***scope*** yet and what that entails, but it is a very important topic in most languages. A *scope* can be thought of as the region in which a variable is created. Depending on this region, there might be other regions that the variable may or may not be able to access. We'll go into this more in a later section.<br>

Scope will come up inevitably when we go over *if, elif, and else* as well as with *loops*. For now, here's a sneak preview of this point in action in a loop:<br><br>

```
   x = 10
   L = [1,2,3]
   for i in L:
       x += i
       print(f"x = {x}")
```
<br>

See that **x** is created by the line ```x = 10``` and that x is reused in the line ```x += i```. Though the same variable is affected, x, the regions are different. Therefore, the scope of each statement is different. The first statement ```x = 10``` is in a scope that is larger than ```x += i```. Because x is created before the loop, in a larger scope, it is accessible within the loop.<br>

Notice that the line ```x += i``` is *indented* below the for-loop ```for i in L```. This is how we denote that the statement ```x += i``` is nested or contained within the region of the loop.<br>

<br><br> 


## Variable Naming

Another syntax-related topic is the naming of variables. At its core, a variable is a programmer-named storage location. When creating variables, a value must be initialized to the variable using the assignment operator **=**. Because of Python's dynamic typing, you do not have to specify the type of the variable prior to initialization. Also, the type of the variable can readily change. While Python is our friend when creating variables, we must abide by naming rules otherwise Python will throw an **SyntaxError**.<br>

### Naming Rules

| OK      | BAD | Error | RULE |
| ------- | --- | ----- | ------ |
| age = 32 | a ge = 32 | SyntaxError | variable names cannot contain spaces | 
| myName = "Mike" | my-Name = "Mike" | SyntaxError | variable names cannot contain special characters|
| Animal = "Zebra" | 5 = "Zebra" | SyntaxError | literals cannot be used in assignment statements |
| cost_33 = 1.22 | 33cost = 1.22 | SyntaxError | variable names cannot start with numbers |
| pizza4free = True | pizza4.0free = True | SyntaxError | variable names must not contain operators such as the membership operator '.' |
| Olay = "Muahaha!" | O = "Muahaha!" | No error, bad practice | Capital 'o' looks too similar to numerical zero |
| idaho = "Yippee!" | I = "Yippee!" | No error, bad practice | Capital 'i' looks too similar to lowercase 'L' |
| lol = "lololol!" | l = "lololol!" | No error, bad practice | Lowercase 'L' looks too similar to capital 'i' |

<br><br>

For more information on best practices when it comes to naming conventions see: [**PEP 8 Style Guide**](https://www.python.org/dev/peps/pep-0008/).


<br>


## String Syntax

A string is a type of *data structure* that is an array of characters. In Python, a string is also a built-in data-type marked by the keyword **str**. At it's core, a string-type is **immutable** which means that the values within the string cannot be changed without creating a new string entirely. A string can be denoted by **single or double quotes**. Each string must have a starting quote and an ending quote of the same style.<br>

| GOOD | BAD |
| ---- | --- |
| "dog" | "dog' |
| 'cat' | 'cat" |
| "the 'dog' and 'cat'!" | 'the 'dog' and 'cat'!' |

<br>

Strings can also be added together or **concatenated** in order to make a new string. The concatenation of two strings **returns** a new string.<br>

```
   birthday = "happy" + " " + "birthday!"
   print(birthday)
   
   # output => happy birthday!

```
<br>
  Strings **cannot** be subtracted though. <br> 

```
   birthday = "happy" + " " + "birthday!"
   birthdayAlone = birthday - "happy"
   
   # output => TypeError: unsupported type(s) for -: 'str' and 'str'

```
<br>
  Blast, we got an error! But why?<br> 
  This error tells us that the **binary operator -** does not work between strings. Why not though? **Because, strings are immutable in Python!**. We cannot change any string     in place without creating a new string to store the changes. Another example of the immutability is below:<br>

```
   myName = "jerry"
   myName.capitalize()
   # output => 'Jerry'
   
   
   print(myName)
   # output => 'jerry'
```
<br>
  In this example, we are *calling* the .capitalize() method on the variable myName containing the string "jerry". That method, .capitalize(), is a built-in method used for string data-types which capitalizes the first letter of the string. The problem is, when we call that method the first time we get the capitalized version of 'jerry', as expected. But when we call it the second time, the name is all lowercase again. Why?<br>

  Once again, because **strings are immutable**. The .capitalize() method *returns* a new string when it is called. So, it's creating a new string of the form 'Jerry' and returning it. By default, when *returning* a value from a function, we're taking the output of the function and storing it somewhere. If there is no where designated, such as a variable, to store that value, it will render on the screen. That is why the first output occurs, and does so, as 'Jerry'. 'Jerry' is the output of the .capitalize() method, which is a member-class function for the string type. And we didn't put it in a variable, so it displayed on the screen.<br> 

## Doc-strings

A doc-string is a type of string that is primarily used for documentation purposes. For any programmer, documentation is very important. Not just for understanding what a specific program or piece of code does, but for building on top of that program, trouble shooting it when it doesn't work, and for the future of that program all together. If you are writing a program in Python that is intended for other people to use then along with comments, doc-strings are definitely something to consider using.<br><br>

Doc-strings are noted with **triple quotation marks** these can be both double quotations or single quotations. Doc-strings can also be used to handle multi-line strings in a simpler way than regular strings. For example, here we'll try to encapsulate Maya Angelou's Quote as a multi-line statement, breaking after the comma: <br>
> You will face many defeats in life, but never let yourself be defeated.
<br>

Here is our attempt with a *regular* string:<br><br>

```
   quote = "You will face many defeats in life,<enter>
   # output: SyntaxError: EOL while scanning string literal

```
<br><br>
 This happened because we were using a regular string. Regular strings, in order to store multi-line statements, must either break up the lines of the string into multiple sub-strings and concatenate them together, or use **escape sequences** such as **\n** (for newline) in order to deal with line breaks. Doing so correctly, would look something like this<br><br>
 ```
   quote = "You will face many defeats in life," + "\n" + "but never let yourself be defeated."
   print(quote)
   
   # output => You will face many defeats in life,
               but never let yourself be defeated.
 ```
 <br><br>Equally, we could've done:<br><br>
 ```
   quote = "You will face many defeats in life,\nbut never let yourself be defeated."
   print(quote)
   
   # output => You will face many defeats in life,
               but never let yourself be defeated.
```
<br><br>
 But, a much easier option is to just use a doc-string.<br><br> 
```
  quote = """You will face many defeats in life,
  but never let yourself be defeated"""
  
  quote
  # output => 'You will face many defeats in life,\nbut never let yourself be defeated'
  
  print(quote)
  # output => You will face many defeats in life,
              but never let yourself be defeated.
```
<br><br>

 When we use a doc-string, any newline, tabs, or spaces we enter into the string, are automatically accounted for. This makes it really easy to copy and paste text from a source online and put into a string in Python and format such that Python is able to use it. Going further, the print function can then render that textual content on the screen as well. This is super useful to know when it comes to applications such as *web scraping* or *parsing* through textual data. There are a number of built-in methods or functions that we can use to enhance our ability to parse data from strings as we'll explore in a later section.<br><br>
 
 For documentation purposes, doc-strings can be used to display instructional information for programmers or users of functions. In the example below, we'll create a function which will display a name parameter along with a greeting such as "Hello, name!" to the screen. There will be a doc-string outlining to the user of the function, a developer, how to use that specific function.<br><br>
 
 ```
   def greetName(name):
       """ Prints a greeting in the form "Hello, {name}!" to the screen. 
           name: must be string.
       """
       
       try:
           if type(name) != str:
                raise ValueError("Unable to process. Arg 'name' must be of type str.")
           
           print("Hello," + " " + name + "!")
       
       except ValueError as e:
           return print(e)
 
  # call built-in help() function for more info
  help(greetName)
  
  # output =>  Help on function greetName in module __main__:
  
               greetName(name)
                   Prints a greeting in the form "Hello, {name}!" to the screen.
                   name: must be string
  
  
  # call function
  greetName("Mitch")
  
  # output => Hello, Mitch!

```

 
 
                  
       

  
  
  
  



















