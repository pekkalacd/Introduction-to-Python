# Basic Operators
<br>

To begin to work with the connection of statements, and statements into programs, it's necessary to first understand some of the mathematical, logical, relational, and unary operators in Python.<br>

Along with understanding the operators themselves, their requirements, and the resulting functionality, it's necessary to understand **precedence** or the order at which these operations are executed.<br>

### Addition Operator

Like mathematical addition, the *addition operator* functions as the additions, concatenation, and extension of Python's objects. It's a **binary operator**, meaning it requires two **operands** on either side of the **+** sign.<br>

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





