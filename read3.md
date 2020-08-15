
# Reading and Writing Files in Python 
###  a file is a contiguous set of bytes used to store data. 

Files on most modern file systems are composed of three main parts:

- Header: metadata about the contents of the file (file name, size, type, and so on)
- Data: contents of the file as written by the creator or editor
- End of file (EOF): special character that indicates the end of the file

## Opening and Closing a File in Python
```
reader = open('dog_breeds.txt')
try:
    # Further file processing goes here
finally:
    reader.close()
```

### positional argument mode
This argument is a string that contains multiple characters to represent how you want to open the file. The default and most common is 'r
- 'r'	Open for reading (default)
- 'w'	Open for writing, truncating (overwriting) the file first
- 'rb' or 'wb'	Open in binary mode (read/write using byte data)
