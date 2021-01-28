# Working with files

## Basic Python reading/writing files
- General formula to read/write a file is **open(file_name, flag)** that flag is **'w'** for writing and **'r'** for reading. Then **close()** after reading/writing files
- **NOTICE**: The return of **open()** is **a file object, not content**. Hence, to truly read content, must call additional statements such as *read()* for reading text.
- 2 ways to use **open()** function:
	- Inline 
	```

	# read
	x = open('file1.txt', 'r')
	print(x.read()) # print content
	x.close() # close

	or

	print(open('file2.txt', 'r').read()) # no need to explicitly call close()

	# write 
	x = open('file3.txt', 'w')
	x.write('hello world')
	x.close()

	or 

	open('file4.txt', 'w').write('hello world') # no need to explicitly call close()
	```

	- Using **with** statement that is to simplify the file-stream management.
	```

	# read
	with open('file1.txt', 'r') as file:
		print(file.read()) # print content

	# write
	with open('file2.txt', 'w') as file:
		file.write('hello world')
	```

## Reading/Wring JSON files
- JSON is a special data structure mixed of dictionary-like and list-like. JSON format is heavily used in RESTful API. 
- Besides being heavily used mathematic computations for scientists & researchers, Python is used for Backend. Example Python-based backend packages such as Django, Flask, etc. Hence, learng to work with JSON files in python is crucial.
	- Inline
	```
	# read
	x = json.load(open('file.json', 'r'))

	# write, given x as a JSON object
	json.dumps(x, open('file.json', 'w'))
	```

	- Using **with** statement
	```
	# read
	with open('file.json', 'r') as file:
		x = json.load(file)

	# write, given x as a JSON object
	with open('file.json', 'w') as file:
		json.dumps(x, file)
	```

## Reading/Writing serialized data in Pickle files
- Sometimes, you want to read/write a big file in order to save memory. It's not common today, but it is still necessary in industry
- Package **pickle** can write any data types/structures into serialized data
- When reading **pickle** file, the returned object inherits the data type/structure of the file content.
- Use statement **open** with flags **rb** for reading and **wb** for writing
```

# write

## write list
l = ['hello', 1] # list
with open('list.pickle', 'wb') as file:
	pickle.dump(l, file)


## write dictionary
d = {'a' : 1, 'b' : 2, 'c' : 3} 
with open('dict.pickle', 'wb') as file:
	pickle.dump(d, file)

## write string
str = 'hello'
with open('str.pickle', 'wb') as file:
	pickle.dump(str, file)

# read
with open('list.pickle', 'rb') as file:
	l = pickle.load(file) # l inherits the list type of content in list.pickle
	print(type(l)) # >> list

with open('dict.pickle', 'rb') as file:
	d = pickle.load(file) # d inherits the dictionary type of content in dict.pickle
	print(type(d)) # >> dict
```
