<br><br>

# Basic Syntax Overview

One of Python's greatest strengths is its simple syntax. In other languages, the use of curly braces, semi-colons, data-types, backslashes, arrays or libraries and strict usage of double-quotes might be used to denote scope, end statements, declare variables, make comments, and create strings and denote their values respectively. While it's not too difficult to abide by these rules, these syntatical requirements can make even simple code look complicated and can pack quite a learning curve for beginners. 

Thankfully, Python's syntax is much simpler. There are no curly braces, semi-colons, nor data-types used to declare variables, backslashes for comments, nor arrays for strings required. Spacing and indentation replaces curly braces' appeal to scope, hitting the enter key replaces the need for semi-colons to end statements, dynamic typing takes care of needing to declare variable types, comments are made with **#** symbol for single line and doc-strings for multi-line, and strings are a basic built-in data type denoted with both double quotes **" "** and single **' '**. 

While Python's ease of use gives beginners a boost in their ability to progress quickly through the language, it's still very important to know about and abide by the syntatical rules of the language. Mastering them will result in less errors, cleaner code, and more control of your programs.

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

If this is confusing for now, do not worry, we'll go over this in more detail in later sections.

<br><br> 


## Variable Naming

Another syntax-related topic is the naming of variables. Like the before topic, we have yet to go over this in more detail. At its core, a variable is a programmer-named storage location. When creating variables, a value must be initialized to the variable using the assignment operator **=**. Because of Python's dynamic typing, you do not have to specify the type of the variable prior to initialization. Also, the type of the variable can readily change. While Python is our friend when creating variables, we must abide by naming rules otherwise Python will throw an **SyntaxError**.<br>

### Naming Rules

| Ex | OK | BAD |
| -- | -- | --- |
|  1 | age = 32 | a ge = 32 **No spaces allowed! SyntaxError** |
|  2 | myName = "Mike" | my-Name = "Mike" **Cannot contain hyphens! SyntaxError** |
|  3 | Animal = "Zebra" | $Animal = "Zebra" **Cannot start with special characters! SyntaxError** |
|  4 | cost_33 = 1.22 | 33cost = 1.22 **Cannot start with number! SyntaxError** |
|  5 | pizza4free = True | pizza4.0free = True **Must not contain membership operator '.'! This will throw an SyntaxError.** |
|  6 | Olay = "Muahaha!" | O = "Muahaha!" **This is a bad practice. O is easy to confuse with numerical zero.** |
|  7 | idaho = "Yippee!" | I = "Yippee!" **This is a bad practice.** Is I = l? If so, you see why this is a bad practice. Capital i is easy to confuse with lowercase L. |
|  8 | lol = "lololol!" | l = "lololol!" **This is a bad practice.** For the same reason above. Likewise, lowercase L is easy to confuse with capital i. |

<br><br>

For more information on best practices when it comes to naming conventions see: [**PEP 8 Style Guide**](https://www.python.org/dev/peps/pep-0008/).


<br>


{need to continue...}
















