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

## Reading/Writing serialized data
