## Files & Exceptions

Real Python Tutorial - https://realpython.com/

### Exceptions

```
x = 10
if x > 5:
    raise Exception('x should not exceed 5. The value of x was: {}'.format(x))
```

#### The try and except Block: Handling Exceptions
The try and except block in Python is used to catch and handle exceptions. Python executes code following the try statement as a “normal” part of the program. The code that follows the except statement is the program’s response to any exceptions in the preceding try clause.

Warning: Catching Exception hides all errors…even those which are completely unexpected. This is why you should avoid bare except clauses in your Python programs. Instead, you’ll want to refer to specific exception classes you want to catch and handle. You can learn more about why this is a good idea in this tutorial.

https://realpython.com/the-most-diabolical-python-antipattern/


<img width="721" alt="Screen Shot 2021-05-19 at 10 02 12 AM" src="https://user-images.githubusercontent.com/45111611/118826243-502ba500-b889-11eb-9d08-795fe28b8e01.png">


There are several advantages to modularizing code in a large application:

**Simplicity**: Rather than focusing on the entire problem at hand, a module typically focuses on one relatively small portion of the problem. If you’re working on a single module, you’ll have a smaller problem domain to wrap your head around. This makes development easier and less error-prone.

**Maintainability**: Modules are typically designed so that they enforce logical boundaries between different problem domains. If modules are written in a way that minimizes interdependency, there is decreased likelihood that modifications to a single module will have an impact on other parts of the program. (You may even be able to make changes to a module without having any knowledge of the application outside that module.) This makes it more viable for a team of many programmers to work collaboratively on a large application.

**Reusability**: Functionality defined in a single module can be easily reused (through an appropriately defined interface) by other parts of the application. This eliminates the need to duplicate code.

**Scoping**: Modules typically define a separate namespace, which helps avoid collisions between identifiers in different areas of a program. (One of the tenets in the Zen of Python is Namespaces are one honking great idea—let’s do more of those!)

### Files

Files on most modern file systems are composed of three main parts:

 - **Header**: metadata about the contents of the file (file name, size, type, and so on)
 - **Data**: contents of the file as written by the creator or editor
 - **End of file (EOF)**: special character that indicates the end of the file

```file = open('dog_breeds.txt')```

You should *always* make sure that an open file is properly closed.

Two ways to ensure that you close a file.

```
reader = open('dog_breeds.txt')
try:
    # Further file processing goes here
finally:
    reader.close()
 ```
 
 And 
 
 ```
 with open('dog_breeds.txt') as reader:
    # Further file processing goes here
```

```.read(size=-1)```	This reads from the file based on the number of size bytes. If no argument is passed or None or -1 is passed, then the entire file is read.

```.readline(size=-1)```	This reads at most size number of characters from the line. This continues to the end of the line and then wraps back around. If no argument is passed or None or -1 is passed, then the entire line (or rest of the line) is read.

A common thing to do while reading a file is to iterate over each line. Here’s an example of how to use the Python .readline() method to perform that iteration:

```
>>> with open('dog_breeds.txt', 'r') as reader:
>>>     # Read and print the entire file line by line
>>>     line = reader.readline()
>>>     while line != '':  # The EOF char is an empty string
>>>         print(line, end='')
>>>         line = reader.readline()
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

    

