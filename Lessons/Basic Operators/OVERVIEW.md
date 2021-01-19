# Basic operators

--

## Arithematic operators
- Basic operators: sum : **+** | subtract : **-** | multiply : ***** | mivide : **/**
```

# sum
print(2 + 2) # output >> 4

# subtract
print(2 - 2) # output >> 0

# multiply
print(2 * 2) # output >> 4

# divide
print(4 / 2) # output >> 2.0
```

- Special notes for **Division**
	- **/** - float divisoin returns *float*
	- **//** - floor division returns the next lower whole number
	- **&** - modules return remainder of the division
	```
	print(5 / 3) # output >> 1.667
	print(5 // 3) # output >> 1
	print(5 & 3) # output >> 2
	``` 

- Exponent __**__
```
print(2**3) # output > 8
```

## Comparison operators
- __less than < __ and __less than or equal to <=__
```
print(2 < 3) # output >> True
print(2 <= 2) # output >> True
```
- __greater than >__ and __greater than or equal to >=__
```
print(2 > 3) # output >> False
print(2 >= 2) # output >> True
```
- __equal ==__ and __different !=__
```
print(2 == 2) # output >> True
print(2 != 2) # output >> False
```

## Logical operators
```
# x and y - returns True if both operands are True. Otherwsie, returns False
print(2 > 1 and 3 > 1) # output >> True
print(2 > 1 and 3 < 1) # output >> True

# x or y - return True if at least one of operands is True. Otherwise, returns False
print(2 > 1 or 3 < 1) # output >> True
print(2 > 1 or 3 > 1) # output >> True
print(2 < 1 or 3 > 1) # output >> True
print(2 < 1 or 3 < 1) # output >> False

# not x - negates the following term
print(not 2 < 1) # output >> True
print(not 2 < 1 or 3 > 1) # output >> True
print(not 2 > 1 and 3 > 1) # output >> True
```

## Assignmet operators
* **=** is used to assign a implict-type to a variable. \n No need to initialize variable or define type of variable in advance as Python cast data type implicitly for appropriate functions.
```

# numbers
x = 2
print(x) # output >> 2
print(x + 4.0) # output >> 4.0

# string
x = 'hello world'
print(x) # output >> hello world
```

* Compound assignment operators
```
# simply combine operator and '='
x = 2

x += 2 # output >> 4
x -= 1 # output >> 3
x /= 3 # output >> 1.0
x *= 100 # output >> 1.0
x **= 4 # output >> 1.0
```

## Special operators
Python has special operators, such as **Identity** and "Membership** operators

### Identity operator: is / is not
**is** and **is not** act as equal-comparison operator and return True/False
```
x = 'washington'
print(x is 'washington') # output >> True
print(x is not 'trump') # output >> True

x = 2
print(x is 2) # output >> True
print(x is not 2) # output >> False
```
### Membership operator: in / not in
**in** and **in not** check if an element exists in a list
```
x = [2, 3, 4, 5] # define a list (called 'array' in other languages)

print(2 in x) # output >> True
print(10 in x) # output >> True
print(10 not in x) # output >> True
```

