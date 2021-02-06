# Basic Operators
<br>

To begin working with programs it's important to understand statements versus expressions. A *statement* is a line of code that does something or performs an action. An *expression* is a line of code that when evaluated results in a True or False value, otherwise known as *boolean* values. Together statements and expressions can be combined to form a basic program.<br>

In order to connect these statements and expressions, we use **operators**. There are a multitude of operator umbrellas in Python: unary, mathematical, comparison, bitwise, relational, membership, and identity. Each of these groups contain multiple individual operators that perform specific tasks. Each of the operator groups, have their own *precedence* and *associativity* that is invoked when used in conjunction with other operators.<br>

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

If these two conditions are met, then statements or expressions are evaluated associatively, not by precedence. The rules for associativity vary by precedence level.<br><br>

<p align="center">
   <img src="https://user-images.githubusercontent.com/34849400/107112096-900ad700-681a-11eb-8180-e0544de05bb0.png"/>
</p>

<br><br>

#### Associativity in Action

```
   We want to evaluate 50//10*32/31*8//4.  
   All *, /, // are multiplicative operators and share operands with each other.
   
   
   (50//10)*32/31*8//4        # all //, *, / have same precedence and share operand 10, left-to-right associativity
   (5*32)/31*8//4             #  * and / share operand 32, left-to-right associativity again
   (160/31)*8//4              # / and * share operand 31, so left-to-right again
   (5.161290322580645*8)//4   #  * and // share operand 8, so left-to-right again
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
|  **  | exponential | binary | exponentiates the left numeric operand by the right numeric operand and returns the result as a float |
<br>

You'll notice in the column labeled *Type* that each of these operators are **binary**. This is not referring to binary in the sense of 1's and 0's, but rather to the requirement of needing two operands in order to function.<br>

### Addition Operator

Like mathematical addition, the *addition operator* functions as the addition, concatenation, and extension operator of Python's objects. It's a binary operator, meaning it requires two operands on either side of the **+** sign, and it's commutative.<br>

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

The addition operator takes two *operands* on either side of the sign and performs a specified action based on the type of the operands. With this, there are limitations to what can be *added*, so-to-speak, and what cannot. See the table below.<br><br>

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
 <br>

{keep working on this...}





