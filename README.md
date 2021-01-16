
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

### *Linked List Reading*

What is a data structure?

- A data structure is a collection of data values, the relationships among them, and the functions or operations that can be applied to the data. 
Examples include: variables, arrays, hashes, and objects
How is a Linked List different from an array?

Arrays are more rigid, more difficult to change & memory management

- Arrays are static data structures where linked lists are dynamic

What is one benefit a Linked List has over an array?

- It is simpler to change a linked list than it is to change an array
What data does a Node hold in a Doubly Linked List?

- Sequentially linked records

What would you use to implement a Linked List data type? (object, function, class, variable…?)

- I believe we’d use a class to create a constructor for adding items to the linked list.

### *Class 05 Reading*

#### Game of Greed

[Random Module Reading](https://www.pythonforbeginners.com/random/how-to-use-the-random-module-in-python)

- When to use the Random Module: 
    - We want the computer to pick a random number in a given range Pick a random element from a list, pick a random card from a deck, flip a coin etc. 
    - When making your password database more secure or powering a random page feature of your website.

- _Randint_: Randint accepts two parameters: a lowest and a highest number.
RANDINT - ex. will return 1-5
import random
print random.randint(0, 5)

- _Random_:
RANDOM - ex. will return 0-100
import random
random.random() * 100

- _Choice_: Generate a random value from the sequence sequence.
CHOICE: Used for choosing a random element from a list.
random.choice( ['red', 'black', 'green'] ).

- _Shuffle_: The shuffle function, shuffles the elements in list in place, so they are in a random order.
SHUFFLE - ex will return something like [[9], [2], [7], [0], [4], [5], [3], [1], [8], [6]]
from random import shuffle
x = [[i] for i in range(10)]
shuffle(x)

- _Randrange_: Generate a randomly selected element from range(start, stop, step)
import random
for i in range(3):
    print random.randrange(0, 101, 5)

[Risk Management](https://www.edureka.co/blog/risk-analysis-in-software-testing/)

- The probability of any unwanted incident is defined as Risk.
- In Software Testing, risk analysis is the process of identifying the risks in applications or software that you built and prioritizing them to test.

- In any software, using risk analysis at the beginning of a project highlights the potential problem areas
- _High_: means the effect of the risk would be very high and non-tolerable. The company might face loss.
- _Medium_: it is tolerable but not desirable. The company may suffer financially but there is a limited risk.
- _Low_: it is tolerable. There lies little or no external exposure or no financial loss.

- _Business Risks_: This risk is the most common risk associated with our topic. It is the risk that may come from your company or your customer, not from your project.
- _Testing Risks_: You should be well acquainted with the platform you are working on, along with the software testing tools being used.
- _Premature Release Risk_: a fair amount of knowledge to analyze the risk associated with releasing unsatisfactory or untested software is required
- _Software Risks_: You should be well versed with the risks associated with the software development process.

- _Effect_ – To assess risk by Effect. In case you identify a condition, event or action and try to determine its impact.
- _Cause_ – To assess risk by Cause is opposite of by Effect. Initialize scanning the problem and reach to the point that could be the most probable reason behind that.
- _Likelihood_ – To assess risk by Likelihood is to say that there is a probability that a requirement won’t be satisfied.


### *Class 07 Reading*

#### Game of Greed 2 

- *Python Scope* -  https://realpython.com/python-scope-legb-rule/

- Using Python scope will help you avoid or minimize bugs related to name collision as well as bad use of global names across your programs.

* Assignments	x = value
* Import operations	import module or from module import name
* Function definitions	def my_func(): ...
* Argument definitions in the context of functions	def my_func(arg1, arg2,... argN): ...
* Class definitions	class MyClass: ...


- Python resolves names using the so-called LEGB rule, which is named after the Python scope for names.
- The letters in LEGB stand for **Local, Enclosing, Global, and Built-in.**


- Local (or function) scope is the code block or body of any Python function or lambda expression. This Python scope contains the names that you define inside the function. These names will only be visible from the code of the function. It’s created at function call, not at function definition, so you’ll have as many different local scopes as function calls. This is true even if you call the same function multiple times, or recursively. Each call will result in a new local scope being created.

- Enclosing (or nonlocal) scope is a special scope that only exists for nested functions. If the local scope is an inner or nested function, then the enclosing scope is the scope of the outer or enclosing function. This scope contains the names that you define in the enclosing function. The names in the enclosing scope are visible from the code of the inner and enclosing functions.

- Global (or module) scope is the top-most scope in a Python program, script, or module. This Python scope contains all of the names that you define at the top level of a program or a module. Names in this Python scope are visible from everywhere in your code.

- Built-in scope is a special Python scope that’s created or loaded whenever you run a script or open an interactive session. This scope contains names such as keywords, functions, exceptions, and other attributes that are built into Python. Names in this Python scope are also available from everywhere in your code. It’s automatically loaded by Python when you run a program or script.


1. Global: With this statement, you can define a list of names that are going to be treated as global names. The statement consists of the global keyword followed by one or more names separated by commas. You can also use multiple global statements with a name (or a list of names). All the names that you list in a global statement will be mapped to the global or module scope in which you define them.

>>> counter = 0  # A global name
>>> def update_counter():
...     counter = counter + 1  # Fail trying to update counter

</br></br>
>>> counter = 0  # A global name
>>> def update_counter():
...     global counter  # Declare counter as global
...     counter = counter + 1  # Successfully update the counter

- With the statement global counter, you’re telling Python to look in the global scope for the name counter. This way, the expression counter = counter + 1 doesn’t create a new name in the function scope, but updates it in the global scope.

2. Nonlocal: nonlocal names can be accessed from inner functions, but not assigned or updated. If you want to modify them, then you need to use a nonlocal statement. With a nonlocal statement, you can define a list of names that are going to be treated as nonlocal.

>>> def func():
...     var = 100  # A nonlocal variable
...     def nested():
...         nonlocal var  # Declare var as nonlocal
...         var += 100

- You can’t use a nonlocal statement in either the global scope or in a local scope.
- You can’t use nonlocal to create lazy nonlocal names. Names must already exist in the enclosing Python scope if you want to use them as nonlocal names

- **A closure is an inner or nested function that carries information about its enclosing scope, even though this scope has completed its execution.**
>>> def power_factory(exp):
...     def power(base):
...         return base ** exp
...     return power
...
>>> square = power_factory(2)
>>> square(10)
100
>>> cube = power_factory(3)
>>> cube(10)
1000
>>> cube(5)
125
>>> square(15)
225

- In the above example, the inner function power() is first assigned to square. In this case, the function remembers that exp equals 2. In the second example, you call power_factory() using 3 as an argument. This way, cube holds a function object, which remembers that exp is 3. Notice that you can freely reuse square and cube because they don’t forget their respective state information.
</br></br>
</br></br>

---

### *Class 08 Reading*

- #### List Comprehensions 
(https://www.pythonforbeginners.com/basics/list-comprehensions-in-python)

- List comprehensions provide a concise way to create lists.


- It consists of brackets containing an expression followed by a for clause, then zero or more for or if clauses. 
- The expressions can be anything, meaning you can put in all kinds of objects in lists.

ORIGINAL
`new_list = []`
`for i in old_list:`
    `if filter(i):`
        `new_list.append(expressions(i))`

NEW
`new_list = [expression(i) for i in old_list if filter(i)]`

##### Syntax:
`for item in list:`
    `if conditional:`
        `expression`

    I
    I
    V
`[ expression for item in list if conditional ]`

*new_list*
The new list (result).

*expression(i)*
Expression is based on the variable used for each element in the old list.

*for i in old_list*
The word for followed by the variable name to use, followed by the word in the
old list.

*if filter(i)*
Apply a filter with an If-statement.


`new_range = [i * i for i in range(5) if i % 2 == 0]`

Which corresponds to:

`*result* = [*transform* *iteration* *filter* ]`

The * operator is used to repeat. The filter part answers the question if the
item should be transformed.

<br>
The output should be: [‘t’, ‘i’, ‘a’, ‘l’, ‘o’, ‘w’]

- `listOfWords = ["this","is","a","list","of","words"]`
- `items = [ word[0] for word in listOfWords ]`
- `print items`
</br></br>
</br></br>

---

### *Class 09 Reading*

- #### Dunder Methods
(https://www.pythonforbeginners.com/basics/list-comprehensions-in-python)

- In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example __init__ or __str__.

- Treat Python’s data model as a powerful API you can interface with by implementing one or more dunder methods.

- **Object Initialization: __init__**
Right upon starting my class I already need a special method. To construct account objects from the Account class I need a constructor which in Python is the __init__ dunder

- **Object Representation: __str__, __repr__**
It’s common practice in Python to provide a string representation of your object for the consumer of your class (a bit like API documentation.) There are two ways to do this using dunder methods:

1. __repr__: The “official” string representation of an object. This is how you would make an object of the class. The goal of __repr__ is to be unambiguous.

2. __str__: The “informal” or nicely printable string representation of an object. This is for the enduser.

- If you don’t want to hardcode "Account" as the name for the class you can also use self.__class__.__name__ to access it programmatically.


- **Iteration: __len__, __getitem__, __reversed__**
In order to iterate over our account object I need to add some transactions. So first, I’ll define a simple method to add transactions. I’ll keep it simple because this is just setup code to explain dunder methods, and not a production-ready accounting system

- **Operator Overloading for Comparing Accounts: __eq__, __lt__**
We all write dozens of statements daily to compare Python objects:

- **Operator Overloading for Merging Accounts: __add__**
In Python, everything is an object. We are completely fine adding two integers or two strings with the + (plus) operator, it behaves in expected ways

- **Callable Python Objects: __call__**
You can make an object callable like a regular function by adding the __call__ dunder method. For our account class we could print a nice report of all the transactions that make up its balance

- **Context Manager Support and the With Statement: __enter__, __exit__**
A context manager is a simple “protocol” (or interface) that your object needs to follow so it can be used with the with statement. Basically all you need to do is add __enter__ and __exit__ methods to an object if you want it to function as a context manager.
</br></br>
</br></br>

---

### *Class 10 Reading*

#### Stacks & Queue Quiz  

1. Come up with an application scenario where you would want to use a stack.

- Reversing a word

2. Come up with an application scenario where you would want to use a queue.

- A ticket buying app or pre-sale vendor thath puts users into an order

3. Why are pop, push, enqueue and dequeue always O(1)?

- It takes the same amount of time no matter how many Nodes (n) you have in the stack.

4. Why do stacks and queues not have traversal or searching operations?

- These data structures do have search functionality, Deapth-First & Breadth-First Searches. ([Source](https://www.cs.cmu.edu/~adamchik/15-121/lectures/Stacks%20and%20Queues/Stacks%20and%20Queues.html))

</br></br>
</br></br>

---

### *Class 11 Reading*
#### JupyterLab 
https://jupyterlab.readthedocs.io/en/stable/getting_started/overview.html

- JupyterLab is a next-generation web-based user interface for Project Jupyter
- Work with documents and activities such as Jupyter notebooks, text editors, terminals, and custom components in a flexible, integrated, and extensible manner

* Code Consoles provide transient scratchpads for running code interactively, with full support for rich output. A code console can be linked to a notebook kernel as a computation log from the notebook, for example.

* Kernel-backed documents enable code in any text file (Markdown, Python, R, LaTeX, etc.) to be run interactively in any Jupyter kernel.

* Notebook cell outputs can be mirrored into their own tab, side by side with the notebook, enabling simple dashboards with interactive controls backed by a kernel.

* Multiple views of documents with different editors or viewers enable live editing of documents reflected in other viewers. For example, it is easy to have live preview of Markdown, Delimiter-separated Values, or Vega/Vega-Lite documents.

- JupyterLab offers customizable keyboard shortcuts and the ability to use key maps from vim, emacs, and Sublime Text in the text editor.




















</br></br>
</br></br>
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

