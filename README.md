
# Reading Notes

## **Code 401** - _Advanced Software Development with Python_

### *Class 01 Reading*

#### Pain vs. Suffering

- Pain of growth is different than suffering
- One way to combat - keep your eye on the prize
- Ask questions, seek answers, and find a remedy

#### Beginner's guide to Big O Notations

- O(1): An algorithm that will always execute in the same time (or space) regardless of the size of the input data set.
- O(N): Algorithm whose performance will grow linearly and in direct proportion to the size of the input data set
- O(N2): Performance is directly proportional to the square of the size of the input data set.
- O(2N): Growth doubles with each additon to the input data set. (One of the worst case scenarios)

- ![Big O Cheat sheet](https://www.bigocheatsheet.com/)





### *Class 02 Reading*

#### In Tests We Trust — TDD with Python

- Test-Driven Development is a strategy to think tests-first.
- Tests can be considered as your living documentation, name of test should self-explain
- Test file name should follow the same name of module name
- AAA: Arrange, Act and Assert
- *Arrange* organize the data needed to execute that piece of code (input)
- *Act* execute the code being tested (exercise the behavior)
- *Assert* check if the result (output) is the same as you were expecting
- Write the test (fail), write the feature (pass), refactor

#### Recursion

- What is recursion (besides my worst nightmare?!)?
- The process in which a function calls itself is called recursion and the corresponding function is called as recursive function.
- Difference between direct and indirect recursion: 
- *Direct* Calls function directly
- *Indirect* Calls function through another function
- *Tail Recursion* is when that function is the last thing to be called

### *Class 03 Reading*

#### Reading and Writing Files in Python

[Reading and Writing Files in Python](https://realpython.com/read-write-files-python/)

- A file is a contiguous set of bytes used to store data. Can be anything as simple as a text file or as complicated as a program executable

> *Header*: metadata about the contents of the file (file name, size, type, and so on)
> *Data*: contents of the file as written by the creator or editor
> *End of file (EOF)*: special character that indicates the end of the file
</br>
</br>

> *Folder Path*: the file folder location on the file system where subsequent folders are separated by a forward slash / (Unix) or backslash \ (Windows)
> *File Name*: the actual name of the file
> *Extension*: the end of the file path pre-pended with a period (.) used to indicate the file type

- LF or \n to indicate a new line
- An encoding is a translation from byte data to human readable characters
- Parsing a file with the incorrect character encoding can lead to failures or misrepresentation of the character

- To open a file: `file = open('dog_breeds.txt')`
- Close a file example: 
`reader = open('dog_breeds.txt')`
`try:`
    `# Further file processing goes here`
`finally:`
    `reader.close()`
- REMEMBER: Try/Finally block

- Another way: Use a `with` block, automatically takes care of closing the file once it leaves the with block
- MODE: a specification on how you want to use that file
- Example with a   `with` block: 
`with open('dog_breeds.txt', 'r') as reader:`
    `# Further file processing goes here`
- 'r'	Open for reading (default)
- 'w'	Open for writing, truncating (overwriting) the file first
- 'rb' or 'wb'	Open in binary mode (read/write using byte data)

- .read(size=-1)	This reads from the file based on the number of size bytes. If no argument is passed or None or -1 is passed, then the entire file is read.
- .readline(size=-1)	This reads at most size number of characters from the line. This continues to the end of the line and then wraps back around. If no argument is passed or None or -1 is passed, then the entire line (or rest of the line) is read.
- .readlines()	This reads the remaining lines from the file object and returns them as a list.

- Can use a while loop to read a file or .readlines() method +  (end= statement)


#### Python Exceptions: An Introduction

[Python Exceptions: An Introduction](https://realpython.com/python-exceptions/)

- In Python, an error can be a syntax error or an exception
- *Syntax errors* : Occur when the parser detects an incorrect statement
- *Exception errors*: Occurs whenever syntactically correct Python code results in an error. *We can use raise to throw an exception if a condition occurs.*

Example: 
```x = 10```
```if x > 5:```
    ```raise Exception('x should not exceed 5. The value of x was: {}'.format(x))```

- *AssertionError exception*: Can be the last thing that the program will do or can use a try/except block
- Try/Except seems similar to a if else statement
- A try clause is executed up until the point where the first exception is encountered.
- Inside the except clause, or the exception handler, you determine how the program responds to the exception.
- You can anticipate multiple exceptions and differentiate how the program should respond to them.
- Avoid using bare except clauses.

### *Class 04 Reading*

#### Classes & Objects
- [Classes and Objects](https://www.learnpython.org/en/Classes_and_Objects)

- Objects are an encapsulation of variables and functions into a single entity
- Objects get their variables and functions from classes. 
- Classes are essentially a template to create your objects

- To access the variable inside of the newly created object, you'd call "className"."variableName" 
- You can create multiple different objects that are of the same class(have the same variables and functions defined). However, each object contains independent copies of the variables defined in the class

- To access a function inside of an object you use notation similar to accessing a variable, but ref the function name

#### Thinking Recursively in Python
- [Thinking Recursively in Python](https://realpython.com/python-thinking-recursively/)

- A recursive function is a function defined in terms of itself via self-referential expressions.
- A function will continue to call itself and repeat its behavior until some condition is met to return a result
- Thread the state through each recursive call so that the current state is part of the current call’s execution context
- Keep the state in global scope
- A data structure is recursive if it can be deﬁned in terms of a smaller version of itself.
- Recursion can also be seen as self-referential function composition. We apply a function to an argument, then pass that result on as an argument to a second application of the same function, and so on. Repeatedly composing attach_head with itself is the same as attach_head calling itself repeatedly.
- Python doesn’t have support for tail-call elimination. As a result, you can cause a stack overflow if you end up using more stack frames than the default call stack depth

























### *Class 05 Reading*
- Coming Soon

### *Class 06 Reading*
- Coming Soon

### *Class 07 Reading*
- Coming Soon

### *Class 08 Reading*
- Coming Soon

### *Class 09 Reading*
- Coming Soon

### *Class 10 Reading*
- Coming Soon

### *Class 11 Reading*
- Coming Soon

### *Class 12 Reading*
- Coming Soon

### *Class 13 Reading*
- Coming Soon

### *Class 14 Reading*
- Coming Soon

### *Class 15 Reading*
- Coming Soon

### *Class 16 Reading*
- Coming Soon

### *Class 17 Reading*
- Coming Soon

### *Class 18 Reading*
- Coming Soon

### *Class 19 Reading*
- Coming Soon

### *Class 20 Reading*
- Coming Soon












<!-- You can use the [editor on GitHub](https://github.com/testOrg762/reading-notes/edit/main/README.md) to maintain and preview the content for your website in Markdown files. -->


<!-- Syntax highlighted code block -->

<!-- # Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text -->

<!-- [Link](url) and ![Image](src) -->
```

