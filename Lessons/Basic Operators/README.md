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

### Addition Operator

Like mathematical addition, the *addition operator* functions as the addition, concatenation, and extension operator of Python's objects. It's a **binary operator**, meaning it requires two **operands** on either side of the **+** sign.<br>

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
<br>

There is a reason for this linearity in the concatenation of strings and it's in the definition of a string, being an *array of characters*. In other languages like C, strings
are formed other ways that are a little more obvious of this definition: ```char string[] = "hello there my friend!"; ```. An array is a linear data structure which can hold multiple objects or literals in **contiguous memory**.<br>

*Contiguous Memory* is memory that is stored one after the other in a linear fashion. A high-level abstraction of what this might look like is below.<br>

<p align="center">
   <img src=" "/>
</p>


{keep working on this...}





