
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

#### Numpy
https://www.dataquest.io/blog/numpy-tutorial-python/

- NumPy is a commonly used Python data analysis package
- Almost every data analysis or machine learning package for Python leverages NumPy in some way.

- In a NumPy array, the number of dimensions is called the rank, and each dimension is called an axis. So the rows are the first axis, and the columns are the second axis.

- We can check the number of rows and columns in our data using the shape property of NumPy arrays. Ex: wines.shape = (1599, 12)

- You can create an array where every element is zero. The below code will create an array with 3 rows and 4 columns, where every element is 0, using numpy.zeros: 
```import numpy as np```
```empty_array = np.zeros((3,4)) empty_array```

- You can also create an array where each element is a random number using numpy.random.rand (Ex: np.random.rand(3,4))

</br></br>
</br></br>

### *Class 12 Reading*

#### Pandas in 10 
https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html

- Pandas is a software library written for the Python programming language for data manipulation and analysis
- Pandas offers data structures and operations for manipulating numerical tables and time series

###### Object creation
###### Viewing data
###### Selection
- Getting
- Selection by label
- Selection by position
- Boolean indexing
- Setting
###### Missing data
###### Operations
- Stats
- Apply
- Histogramming
- String Methods
###### Merge
- Concat
- Join
###### Grouping
###### Reshaping
- Stack
- Pivot tables
###### Time series
###### Categoricals
###### Plotting
###### Getting data in/out
- CSV
- HDF5
- Excel
###### Gotchas


</br></br>
</br></br>

### *Class 13 Reading*

#### Linear Regression
- https://bigdata-madesimple.com/how-to-run-linear-regression-in-python-scikit-learn/

- Scikit-learn is a powerful Python module for machine learning. 
** Can do regression, classification, clustering, model selection and dimensionality reduction
- sklearn.linear_model module: Contains “methods intended for regression in which the target value is expected to be a linear combination of the input variables”.

