# FileIO & Exceptions

## FileIO 

### What Is a File? 

a file is a contiguous set of bytes used to store data, This data is organized in a specific format and can be anything as simple as a text file or as complicated as a program executable.

file parts :
- Header: contains (file name, size, type).
- Data: contents of the file as written by the creator or editor.
- End of File: a special character that indicates the end of the file.

### File Paths 

The file path is a string that represents the location of a file. It’s broken up into three major parts:
- Folder Path: the file folder location on the file system where subsequent folders are separated by a forward slash / (Unix) or backslash \ (Windows).
- File Name: the actual name of the file.
- Extension: the end of the file path pre-pended with a period (.) used to indicate the file type.

### Opening and Closing a File in Python

There are many ways to open a file, but the most important that you should make sure to close the file after you have done your work, This can lead to unwanted behavior including resource leaks. It’s also a best practice within Python (Pythonic) to make sure that your code behaves in a way that is well-defined and reduces any unwanted behavior.

below some examples to open a file and close it :

```
file = open('dog_breeds.txt')
```
```
reader = open('dog_breeds.txt')
try:
    # Further file processing goes here
finally:
    reader.close()
 ```
 
 ```
with open('dog_breeds.txt') as reader:
    # Further file processing goes here
 ```
 
 
 ### files type:
 There are three different categories of file objects:
 - Text files : ``` open('abc.txt', 'r') ```
 - Buffered binary files: ```open('abc.txt', 'rb') ```
 - Raw binary files: ``` file = open('dog_breeds.txt', 'rb', buffering=0) ```
 
 
 
### Reading and Writing Opened Files

#### Reading :
Here’s an example of how to read the entire file as a list using the Python .readlines() method:
``` 
>>> f = open('dog_breeds.txt')
>>> f.readlines()  # Returns a list object
['Pug\n', 'Jack Russell Terrier\n', 'English Springer Spaniel\n', 'German Shepherd\n', 'Staffordshire Bull Terrier\n', 'Cavalier King Charles Spaniel\n', 'Golden Retriever\n', 'West Highland White Terrier\n', 'Boxer\n', 'Border Terrier\n']
```

Iterating Over Each Line in the File :

```

>>> with open('dog_breeds.txt', 'r') as reader:
>>>     # Read and print the entire file line by line
>>>     for line in reader:
>>>         print(line, end='')
Pug
Jack Russell Terrier
English Springer Spaniel
German Shepherd
Staffordshire Bull Terrier
Cavalier King Charles Spaniel
Golden Retriever
West Highland White Terrier
Boxer
Border Terrier

``` 
 
 
 #### Writing:
 
 ``` 
 
 with open('dog_breeds.txt', 'r') as reader:
    # Note: readlines doesn't trim the line endings
    dog_breeds = reader.readlines()

with open('dog_breeds_reversed.txt', 'w') as writer:
    # Alternatively you could use
    # writer.writelines(reversed(dog_breeds))

    # Write the dog breeds to the file in reversed order
    for breed in reversed(dog_breeds):
        writer.write(breed)
        
    
 ``` 
 
 - - -
 
 ## Exceptions 
 
 ### Exceptions versus Syntax Errors
 
 Syntax errors occur when the parser detects an incorrect statement, the exceptions type of error occurs whenever syntactically correct Python code results in an error

### Raising an Exception
We can use ``` raise ``` to throw an exception if a condition occurs. The statement can be complemented with a custom exception.
#### below ex :

```
x = 10
if x > 5:
    raise Exception('x should not exceed 5. The value of x was: {}'.format(x))
    
```

 ### The try and except Block: Handling Exceptions
 
 The ``` try ``` and ``` except ``` block in Python is used to catch and handle exceptions
 
 #### ex :
 
 ``` 
 try:
    linux_interaction()
except AssertionError as error:
    print(error)
    print('The linux_interaction() function was not executed')
    
 ```
 
 we can determine the error type and print it on screen.
 #### ex:
```
 try:
    with open('file.log') as file:
        read_data = file.read()
except FileNotFoundError as fnf_error:
    print(fnf_error)
    
```
 
### The else Clause
we can use  ``` else ``` statement to execute the code if there is no error after ``` try ``` statement, and in case of error, the else statement will not be executed .

#### ex:
```
try:
    linux_interaction()
except AssertionError as error:
    print(error)
else:
    print('Executing the else clause.')
```

### Cleaning Up After Using finally 

``` finally ``` statemnt will be excuted no matter erorr ocurres in above statments .

#### ex:

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
 



