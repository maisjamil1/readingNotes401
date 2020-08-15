
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
