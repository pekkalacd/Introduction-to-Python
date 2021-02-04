# If, elif, and else

## If else
Similar to other programming languages, Python has its if-else statement but simplier and east-to-read formats.
If-else statement can be written in 2 formats: *inline* and *block*
```
# inline
x = 2
print(2 if x >= 2 else 0)
print(2 if x >=2) # invalid statement because inline if-else statements require else clause

# block
x = 2
if x >= 2:
	print(2)
else:
	print(0) 

if x >= 2:
	print(2) # else cause can be omitted
```

## Nested if-else
* In Python, nested if-else statements can be written either in *inline* or *block* formats. However, the nested *inline* if-else statements are not recommended due to its low readability.
```

# inline
x = 6 
print(10 if x >= 10 else 5 if x >=5 else 0)

# block
x = 6
if x >= 10:
	print(10)
else:
	if x>= 5:
		print(5)
	else:
		print(0)
``` 
* You can use *elif* instead of else-if blocks for high readability.
```
x = 6
if x >= 10:
	print(10)
elif x >= 5:
	print(5)
else:
	print(0)
```
