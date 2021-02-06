# Basic Operators
<br>

To begin working with programs it's important to understand **statements** versus **expressions**. A *statement* is a line of code that does something or performs an action. An *expression* is a line of code that when evaluated results in a True or False value, otherwise known as a **boolean value**. Together statements and expressions can be tied together in order to form a basic program.<br>

Writing programs requires that statements, along with expressions, be connected in a logical way. In order to do so, **operators** are used. There are a multitude of operators in Python: mathematical, comparison, bitwise, relational, membership, and identity. Each of these operator umbrellas contain multiple individual operators that perform specific tasks. Each of the individual operators, adhere to rules of **precedence** and **associativity** when used in conjunction with one another.<br>

This section will cover the general basics of each operator group.<br>

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

You'll notice in the column labeled *Type* that each of these operators are **binary**. This is not referring to binary in the sense of 1's and 0's, but rather to the requirement of needing two operands in order to function. An **operand** is an object or literal that is used in conjunction with an operator for a specific action to be done.
For example, in the statement ``2 + 3``, notice the addition operator **+** is surrounded by two integer-literals '2' and '3'. These are *operands*.<br>

### Precedence

The requirement for two operands **does not mean** that only two literals or objects can be operated upon at a time. More complex statements such as ``12+14+13/2*9//7%4`` can also be evaluated. Because statements like this *share* operands with other operators acting on those same operands, this is where **operator precedence** would need to be considered.<br><br>
**The higher the operator on this [chart](https://www.programiz.com/python-programming/precedence-associativity), the more *precedence* it takes over other operators if used in the same statement.**<br><br>

<p align="center">
   <img src="https://user-images.githubusercontent.com/34849400/107108718-ad7e7780-67ff-11eb-94d7-109e2bcc06aa.png"/>
</p>

<br><br>

Precedence is what dictates which operator performs its action first, before other operators. Consider the following example, looking at the previously given statement ``12+14+13/2*9//7%4``.<br><br>

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

### Addition Operator

Like mathematical addition, the *addition operator* functions as the addition, concatenation, and extension operator of Python's objects. It's a binary operator, meaning it requires two operands on either side of the **+** sign.<br>

```
   3+3
   # output => 6
   
   num = 2
   num2 = 3
   num+num2
   # output => 5
 ```
<br>

The addition operator takes two *operands* on either side of the sign and performs a specified action based on the type of the operands. With this, there are limitations to what can be *added*, so-to-speak, and what cannot. See the table below.<br>

| OPERATION  |  STATUS  |
| ----------  | -------- |
| int+int    |   **OK** |
| int+float  |  **OK**  |
| int+str    |  **ERROR** |
| int+list   | **ERROR**  |
| float+str  | **ERROR** | 
| set+list   | **ERROR** |
| dict+list  | **ERROR** |
<br>

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