- For Later [UCI Machine Learning Repository](http://archive.ics.uci.edu/ml/)

- First step: Import the required Python libraries into Ipython Notebook.
`%matplotlib inline`
`import numpy as np`
`import pandas as pd`
`import scipy.stats as stats`
`import matplotlib as plt`
`import sklearn`

- Import Boston data set into Ipython notebook and store it in a variable called boston.
`from sklearn.datasets import load_boston`
`boston = load_boston`

- boston is a dictionary - to explore keys:
`boston.keys()`

- Print the feature names of boston data set.
`print boston.feature_names`

### The goal of this exercise is to predict the housing prices in boston region using the features given.

- Print the description of this data set to know more about it.
`print boston.DESCR`

- Convert boston.data into a pandas data frame.
`bos = pd.DataFrame(boston.data)`
`bos.head()`

- Replace tthe column names with the feature names.
`bos.columns = boston.feature_names`
`bos.head()`

- boston.target contains the housing prices.
`boston.target[:5]`

- Add these target prices to the bos data frame.
``bos['PRICE'] = boston.target

- Y = boston housing price(also called “target” data in Python)
- X = all the other features (or independent variables)

- Import linear regression from sci-kit learn module. Then I am going to drop the price column as I want only the parameters as my X values. I am going to store linear regression object in a variable called lm.
`from sklearn.linear_model import LinearRegressiom`
`X=bos.drop('PRICE', axis = 1)`

`lm = LinearRegression()`
`lm`

- To look inside the linear regression object, you can do so by typing LinearRegression. and the press `<tab>` key. This will give a list 
- You can also explore the functions inside lm object by pressing `lm.<tab>`


*Important functions to keep in mind while fitting a linear regression model are:*
- lm.fit() -> fits a linear model
- lm.predict() -> Predict Y using the linear model with estimated coefficients
- lm.score() -> Returns the coefficient of determination (R^2). A measure of how well observed outcomes are replicated by the model, as the proportion of total variation of outcomes explained by the model.
- coef_ gives the coefficients and .intercept_ gives the estimated intercepts

</br></br>
</br></br>

### *Class 14 Reading*

#### Matplotlib tutorial
https://github.com/rougier/matplotlib-tutorial

- matplotlib is the single most used Python package for 2D-graphics
- an enhanced interactive Python shell containing named inputs and outputs, access to shell commands, improved debugging and much more.

- **pyplot** provides a convenient interface to the matplotlib object-oriented plotting library.
- The majority of plotting commands in pyplot have Matlab(TM) analogs with similar argument

**Simple Plot Example**

- The first step is to get the data for the sine and cosine functions:
`import numpy as np`
`X = np.linspace(-np.pi, np.pi, 256, endpoint=True)`
`C, S = np.cos(X), np.sin(X)`

- X is now a NumPy array with 256 values ranging from -π to +π (included). C is the cosine (256 values) and S is the sine (256 values).

- To run the example, you can download each of the examples and run it using:

`$ python exercice_1.py`

- We want to have the cosine in blue and the sine in red and a slightly thicker line for both of them. We'll also slightly alter the figure size to make it more horizontal.
`...`
`plt.figure(figsize=(10,6), dpi=80)`
`plt.plot(X, C, color="blue", linewidth=2.5, linestyle="-")`
`plt.plot(X, S, color="red",  linewidth=2.5, linestyle="-")`
`...`

- Current limits of the figure are a bit too tight and we want to make some space in order to clearly see all data points.

`...`
`plt.xlim(X.min()*1.1, X.max()*1.1)`
`plt.ylim(C.min()*1.1, C.max()*1.1)`
`...`

- Current ticks are not ideal because they do not show the interesting values (+/-π,+/-π/2) for sine and cosine. We'll change them such that they show only these values.
`...`
`plt.xticks( [-np.pi, -np.pi/2, 0, np.pi/2, np.pi])`
`plt.yticks([-1, 0, +1])`
`...`

- When we set tick values, we can also provide a corresponding label in the second argument list. Note that we'll use latex to allow for nice rendering of the label.
`...`
`plt.xticks([-np.pi, -np.pi/2, 0, np.pi/2, np.pi],`
`       [r'$-\pi$', r'$-\pi/2$', r'$0$', r'$+\pi/2$', r'$+\pi$'])`

`plt.yticks([-1, 0, +1],`
`       [r'$-1$', r'$0$', r'$+1$'])`
`...`

- Spines are the lines connecting the axis tick marks and noting the boundaries of the data area. We'll change that since we want to have them in the middle.
- Since there are four of them (top/bottom/left/right), we'll discard the top and right by setting their color to none and we'll move the bottom and left ones to coordinate 0 in data space coordinates.

`...`
`ax = plt.gca()`
`ax.spines['right'].set_color('none')`
`ax.spines['top'].set_color('none')`
`ax.xaxis.set_ticks_position('bottom')`
`ax.spines['bottom'].set_position(('data',0))`
`ax.yaxis.set_ticks_position('left')`
`ax.spines['left'].set_position(('data',0))`
`...`

- add a legend in the upper left corner

`...`
`plt.plot(X, C, color="blue", linewidth=2.5, linestyle="-", label="cosine")`
`plt.plot(X, S, color="red",  linewidth=2.5, linestyle="-", label="sine")`

`plt.legend(loc='upper left', frameon=False)`
`...`

- To annotate some interesting points use the annotate command
- We choose the 2π/3 value and we want to annotate both the sine and the cosine.
`...`
`t = 2*np.pi/3`
`plt.plot([t,t],[0,np.cos(t)], color ='blue', linewidth=1.5, linestyle="--")`
`plt.scatter([t,],[np.cos(t),], 50, color ='blue')`

`plt.annotate(r'$\sin(\frac{2\pi}{3})=\frac{\sqrt{3}}{2}$',`
`             xy=(t, np.sin(t)), xycoords='data',`
`             xytext=(+10, +30), textcoords='offset points', fontsize=16,`
`             arrowprops=dict(arrowstyle="->", connectionstyle="arc3,rad=.2"))`

`plt.plot([t,t],[0,np.sin(t)], color ='red', linewidth=1.5, linestyle="--")`
`plt.scatter([t,],[np.sin(t),], 50, color ='red')`

`plt.annotate(r'$\cos(\frac{2\pi}{3})=-\frac{1}{2}$',`
`             xy=(t, np.cos(t)), xycoords='data',`
`             xytext=(-90, -50), textcoords='offset points', fontsize=16,`
`             arrowprops=dict(arrowstyle="->", connectionstyle="arc3,rad=.2"))`
`...`

- The tick labels are now hardly visible because of the blue and red lines. We can make them bigger and we can also adjust their properties such that they'll be rendered on a semi-transparent white background. This will allow us to see both the data and the labels.
`...`
`for label in ax.get_xticklabels() + ax.get_yticklabels():`
`    label.set_fontsize(16)`
`    label.set_bbox(dict(facecolor='white', edgecolor='None', alpha=0.65 ))`
`...`

- We can have more control over the display using figure, subplot, and axes explicitly
- When we call plot, matplotlib calls gca() to get the current axes and gca in turn calls gcf() to get the current figure. If there is none it calls figure() to make one, strictly speaking, to make a subplot(111). Let's look at the details.

- A figure is the windows in the GUI that has "Figure #" as title. Figures are numbered starting from 1 as opposed to the normal Python way starting from 0. This is clearly MATLAB-style. There are several parameters that determine what the figure looks like:

Argument    Default	            Description
num	        1	                number of figure
figsize	    figure.figsize      figure size in in inches (width, height)
dpi	        figure.dpi	        resolution in dots per inch
facecolor	figure.facecolor    color of the drawing background
edgecolor	figure.edgecolor    color of edge around the drawing background
frameon	    True	            draw figure frame or not


- You can close a figure programmatically by calling close.
- **Depending on the argument it closes (1) the current figure (no argument), (2) a specific figure (figure number or figure instance as argument), or (3) all figures (all as argument).**

</br></br>
</br></br>

### *Class 15 Reading*

1. What is a leaf node? Why is it important to be able to find leaf nodes?
>> The leaf node is the last node in a tree with no attached edges - when traversing a tree, once it hits a leaf and both left and right return null, it will end the execution of the method.
2. Describe the differences between pre-order, in-order, and post-order traversal. Why are they called pre, in, and post order?
>> PRE: means that the root has to be looked at first/top to bottom
>> POST: this means that the root is looked at last/bottom to top
>> IN: reads the tree from left to right
3. What is the height of a fully balanced (each non-leaf node has two children) tree? What is this used for?
>> log(n) , used for searching. If a tree is balanced, it is easier to say for sure how the big O is going to look. If unbalanced, worse case, one side could be O(1) where the other is o(n)
4. How are stacks and queues used in relation to trees?
>> They are used to hold the place of the traversal as it goes through the tree - as if reaches a leaf, values are popped or dequeued onto the return

</br></br>
</br></br>

### *Class 16 Reading*

#### Web Scrape with Python in 4 Minutes
- https://towardsdatascience.com/how-to-web-scrape-with-python-in-4-minutes-bc49186a8460

- Web scraping is a technique to automatically access and extract large amounts of information from a website
- Turnstile data: 

- It would be torturous to manually right click on a hundred links and save to your desktop. Luckily, there’s web-scraping!

- Inspect the Website: Figure out where we can locate the links to the files we want to download inside the multiple levels of HTML tags.

1. On the website, right click and click on “Inspect”. This allows you to see the raw code behind the site.

- Notice that on the top left of the console, there is an arrow symbol. Click on this arrow and then click on an area of the site itself, the code for that particular item will be highlighted in the console

2. Import the following libraries.
import requests
import urllib.request
import time
from bs4 import BeautifulSoup

3. Set the url to the website and access the site with our requests library.
url = 'http://web.mta.info/developers/turnstile.html'
response = requests.get(url)

- If the access was successful, you should see the following output: <Response [200]>

4. Parse the html with BeautifulSoup so that we can work with a nicer, nested BeautifulSoup data structure.
soup = BeautifulSoup(response.text, “html.parser”)
^^This code gives us every line of code that has an `<a>` tag.

5. To extract the actual link that we want. Let’s test out the first link.
`one_a_tag = soup.findAll(‘a’)[38]`
`link = one_a_tag[‘href’]`

6. We can use our urllib.request library to download this file path to our computer. We provide request.urlretrieve with two parameters: file url and the filename. For my files, I named them “turnstile_180922.txt”, “turnstile_180901”, etc.

`download_url = 'http://web.mta.info/developers/'+ link`
`urllib.request.urlretrieve(download_url,'./'+link[link.find('/turnstile_')+1:])`

7. *Include this line of code so that we can pause our code for a second so that we are not spamming the website with requests. This helps us avoid getting flagged as a spammer.*
`time.sleep(1)`

8. Download the entire set of data files with a for loop. The code below contains the entire set of code for web scraping the NY MTA turnstile data.
`# Import libraries`
`import requests`
`import urllib.request`
`import time`
`from bs4 import BeautifulSoup`

`# Set the URL you want to webscrape from`
`url = 'http://web.mta.info/developers/turnstile.html'`

`# Connect to the URL`
`response = requests.get(url)`

`# Parse HTML and save to BeautifulSoup object¶`
`soup = BeautifulSoup(response.text, "html.parser")`

`# To download the whole data set, let's do a for loop through all a tags`
`line_count = 1 #variable to track what line you are on`
`for one_a_tag in soup.findAll('a'):  #'a' tags are for links`
    `if line_count >= 36: #code for text files starts at line 36`
        `link = one_a_tag['href']`
        `download_url = 'http://web.mta.info/developers/'+ link`
        `urllib.request.urlretrieve(download_url,'./'+link[link.find('/turnstile_')+1:])`
        `time.sleep(1) #pause the code for a sec`
    `#add 1 for next line`
    `line_count +=1`



- #### Wikipedia Web Scraping Info
- https://en.wikipedia.org/wiki/Web_scraping

- Web scraping, web harvesting, or web data extraction is data scraping used for extracting data from websites
- It is a form of copying, in which specific data is gathered and copied from the web, typically into a central local database or spreadsheet, for later retrieval or analysis.

- Web scraping a web page involves fetching it and extracting from it.
- *Fetching*: Downloading of a page (which a browser does when a user views a page)





</br></br>
</br></br>

### *Class 17 Reading*

### Encryption, decryption, and cracking
- https://www.khanacademy.org/computing/computers-and-internet/xcae6f4a7ff015e7d:online-data-security/xcae6f4a7ff015e7d:data-encryption-techniques/a/encryption-decryption-and-code-cracking

- Caesar Cipher: One of the earliest encryption techniques. 
- Messages would be shifted in 3's (According to historical records, Caesar always used a shift of 3. As long as his message recipient knew the shift amount, it was trivial for them to decode the message)


- There are three main techniques : frequency analysis, known plaintext, and brute force
- Human languages tend to use some letters more than others. For example, "E" is the most popular letter in the English language.

- Another term for the original unencrypted message is plaintext.

- Encryption: scrambling the data according to a secret key (Alphabet shift).
- Decryption: recovering the original data from scrambled data by using the secret key.
- Code cracking: uncovering the original data without knowing the secret, by using a variety of clever techniques.

</br></br>
</br></br>

### *Class 18 Reading*

#### Python Regular Expression Tutorial
- https://www.datacamp.com/community/tutorials/python-regular-expression-tutorial

- Regex: A sequence of characters used to check whether a pattern exists in a given text (string) or not
- They help in manipulating textual data, which is often a prerequisite for data science projects involving text mining
- In Python, regular expressions are supported by the `re` module

- EXAMPLE: compile(), search(), findall(), sub() for search and replace, split()

- Ordinary characters are the simplest regular expressions. They match themselves exactly and do not have a special meaning in their regular expression syntax.

- EXAMPLE: 'A', 'a', 'X', '5'.

- The match() function returns a match object if the text matches the pattern. Otherwise, it returns None

- Starting a str with `r` (EX. r"Cookie"): This is called a raw string literal. It changes how the string literal is interpreted. Such literals are stored as they appear.

- EXAMPLE:  \ is just a backslash when prefixed with an r rather than being interpreted as an escape sequence

- Special characters are characters that do not match themselves as seen but have a special meaning when used in a regular expression.
- They can be thought of as reserved metacharacters that denote something else and not what they look like

- `.` - A period. Matches any single character except the newline character.
- `^` - A caret. Matches the start of the string.
- `$` - Matches the end of string.
- `[abc]` - Matches a or b or c.
- `[a-zA-Z0-9]` - Matches any letter from (a to z) or (A to Z) or (0 to 9)
- `\` - Backslash:
    - If the character following the backslash is a recognized escape character, then the special meaning of the term is taken (Scenario 1)
    - Else if the character following the \ is not a recognized escape character, then the \ is treated like any other character and passed through (Scenario 2).
    - \ can be used in front of all the metacharacters to remove their special meaning (Scenario 3)
- `\w` - Lowercase 'w'. Matches any single letter, digit, or underscore.
- `\W`- Uppercase 'W'. Matches any character not part of \w (lowercase w).

- `\s` - Lowercase 's'. Matches a single whitespace character like: space, newline, tab, return.
- `\S` - Uppercase 'S'. Matches any character not part of \s (lowercase s).

- `\d` - Lowercase d. Matches decimal digit 0-9. The + symbol used after the \d is used for repetition
- `\D` - Uppercase d. Matches any character that is not a decimal digit.

- `\t` - Lowercase t. Matches tab.
- `\n` - Lowercase n. Matches newline.
- `\r` - Lowercase r. Matches return.
- `\A` - Uppercase a. Matches only at the start of the string. Works across multiple lines as well.
- `\Z` - Uppercase z. Matches only at the end of the string.

- `\b` - Lowercase b. Matches only the beginning or end of the word


- `+` Checks if the preceding character appears one or more times.
- `*` Checks if the preceding character appears zero or more times.
- `?` Checks if the preceding character appears exactly zero or one time. Specifies a non-greedy version of +, *
- `{ }` Checks for an explicit number of times.
- `( )` Creates a group when performing matches.
- `< >` Creates a named group when performing matches.

- IGNORECASE (I) - Allows case-insensitive matches.
- DOTALL (S) - Allows . to match any character, including newline.
- MULTILINE (M) - Allows start of string (^) and end of string ($) anchor to match newlines as well.
- VERBOSE (X) - Allows you to write whitespace and comments within a regular expression to make it more readable.
</br></br>
</br></br>


### *Class 26 Reading*

#### Getting started with Django
- https://www.djangoproject.com/start/

- Deﬁne your data models entirely in Python. You get a rich, dynamic database-access API for free — but you can *still write SQL if needed.*
- To design URLs for an application, you create a Python module called a URLconf. 
- Like a table of contents for your app, it contains a simple mapping between URL patterns and your views.
- Django’s template language is designed to strike a balance between power and ease. It’s designed to feel comfortable and easy-to-learn to those used to working with HTML, like designers and front-end developers. But it is also flexible and highly extensible, allowing developers to augment the template language as needed.

`<html>`
  `<head>`
    `<title>Band Listing</title>`
  `</head>`
  `<body>`
   `<h1>All Bands</h1>`
    `<ul>`
    `{% for band in bands %}`
      `<li>`
        `<h2><a href="{{ band.get_absolute_url }}">{{ band.name }}</a></h2>`
        `{% if band.can_rock %}<p>This band can rock!</p>{% endif %}`
      `</li>`
    `{% endfor %}`
    `</ul>`
  `</body>`
`</html>`

- !!!Django provides a powerful form library that handles rendering forms as HTML, validating user-submitted data, and converting that data to native Python types. Django also provides a way to generate forms from your existing models and use those forms to create and update data.!!!

`from django import forms`

- Django comes with a full-featured and secure authentication system. 
- It handles user accounts, groups, permissions and cookie-based user sessions. This lets you easily build sites that allow users to create accounts and safely log in/out.
- One of the most powerful parts of Django is its automatic admin interface. It reads metadata in your models to provide a powerful and production-ready interface that content producers can immediately use to start managing content on your site. It’s easy to set up and provides many hooks for customization.
- Django offers full support for translating text into different languages, plus locale-specific formatting of dates, times, numbers, and time zones. It lets developers and template authors specify which parts of their apps should be translated or formatted for local languages and cultures, and it uses these hooks to localize Web applications for particular users according to their preferences.

### *Class 27 Reading*

#### Django Models
- https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Models

- Python objects are referred to as models
- Models define the structure of stored data, including the field types and possibly also their maximum size, default values, selection list options, help text for documentation, label text for forms, etc
- *Write your model structure and other code, and Django handles all the dirty work of communicating with the database for you.*

##### Creating your model (Ex. Library) 

- Models are usually defined in an application's models.py file.
- They are implemented as subclasses of django.db.models.Model, and can include fields, methods and metadata.

`from django.db import models`

`class MyModelName(models.Model):`
    `"""A typical class defining a model, derived from the Model class."""`

    `# Fields`
    `my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')`

    `# Metadata`
    `class Meta:`
        `ordering = ['-my_field_name']`

    `# Methods`
    `def get_absolute_url(self):`
        `"""Returns the url to access a particular instance of MyModelName."""`
        `return reverse('model-detail-view', args=[str(self.id)])`

    `def __str__(self):`
        `"""String for representing the MyModelName object (in Admin site etc.)."""`
        `return self.my_field_name`

- When designing your models it makes sense to have separate models for every "object" (a group of related information). In this case, the obvious objects are books, book instances, and authors.

- Use models to represent selection-list options (e.g. like a drop down list of choices), rather than hard coding the choices into the website itself — this is recommended when all the options aren't known up front or may change
- *Think about the relationships* - Django allows you to define relationships that are one to one (OneToOneField), one to many (ForeignKey) and many to many (ManyToManyField).
- A model can have an arbitrary number of fields, of any type — each one represents a column of data that we want to store in one of our database tables. Each database record (row) will consist of one of each field value.
- The field name is used to refer to it in queries and templates.



- Replacing any underscores in the field name with a space (for example my_field_name would have a default label of my field name)
- Note that when the label is used as a form label through Django frame, the first letter of the label is capitalised (for example my_field_name would be My field name).

- **In every model you should define the standard Python class method __str__() to return a human-readable string for each object.**
`def __str__(self):`
    `return self.field_name`

- `get_absolute_url()`, will return a URL for displaying individual model records on the website
`def get_absolute_url(self):`
    `"""Returns the url to access a particular instance of the model."""`
    `return reverse('model-detail-view', args=[str(self.id)])`

- Use ypur models to create, update, or delete records, and to run queries to get all records or particular subsets of records

#### Django admin site
- https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Admin_site

- The Django admin application can use your models to automatically build a site area that you can use to create, view, update, and delete records.
- The admin application can also be useful for managing data in production, depending on the type of website
- After registering some models, you can create a new "superuser"


- Register the models by copying the following text into the bottom of the file. This code imports the models and then calls admin.site.register to register each of them.
`from .models import Author, Genre, Book, BookInstance`

`admin.site.register(Book)`
`admin.site.register(Author)`
`admin.site.register(Genre)`
`admin.site.register(BookInstance)`

- In order to log into the admin site, we need a user account with Staff status enabled

- On order to view and create records we also need this user to have permissions to manage all our objects.  You can create a "superuser" account that has full access to the site and all needed permissions using manage.py.
- Call the following command, in the same directory as manage.py, to create the superuser. You will be prompted to enter a username, email address, and strong password.
`python3 manage.py createsuperuser`

`python3 manage.py runserver`

- ***The admin site displays all our models, grouped by installed application. You can click on a model name to go to a screen that lists all its associated records, and you can further click on those records to edit them. You can also directly click the Add link next to each model to start creating a record of that type***

### *Class 28 Reading*

#### Django: Working with forms

- https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Forms

- An HTML Form is a group of one or more fields/widgets on a web page, which can be used to collect information from users for submission to a server.
-  Developers need to write HTML for the form, validate and properly sanitize entered data on the server (and possibly also in the browser), repost the form with error messages to inform users of any invalid fields, handle the data when it has successfully been submitted, and finally respond to the user in some way to indicate success
- *Django Forms take a lot of the work out of all these steps, by providing a framework that lets you define forms and their fields programmatically, and then use these objects to both generate the form HTML code and handle much of the validation and user interaction.*

Normal HTML:
`<form action="/team_name_url/" method="post">`
    `<label for="team_name">Enter name: </label>`
    `<input id="team_name" type="text" name="name_field" value="Default name for team.">`
    `<input type="submit" value="OK">`
`</form>`

- The field's type attribute defines what sort of widget will be displayed. The name and id of the field are used to identify the field in JavaScript/CSS/HTML, while value defines the initial value for the field when it is first displayed. The matching team label is specified using the label tag (see "Enter name" above), with a for field containing the id value of the associated input.
- `action`: The resource/URL where data is to be sent for processing when the form is submitted. If this is not set (or set to an empty string), then the form will be submitted back to the current page URL.
- `method`: The HTTP method used to send the data: post or get.
    - The POST method should always be used if the data is going to result in a change to the server's database because this can be made more resistant to cross-site forgery request attacks.
    - The GET method should only be used for forms that don't change user data (e.g. a search form). It is recommended for when you want to be able to bookmark or share the URL.
    <br>
    <br>
- Django's form handling uses all of the same techniques that we learned about in previous tutorials (for displaying information about our models): the view gets a request, performs any actions required including reading data from the models, then generates and returns an HTML page (from a template, into which we pass a context containing the data to be displayed)
- What makes things more complicated is that the server also needs to be able to process data provided by the user, and redisplay the page if there are any errors.
 !(Django Form Flow)[https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Forms/form_handling_-_standard.png]

- **Display the default form the first time it is requested by the user.**
    - The form may contain blank fields (e.g. if you're creating a new record), or it may be pre-populated with initial values (e.g. if you are changing a record, or have useful default initial values).
    - The form is referred to as unbound at this point, because it isn't associated with any user-entered data (though it may have initial values).
- **Receive data from a submit request and bind it to the form.**
    - Binding data to the form means that the user-entered data and any errors are available when we need to redisplay the form.
- **Clean and validate the data.**
    - Cleaning the data performs sanitization of the input (e.g. removing invalid characters that might be used to send malicious content to the server) and converts them into consistent Python types.
    - Validation checks that the values are appropriate for the field (e.g. are in the right date range, aren't too short or too long, etc.)
- **If any data is invalid, re-display the form, this time with any user populated values and error messages for the problem fields**
- **If all data is valid, perform required actions (e.g. save the data, send an email, return the result of a search, upload a file, etc.)**
- **Once all actions are complete, redirect the user to another page.**
<br>

- The most fundamental is the Form class, which simplifies both generation of form HTML and data cleaning/validation.
- The Form class is the heart of Django's form handling system. It specifies the fields in the form, their layout, display widgets, labels, initial values, valid values, and (once validated) the error messages associated with invalid fields. 
- The class also provides methods for rendering itself in templates using predefined formats (tables, lists, etc.) or for getting the value of any element (enabling fine-grained manual rendering).

`from django import forms`

`class RenewBookForm(forms.Form):`
    `renewal_date = forms.DateField(help_text="Enter a date between now and 4 weeks (default 3).")`

- There are many other types of form fields, which you will largely recognize from their similarity to the equivalent model field classes: BooleanField, CharField, ChoiceField, TypedChoiceField, DateField, DateTimeField, DecimalField, DurationField, EmailField, FileField, FilePathField, FloatField, ImageField, IntegerField, GenericIPAddressField, MultipleChoiceField, TypedMultipleChoiceField, NullBooleanField, RegexField, SlugField, TimeField, URLField, UUIDField, ComboField, MultiValueField, SplitDateTimeField, ModelMultipleChoiceField, ModelChoiceField.
- Django provides numerous places where you can validate your data. The easiest way to validate a single field is to override the method clean_<fieldname>() for the field you want to check.

`import datetime`

`from django import forms`
`from django.core.exceptions import ValidationError`
`from django.utils.translation import ugettext_lazy as _`

`class RenewBookForm(forms.Form):`
    `renewal_date = forms.DateField(help_text="Enter a date between now and 4 weeks (default 3).")`

    `def clean_renewal_date(self):`
        `data = self.cleaned_data['renewal_date']`

        `# Check if a date is not in the past.`
        `if data < datetime.date.today():`
            `raise ValidationError(_('Invalid date - renewal in past'))`

        `# Check if a date is in the allowed range (+4 weeks from today).`
        `if data > datetime.date.today() + datetime.timedelta(weeks=4):`
            `raise ValidationError(_('Invalid date - renewal more than 4 weeks ahead'))`

        `# Remember to always return the cleaned data.`
        `return data`

- The first is that we get our data using self.cleaned_data['renewal_date'] and that we return this data whether or not we change it at the end of the function.
- If a value falls outside our range we raise a ValidationError, specifying the error text that we want to display in the form if an invalid value is entered. The example above also wraps this text in one of Django's translation functions ugettext_lazy() (imported as _()), which is good practice if you want to translate your site later.

- Add a URL configuration for the renew-books page. Copy the following configuration to the bottom of locallibrary/catalog/urls.py.

`urlpatterns += [`
    `path('book/<uuid:pk>/renew/', views.renew_book_librarian,name='renew-book-librarian'),`
`]`

- The URL configuration will redirect URLs with the format /catalog/book/<bookinstance_id>/renew/ to the function named renew_book_librarian() in views.py, and send the BookInstance id as the parameter named pk. The pattern only matches if pk is a correctly formatted uuid.

- If you just need a form to map the fields of a single model then your model will already define most of the information that you need in your form: fields, labels, help text and so on.

- Rather than recreating the model definitions in your form, it is easier to use the **ModelForm** helper class to create the form from your model. This ModelForm can then be used within your views in exactly the same way as an ordinary Form.

`from django.forms import ModelForm`

`from catalog.models import BookInstance`

`class RenewBookModelForm(ModelForm):`
    `class Meta:`
        `model = BookInstance`
        `fields = ['due_back']`

---------------------------------------------------------

`class Meta:`
    `model = BookInstance`
    `fields = ['due_back']`
    `labels = {'due_back': _('New renewal date')}`
    `help_texts = {'due_back': _('Enter a date between now and 4 weeks (default 3).')}`

- Django provides generic form editing views that can do almost all the work to define pages that can create, edit, and delete records associated with a single model instance

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
