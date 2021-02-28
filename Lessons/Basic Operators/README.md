# Basic Operators
<br>

To begin working with programs it's important to understand statements versus expressions. A *statement* is a line of code that does something or performs an action. An *expression* is a line of code that when evaluated results in a True or False value, otherwise known as *boolean* values. Together statements and expressions can be combined to form a basic program.<br>

In order to connect these statements and expressions, we use **operators**. There are a multitude of operator umbrellas in Python: mathematical, assignment, unary, comparison,  relational, membership, identity, and more. Each of these groups contain multiple individual operators that perform specific tasks. Each of the operator groups, have their own *precedence* and *associativity* that is invoked when used in conjunction with other operators.<br>

This section will cover the general basics of each operator group.<br><br>

### Unary, Binary, and Ternary

Operators require the use of *operands* in order to perform some action or evaluate an expression. An **operand** is an object or literal that is used in conjunction with an operator. In most languages, there are three kinds of operators: *unary*, *binary*, and *ternary*.<br>

A **unary operator** requires one operand that sits to the right of the operator. A **binary operator** requires two operands which sit on either side of the operator. And a **ternary operator** requires two operands on either side and an additional one on a single side.<br>

Most commonly, binary and unary operators are used. Generally, the format of using each of those is as follows.<br>

```
   # unary: {operator}(operand)
   # examples:
           ~12
           # output => -13    (~ is unary 'invert' operator: ~x = -(x+1))
          
           -123
           # output => -123   (- is unary minus: -x = 'negative' x)
           
           +123
           # output => 123    (+ is unary plus: +x = x)
   
   
   # binary: (operand) {operator} (operand)
   # examples:
          
          2 + 3
          # output => 5       (+ is addition operator)
          
          2 - 3
          # output => -1      (- is subtraction operator)
          
          True and False
          # output => False   ('and' is logical AND operator)
          
          1 << 2
          # output => 4       (<< is left-shift:  x << y = x(2^y) )
 ```
<br>

In other languages, the **?** ternary operator might be used to form ternary expressions. A ternary expression is commonly associated with if-else chains as a viable alternative. The way a ternary expression is evaluated in Python is:<br><br>
```{result if expression is true} if {expression} else {result if expression is false}```<br>

Consider the sample below, where we're determining if the number 32 is even or odd and printing whether it is or isn't.<br>

```
  num = 32
  
   # normal if-else
  if num % 2 == 1:
         print(f"{num} is odd!")
  else:
         print(f"{num} is even!")
         
  # output => 32 is even!
 
 
  # ternary if-else
  print(f"{num} is odd!" if num % 2 == 1 else f"{num} is even!")
  
  # output => 32 is even!

```
<br>

For the sake of the rest of this lesson, we will not be focusing as much on ternary expressions, but we might come back to them as alternatives in the if-elif-else lesson.<br>
<br>
### Assignment Operator

You've seen this operator used many times already. The assignment operator **=** is a binary operator used to assign a value to the right of it to the memory location on the left. In an earlier lesson, when discussing [Variables](https://github.com/pekkalacd/Introduction-to-Python/tree/master/Lessons/Variables), a variable was stated to be a named storage location. It is a space in memory which contains **an address and a value**. The address is *where* that object is in RAM and the value is *what* that space holds.<br>

```
   {object} = {value}
   
   dog = "sparky"
   # dog is a variable, it's the object
   # "sparky" is a string and it's the value stored in the variable 'dog'
   
   # displaying address of 'dog'
   print(hex(id(dog)))
   
   # displaying value inside 'dog' ~ "sparky"
   print(dog)
   
   # output =>  0x252f8ef2af0
                sparky
```
<br>

The object to the left of the assignment operator **must have a location**. This is because the assignment operator does 3 things.<br><br>
**Steps of the assignment operator:**<br>
   **1. Reduces the right value to a single type**<br>
   **2. Assigns the right value to the left object's location in memory**<br>
   **3. Returns the left object**<br>
<br><br>
If the left object does not have a space in memory for Python to refer to, using the assignment operator will not work. 
<br><br>

```
   2 = 2
   # output => SyntaxError: cannot assign to literal
   
   "person" = "fun"
   # output => SyntaxError: cannot assign to literal
   
   [1,2,3] = [1,2]
   # output => SyntaxError: cannot assign to literal 
```
<br>

When working with structures such as lists these lines can be *blurred* easy, but the principle is the same. A list contains a collection of memory locations. Each index of a list has it's own unique memory address. So, when assigning values to a specific index of a list, this is seen as equivalent as assigning a value to a space in memory.<br>

