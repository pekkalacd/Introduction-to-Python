# Basic Operators
<br>

To begin working with programs it's important to understand statements versus expressions. A *statement* is a line of code that does something or performs an action. An *expression* is a line of code that when evaluated results in a True or False value, otherwise known as *boolean* values. Together statements and expressions can be combined to form a basic program.<br>

In order to connect these statements and expressions, we use **operators**. There are a multitude of operator umbrellas in Python: mathematical, comparison, bitwise, relational, membership, and identity. Each of these groups contain multiple individual operators that perform specific tasks. Each of the individual operators, adhere to rules of **precedence** and **associativity** when used in conjunction with one another.<br>

This section will cover the general basics of each operator group.<br>

### Unary, Binary, and Ternary

Operators require the use of *operands* in order to perform some action or evaluate an expression. An **operand** is an object or literal that is used in conjunction with an operator. In most languages, there are three kinds of operators: *unary*, *binary*, and *ternary*. A **unary operator** requires one operand that sits to the right of the operator. A **binary operator** requires two operands which sit on either side of the operator. And a **ternary operator** requires two operands on either side and an additional one on a single side.<br>

In Python, there are no ternary operators. However, *ternary expressions* can still be formed. Most commonly, binary and unary operators are used. Generally, the format of using each of those is as follows.<br>

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

In other languages, the **?** ternary operator might be used to form ternary expressions. A ternary expression is commonly associated with if-else chains as a viable alternative. The way a ternary expression is evaluated in Python is: <br>
``{result if expression is true} if {expression} else {result if expression is false}``.<br>

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

For the sake of the rest of this lesson, we will not be focusing as much on ternary expressions, but we might come back to them as alternatives in the if-elif-else lesson.

### Precedence and Associativity

Before we get started into the specific operator umbrellas, consider the subheading. The *precedence* of an operator determines when that operation will be applied. When programmers talk about precedence, they are usually referring to the use of multiple types of operators in a specific statement.<br>

For example, in mathematics, if we wanted to evaluate ```2 + 3 * 5``` we might refer to **PEMDAS** which is the acronym for the *order of operations*; that is, **P**arentheses, **E**xponents, **M**ultiplication, **A**ddition, and **S**ubtraction. The earlier an operation resides in the acryonym, PEMDAS, the more *precedence* that operation has over the others.<br>

For example, in evaluating ``2 + 3 * 5`` we'd do:<br>
``
    2 + (3*5)  # since multiplication 'M' comes before addition 'A' in 'PEMDAS'
    2 + 15     # now, we'd add since there's only 1 operator left
    17
``

<br>

Much like in mathematics, operators in programming languages also abide by their own order of operations. <br><br>
**The order at which statements or expressions are evaluated is dictated by *operator precedence***.<br>

See the following [chart](https://www.programiz.com/python-programming/precedence-associativity) below for more clarification. The higher an operator is, the more precedence it has over other operators. Meaning if two or more different operators are used in the same statement, the operation whose operator has the highest precedence will happen first.<br>

<p align="center">
   <img src="https://user-images.githubusercontent.com/34849400/107108718-ad7e7780-67ff-11eb-94d7-109e2bcc06aa.png"/>
</p>

For more information on operator or keyword precedence, you can access information directly in the Python interpreter by typing an operator in a string and inserting it into the help function like so **``help('+')``**. <br>

Now, consider the following example which evaluates ``12+14+13/2*9//7%4``. This statement uses multiple operators. So, we must refer to precedence when evaluating.<br><br>

```
  12+14+13/(2*9)//7%4              # happens 1st, since * has the highest precedence
  12+14+(13/18)//7%4               # happens 2nd, since / has the next highest precedence 
  12+14+(0.7222222222222222//7)%4  # happens 3rd, since // has the next highest precedence
  12+14+(0%4)                      # happens 4th, since % has the next highest precedence
  (12+14)+0                        # happens 5th, since + and + are same, left-to-right associativity kicks in
  26+0                             # happens last, since there's only 1 + left, this is evaluated
  
  # output => 26
```
<br>

Along with the concept of operator precedence is **associativity**. 

{write more about Python associativity}

### Mathematical Operators
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

For *Lists*, this operator serves to *extend* the left list by the right list. This can also be accomplished by using the ```list.extend(list_object)``` member-function or method of the builtin List class.<br>

```
   List1 = [1,2,3]
   List2 = [4,5,6]
   List1.extend(List2)
   # output => [1,2,3,4,5,6]
   
   List2.extend(List1)
   # output => [4,5,6,1,2,3]
   
   List1 + List2
   # output => [1,2,3,4,5,6]
   
   List2 + List1
   # output => [4,5,6,1,2,3]
 ```
 <br>

{keep working on this...}





