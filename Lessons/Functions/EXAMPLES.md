# Functions

---

## Function definition
A Python function can be defined using the below statement
```
def myfunc(arg_1, arg_2, arg_3, *args, **kwargs): # list of arguments
	# codes here
	pritn("hello world")
```
* ***args** and ****kwargs** allow you pass in unspecificed arguments to the function. Hence, when use them, you do not need to know the exact number of arguments. 
* ***args** represents the list of non-keyworded arguments right after the named arguments
* ****kwargs** represents the keyworded arguments. Hence, **kwargs is similair to dictionary strucutre.
```

# *args
def myfunc(arg, *args):
	print(arg)
	for x in args:
		print(x)

myfunc('eric', 'john', 'kevin')
>> eric
john
kevin

# **kwargs
def myfunc(arg, **kwargs):
	print(arg):
	print(kwargs['last_name'])
	print(kwargs['email'])
	print(kwargs['number'])

myfunc('eric', name='ngo', email='non@existing.com', number='0101010101')
>> eric
ngo
non@existing.com
0101010101
```

## Lambda function
Instead of definining a block function, you can lazily define a simple function using **lambda** statement
```
x = lambda i: i + 1

pritn(x(2))
>> 3
```
* Lambda function accepts multilple arguments of various types and return only 1 output.
```
# 2 arguments
x = lambda i, j: i + j

print(x(1,2))
>> 3

# argument as list
x = lambda x: sum(x)

print(x([1,2,3])
>> 6
```
* Instead of returning value, **lambda function** may execute simple statements
```
# with if-else 
x = lambda x: x + 1 if x > 2 else x - 1

print(x(4))
>> 5

# with loop
x = lambda x, y: [i + y for i in x]
print(x([1,2,3], 2))
>> [3,4,5]
```