```
   dog = ["sparky","bones","fred"]
   dog[-1] = "toby"
   print(dog)
   # output => ["sparky","bones","toby"]
```
<br>

If we try to do similar for strings, we'll come across a **TypeError** since strings are *immutable*.<br>

```
   dog = "moby"
   dog[0] = "t"
   # output => TypeError: 'str' object does not support item assignment
```
<br>

We'll continue using the assignment operator throughout the rest of this lesson and other lessons moving forward, so if there was one operator to completely familiarize with, it'd be this one.

<br>

### Precedence

Before we get started into the specific operator umbrellas, consider the subheading. The *precedence* of an operator determines when that operation will be applied. When programmers talk about precedence, they are usually referring to the use of multiple types of operators in a specific statement.<br>

For example, in mathematics, if we wanted to evaluate ```2 + 3 * 5``` we might refer to **PEMDAS** which is the acronym for the *order of operations*; that is, **P**arentheses, **E**xponents, **M**ultiplication, **A**ddition, and **S**ubtraction. The earlier an operation resides in the acryonym, PEMDAS, the more *precedence* that operation has over the others.<br>

For example, in evaluating ``2 + 3 * 5`` we'd do:<br>

```
    2 + (3*5)  # since multiplication 'M' comes before addition 'A' in 'PEMDAS'
    2 + 15     # now, we'd add since there's only 1 operator left
    17
```

Much like in mathematics, operators in programming languages also abide by their own order of operations. <br><br>
  1. The order at which statements or expressions are evaluated is dictated by *operator precedence*.<br>
  2. If two operators with different levels of precedence are in the same statement or expression, the operator with the higher precedence will execute first.<br><br>

<p align="center">
   <img src="https://user-images.githubusercontent.com/34849400/107112326-6652af80-681c-11eb-89a1-accad15c0898.png"/>
</p>
<br>

For more information on operator or keyword precedence, you can access information directly in the Python interpreter by typing an operator in a string and inserting it into the help function like so **``help('+')``**. <br><br>

### Associativity

Sometimes a statement or expression will contain two or more operators on the same level precedence. For example, if //, /, and % were all used in the same statement, which one would execute first?<br>

This would be a scenario where *associativity* would come into play.

**Rules of Associativity:**<br>
   **1. Two operators share the same operand**<br>
   **2. Each operator is on the same level of precedence**<br>
<br>

**If these two conditions are met, then statements or expressions are evaluated associatively, not by precedence.**<br><br>

<p align="center">
   <img src="https://user-images.githubusercontent.com/34849400/107112096-900ad700-681a-11eb-8180-e0544de05bb0.png"/>
</p>

<br><br>

If associativity has kicked in, then we know that there are two operators on the same level of precedence that share an operand.<br>
 - **Left-to-Right associativity** means that we process the left operator first, then the right one.<br>
 - **Right-to-Left associativity** is the opposite; we process the right operator first, then the left one.<br>
 <br>


#### Associativity in Action

```
   We want to evaluate 50//10*32/31*8//4.  
   All *, /, // are multiplicative operators and share operands with each other.
   
   
   (50//10)*32/31*8//4        # // and * share operand 10, left-to-right associativity
   (5*32)/31*8//4             #  * and / share operand 32, left-to-right associativity
   (160/31)*8//4              # / and * share operand 31, left-to-right associativity
   (5.161290322580645*8)//4   #  * and // share operand 8, left-to-right associativity
   41.29032258064516//4       # only // remains
   
   # output => 10.0
```
<br><br>

#### Combining Precedence & Associativity Rules

Consider the following example which evaluates ``12+14+13/2*9//70%4**2``. This statement uses multiple operators that have varying levels of precedence and associativity. So, we must refer to precedence and associativity rules when evaluating.<br><br>

```
  12+14+13/2*9//70%(4**2)              # ** has the highest precedence
  12+14+(13/2)*9//70%16                # all multiplicative operators have higher precedence than additive. 
                                         And / and * share the operand 2. So, this is left-to-right associativity.
                                         
  12+14+(6.5*9)//70%16                 # * and // share operand 9, left-to-right associativity.
  12+14+(58.5//70)%16                  # // and % share operand 70, left-to-right associativity.
  12+14+(0.0%16)                       # % has a higher precedence than +.
  (12+14)+0.0                          # same operator, additive are left-to-right associativity.
  26+0.0                               # only 1 operator left.
  
  # output => 26.0
  
```

<br><br><br>

