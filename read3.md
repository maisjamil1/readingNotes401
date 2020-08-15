
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

## Reading an Opened Files
- .read(size=-1)	This reads from the file based on the number of size bytes. If no argument is passed or None or -1 is passed, then the entire file is read.
- .readline(size=-1)	This reads at most size number of characters from the line. This continues to the end of the line and then wraps back around. If no argument is passed or None or -1 is passed, then the entire line (or rest of the line) is read.
- .readlines()	This reads the remaining lines from the file object and returns them as a list.

## Writing inside an opened file

- .write(string)	This writes the string to the file.
- .writelines(seq)	This writes the sequence to the file. No line endings are appended to each sequence item. It’s up to you to add the appropriate line ending(s).

______________________________________________________
# Python Exceptions
![img](https://files.realpython.com/media/intro.8915db1758d8.png)

### Raising an Exception
We can use raise to throw an exception if a condition occurs. The statement can be complemented with a custom exception.
```
x = 10
if x > 5:
    raise Exception('x should not exceed 5. The value of x was: {}'.format(x))
```
### The AssertionError Exception ____assert ()
 We assert that a certain condition is met. If this condition turns out to be True, then that is excellent! The program can continue. If the condition turns out to be False, you can have the program throw an AssertionError exception.
 
### In the try clause, all statements are executed until an exception is encountered.

### except is used to catch and handle the exception(s) that are encountered in the try clause.

### else lets you code sections that should run only when no exceptions are encountered in the try clause.

### finally enables you to execute sections of code that should always run, with or without any previously encountered exceptions.
```
try:
    linux_interaction()
except AssertionError as error:
    print(error)
else:
    try:
        with open('file.log') as file:
            read_data = file.read()
    except FileNotFoundError as fnf_error:
        print(fnf_error)
finally:
    print('Cleaning up, irrespective of any exceptions.')
```
