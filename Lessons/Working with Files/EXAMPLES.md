# Working with files

## Basic Python reading/writing files
- General formula to read/write a fil eis **open(file_name, flag)** that flag is **'w'** for writing and **'r'** for reading. Then **close()** after reading/writing files
- **NOTICE*:* The return of **open()** is **a file object, not content**. Hence, to truly read content, must call additional statements such as *read()* for reading text.
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