## Mathematical Operators
<br>
Mathematical operators, as the name implies, are responsible for performing mathematical operations on numeric data-types such as addition, subtraction, multiplication, division, floor-division, modulation, and exponentiation. Consider the table below for the Python representation of each.<br><br>

| Operator |  Name  |   Type    | Purpose  |
| -------- | ------ | --------- | -------- |
|**+**| addition | binary | adds, concatenates, extends two operands of numeric, string, or list types, respectively |
|**-**| subtraction | binary | subtracts two operands of numeric type and returns their difference |
|  *  | multiplication | binary | multiplies two operands of numeric and returns their product |
|**/**| division | binary | divides two operands of numeric type and returns their quotient as a float |
|**//**| floor-division | binary | divides two operands of numeric type and returns their integer divsion |
|**%** | modulus | binary | divides two operands of numeric type and returns their remainder as an integer |
|  **  | exponential | binary | exponentiates the left by the right numeric operand|
<br><br>

### Addition Operator

Like mathematical addition, the *addition operator* functions as the addition of two numeric operands and it's commutative. In Python, this operator is also responsible for string concatenation and can be used to extend Lists. It's a binary operator, meaning it requires two operands on either side of the **+** sign.<br>

```
   3+3
   # output => 6
   
   num = 2
   num2 = 3
   num+num2
   # output => 5
 ```
<br>

There are certain data-types we can apply the addition operator to and others that we cannot.<br>

<p align="center">
   <img src="https://user-images.githubusercontent.com/34849400/107110273-369bab80-680c-11eb-84d7-75428794ccc4.png"/>
</p>

While numeric types are generally in the clear when using the addition operator, there are some combinations of operand types that cannot be added. See the table above.<br><br>

For *strings*, the addition operator is the mode of ***concatenation***. Two or more strings, with each pair separated by the addition operator will be combined or concatenated
together linearly.<br>

```
   string1 = "hello"
   string2 = " there"
   string3 = " my friend!"
   
   phrase = string1 + string2 + string3
            # (string1 + string2) -> "hello" + " there" -> "hello there"
            # ("hello there" + string3) -> "hello there" + " my friend!" -> "hello there my friend!"
   
   print(phrase)
   # output => 'hello there my friend!'
```
<br><br>

For *Lists*, this operator serves to *extend* the left list by the right list. Similarly, the .extend() method on list types can also be used to modify an existing list.<br>

```
   List1 = [1,2,3]
   List2 = [4,5,6]
   List3 = [7,8,9,10]
   List1 + List2 + List3
   # output => [1,2,3,4,5,6,7,8,9,10]
   
   List1.extend(List2)   # ~ List1 = List1 + List2 = [1,2,3] + [4,5,6]
   List1.extend(List3)   # ~ List1 = List1 + List3 = [1,2,3,4,5,6] + [7,8,9,10]
   List1 
   # output => [1,2,3,4,5,6,7,8,9,10]
   
 ```
 <br><br>
 
 ### Subtraction Operator
 
In the scope of mathematics, subtraction can be viewed in multiple ways. Generally, it's seen as the sum of a positive number and a negative number: x + y = x + (-y).<br>

In Python, the subtraction functions similarly to the mathematical version. It can be used to find the difference between two numeric types or sets of elements. Unlike the addition operator,the subtraction operator **does not work on strings or lists**.<br>

```
  A = 13
  B = 2
  A - B
  # output => 11
  
  s1 = set([1,2,3])
  s2 = set([1,2])
  s1 - s2
  # output => {3}
```
<br>

The above use of the subtraction operator for numeric types is straight forward, but the usage of the operator with sets might not be.<br>

In discrete mathematics, a set is an object containing distinct values where multiplicity and order do not matter. For example, the set of elements in the sequence 11111232131233123132 would only be {1,2,3} since these are the *distinct values* and *multiplicity* (or the amount of which each value occurs) is irrelevant, and since order doesn't matter the set {1,2,3} would be the same as {2,3,1} or {3,2,1} and so on.<br>

The difference of two sets A and B is the set of elements that are contained within A that are not in B. Oppositely, the difference between a set B and
a set A is the set of elements in B that are not in A. This difference can be computed using the subtraction operator in Python.<br>

```
   A = {1,23}
   B = {1}
   A - B
   # output => {23}  since 23 is in A but not in B
   
   B - A
   # output => set()  or empty set object since all of the elements of B -  1 - are also in A.
```
<br>

Just as it was with addition, there are certain types that can be subtracted from one another and those that cannot.<br>

<p align = "center">
   <img src = "https://user-images.githubusercontent.com/34849400/108668207-600d3600-74a0-11eb-8f4b-fcfe95c9c516.png"/>
</p>

**note: || is 'or'**<br>

<br><br>

 ### Multiplication Operator <br>
 
 The multiplication operator, much like mathematical multiplication, generally, returns the product of two numerical operands. However, unlike mathematical multiplication,
 this operator ***can be used in combination with numeric and non-numeric types***. The multiplication operator is marked by ``*`` and is a binary operator requiring two operands. <br>
 
 Generally, the syntax is as follows:<br>
 
 ```
    {type} * {type}
    
    # for numeric-types
    32 * 2
    32.4 * 2

    # output => 64
                64.8 
    
    # for numeric & non-numeric
    3 * "abc" 
    2 * [1,2,3]
    
    # output => "abcabcabc"
                [1,2,3,1,2,3]
   
```
<br>

Part of the 'magic' of this operator lies in mathematics. Multiplication is the subsequent addition of traditionally numeric types a certain number of times. So, for a list like [1,2,3] that is multiplied by 2, we're adding together the lists [1,2,3] + [1,2,3], and by addition operator rules, under extension, [1,2,3,1,2,3] is returned. Likewise, for another *iterable* such as a string like "abc", 3 * "abc" is "abc" + "abc" + "abc" and by addition operator rules, under concatenation, "abcabcabc" is returned.<br>

Much like the other mathematical operators, there are some operand-types which cannot be multiplied together.<br>

<p align = "center">
   <img src = "https://user-images.githubusercontent.com/34849400/108669507-cb580780-74a2-11eb-963d-c634f8bb0d78.png"/>
</p>

<br><br>

### Division Operator

In Python, the division operator is marked by a single backslash ``/``. This operator is binary and **returns a float type** when used. It is constrained to the same constraints as mathematics in that, you cannot divide by zero, nor by some structure that is non-numeric. And likewise, the numerator cannot be a non-numeric structure. Unlike the multiplication operator, division cannot be broken up into the subsequent sum of partial elements.<br>

Syntax for using the division operator is as followed.<br>

```
    {type} / {type} -> float
    
    # using integers
    2 / 2
    
    # output => 1.0
    
    # using floats
    
    2.0 / 2.0
    
    # output => 1.0
    
    # using integers and floats
    
    2 / 3.0
    
    output => 0.6666666666666666

```
<br>

Other languages like C/C++ have a default *precision* value for how many decimal places a number will be displayed to, in Python, the default precision value is **about 15 digits after the decimal** or *double precision*.<br>

There are some types that may not be divided by each other. Below is a table describing them.<br>

<p align="center">
   <img src="https://user-images.githubusercontent.com/34849400/109402753-2021d500-791e-11eb-84a2-11ce416f5099.png"/>
</p>
<br>

A point of interest, as we'll discuss shortly, is what Python does with **boolean** values that are used in conjunction with mathematical operators. A **True** value is evaluated as the integer 1 and a **False** value is treated as the integer 0. When dividing, we cannot divide by 0, as this will trigger a **ZeroDivisionError** in Python. But using this knowledge, we can do some weird calculations as well.<br>

```
   (2 + True)/(True + 3*False)
   # (2 + 1) / (1 + 3*0)
   # (3) / (1)
   # output => 3.0
```
<br><br>

### Floor-Division Operator

Similar to the division operator, the floor-division operator marked by **//** is a binary operator which divides a left-value by the right-value. Differently, this operator returns an **integer** that is equal to or less than the normal quotient of the left and right values.<br>

In mathematics, a **floor** function, written **floor(x)**, takes a real number **x** and returns the greatest integer that is less than or equal to x. In Python, using the math library, we can access this same functionality.<br>

```
   from math import floor
   x = 3.4
   floor(x)
   # output => 3 
   
   y = 5.9
   floor(y)
   # output => 5
```
<br>

The floor function *truncates* the floating point or decimal portion of the input that is put in and returns just the integer portion. This can also be achieved by **casting** or converting the input to an integer using **int(x)**.<br>

Similarly, **floor-division** does the same thing. Consider, the following.<br>

```
    x = 2
    y = 3
    x/y
    # output => 0.66666666666666666
    
    int(x/y)
    # output => 0
    
    floor(x/y)
    # output => 0
    
    x // y
    # output => 0
```
<br>

So, **//** takes care of the truncation of the decimal portion of the quotient without needing to use an external library or casting the quotient to an integer.<br>

As all operators before it, there are some types that cannot be used with one another separated by **//**.<br>

















