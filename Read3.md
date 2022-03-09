# opene 
## Files on most modern file systems are composed of three main parts:

   - Header: metadata about the contents of the file (file name, size, type, and so on)
   - Data: contents of the file as written by the creator or editor
   - End of file (EOF): special character that indicates the end of the file
# File Paths
The file path is a string that represents the location of a file. It’s broken up into three major parts:

    - Folder Path: the file folder location on the file system where subsequent folders are separated by a forward slash / (Unix) or backslash \ (Windows)
    - File Name: the actual name of the file
    - Extension: the end of the file path pre-pended with a period (.) used to indicate the file type
# Opening and Closing a File in Python
by open() built-in function. open() has a single required argument that is the path to the file. open() has a single return, the file object:
file = open('dog_breeds.txt')

|Character| Meaning|
| ----------- | ----------- |
|'r'|Open for reading (default)|
|'w'| Open for writing, truncating (overwriting) the file first|
|'rb' or 'wb'|Open in binary mode (read/write using byte data)|

after opening the file we should close it using the close function by insert it in the try stament 
or we can use a with satement to close the file by default 

# The try and except Block: Handling Exceptions
we use it with try to raise an error 
when syntactically correct code runs into an error, Python will throw an exception error. This exception error will crash the program if it is unhandled. The except clause determines how your program responds to exceptions.
except is used to catch and handle the exception(s) that are encountered in the try clause.
# The else Clause
In Python, using the else statement, you can instruct a program to execute a certain block of code only in the absence of exceptions.

# Using finally
Imagine that you always had to implement some sort of action to clean up after executing your code. Python enables you to do so using the finally clause
everything in the **finally** clause will be executed. It does not matter if you encounter an exception somewhere in the try or else clauses. 
finally enables you to execute sections of code that should always run, with or without any previously encountered exceptions.
