+++
date = 2017-09-11
draft = false
tags = ["daco_prac_17"]
title = "DACO - Practical Lecture 1 - Introduction to Python for Scientific Computing"
math = false
summary = """
Where we learn the basics of how set up a Python-based system to develop Machine Learning,
Computer Vision, and Image Processing projects.
"""
+++

**NOTE: This tutorial is under construction**

This year we have decided to move from Matlab to Python for the practical sessions.
Some of you maybe will not have worked with this programming language.
This first lecture is intended to guide you through your first steps in this programming language,
and make you aware of the (super-rich) Python ecosystem for scientific computing.

I really hope that by the end of this course you will be a Python fan, and consider abandoning Matlab once and forever!
This is an overview of what you will be learning today:

1. **Motivation and Goals. What is Python?**

2. **Python Installation. Accompanying Tools**

3. **A Quick Introduction to the Python Programming Language**
    1. Data Types
    2. Python Operators
    3. Flow Control in Python
    4. Python Variables and Functions
    5. Python Objects and Classes
    6. Modules and Packages

4. **Complementary Python Scientific Computing Tools**

5. **Homework :scream:**

6. **Sources and References**

So... let's move on.

## 1.- **Motivation and Goals. What is Python?**

First thing, Python is **free**. Second, it is **simple**.
Third, it is increasingly becoming the tool of choice for data science projects.
Fourth, it's multi-platform, it can run in Windows, Linux, Mac, your mobile phone...
And last, there is a **huge** community of contributors to lots of open-source projects that complement it.
This manifests in the form of a large ecosystem of scientific computing tools that grow along with the number of users.

However, to add all this to your tool-belt, the first step is to familiarize yourself with the Python language itself.
Today we will quickly review the main notions to get started on it.

But first, let us install Python!

## 2. **Python Installation. Accompanying tools**
### 2.1 Anaconda Python Distribution
In this course we will use the Python language programming. 
However, as mentioned above, one of the main strengths of Python is the large amount of available scientific libraries.
This means that, together with the core Python language, we'll be using several Python packages to perform scientific computations. 
But instead of installing all these packages manually one at a time, we will be using a **Python distribution**.
A distribution consists of the core Python package and several hundred modules, and available through a single download and installation. 
In this course, we will use the Anaconda Python distribution. 
Apart of Python itself and several hundred libraries, Anaconda also includes two very useful development environments: **Jupyter** and **Spyder**. 
More on this below.

{{% alert note %}}
The Anaconda Python distribution can be found [here](https://www.continuum.io/downloads). Please install the Python 3.
{{% /alert %}}

Questions for the slide/quizzes:
a) Python has two operating modes. Which are they?
Interactive mode
Standard mode
Both of the above - correct
None of the above

b) Which version of Python will we focus on in this course?
Python 2
Python 3 - correct
Spyder
Jupyter

### 2.2  Executing Python code
Python has two different modes: **interactive** and **standard**.
The interactive mode is meant for experimenting your code one line or one expression at a time.
The standard mode is useful for running programs from start to finish.
You will probably find yourself alternating between both modes.

#### 2.2.1 Python Interactive Mode
For a first example on interactive mode, open a command console, type `python`, and you will start using Python. Experiment a bit.

A more convenient way of building code interactively is through **iPython notebooks - Jupyter**. 
This also allows us to mix text, code, and maths, which is really cool. 
To start an iPython notebook, open a console, type jupyter notebook, and navigate in your browser to localhost/whatever.
Explanations on ipython.


#### 2.2.2 Python Standard Mode
In this case, we write a text file with Python instructions, and run it. ``hello_world.py``.

Again, there is a more convenient way for building code in standard mode, which is using an **IDE** (Integrated Development Environment).
This programming tool will allow you to more easily debug, inspect variables, and quickly modify your code. 
They typically also include an embedded interactive system. An example of an IDE is **Spyder**, already contained in the Anaconda distribution.

Questions for the slide/quizzes:
For the contents of this lecture, starting from Section 3, a notebook version of this lecture is available here. Open it!


## 3. **Introduction to the Python Programming Language**

### 3.1 - Fundamental Python data types
Python contains several typical built-in data types as part of the core language.
The same as in e.g Matlab (and different from e.g. C) you do not need to explicitly declare the type of a variable.
Python determines data type of variables by how they are used.

For instance, to create an integer (`int`) variable you simply type:
```python
# An integer variable a
a = 5
print(type(a))
```
Other basic/common python types are for instance`float`, `string`, or `boolean`, exemplified below:
```python
# A float variable f
f = 5.0
# A boolean
b = True
# A string
c = 'bom dia'
```

### 3.2 - Everything is an object
It is important that you start thinking of the above examples ``a,f,b,c`` as **objects**. 
Each object in Python has three characteristics: object **type**, object **value**, and object **identity**.
Object type tells Python what kind of an object it's dealing with.
A type could be a number, or a string, or a list, or something else.
Object value is the data value is contained by the object.
This could be a specific number, for example.
Finally, you can think of object identity as an identity number for the object.
Each distinct object in the computer's memory will have its own identity number.

Questions for the slide/quizzes:
Consider the following line of code:
x = 4
In this assignment, what does the number 4 represent?
The object type.
The object value. correct
The object identity.

Most Python objects have either data or functions or both associated with them.
These are known as attributes.
The name of the attribute follows the name of the object.
And these two are separated by a dot in between them.
The two types of attributes are called either data attributes or methods.
A data attribute is a value that is attached to a specific object.
In contrast, a method is a function that is attached to an object.
And typically a method performs some function
or some operation on that object.
Object type always determines the kind of operations that it supports.
In other words, depending on the type of the object,
different methods may be available to you as a programmer.
Finally, an instance is one occurrence of an object.
For example, you could have two strings.
They may have different values stored in them,
but they nevertheless support the same set of methods.


### 3.3 - Python Modules
Python contains builtin functions, such as ``print`` that can be used by all Python programs.
However, while the Python library consists of all core elements, such as data types and built-in functions,
the bulk of the Python library consists of modules.
In order for you to be able to make use of modules in your own code,
you first need to import those modules using the import statement.

**Example of modules, attributes, methods, in numpy.** 

The numpy example above made available some specific data types and methods for us. 
This is an example of a **Python module**.
In general, Python modules are libraries of code that you import and use through ``import`` statements.
Let's go through a simple example. Import the ``math`` module. 
This module gives you access to the pi constant. Print its value.
This module also gives you access to several mathematical operations. Find out (print) the value of the sine of pi.

{{% alert note %}}
If you only need, e.g., the value of pi from the entire ``math`` module, you can import it selectively:
```python
from math import pi
print(pi)
```
{{% /alert %}}

### 3.4 - Python Basic Operators:
Operators are symbols that allow you to use logic and arithmetic in your computations.
Python has several operators, the most prominent ones being **arithmetic**, **comparison**, and **logical**.
#### 3.4.1 - Arithmetic operators:
They will take two variables and perform simple mathematical operations on them.
They are addition `+`, subtraction `-`, multiplication `*`, division `/`, modulus `%`, floor division `//`, and exponentiation `**`
```python
print(3+2, 3-2, 3*2, 3/2, 3%2, 3//2, 3**2)
```
#### 3.4.2 - Comparison operators:
They observe two variables and return a boolean value.
They are the usual greater than (`>`,`>=`), equal (`=`), different (`!=`), and lower than (`<`,`<=`) mathematical operators.
```python
print(3>2, 3<2, 3==2, 3!=2, 3>=2, 3<=2)
```
#### 3.4.3 - Logical operators:
These operators will interpret their input as boolean values, and return a boolean value depending on the truth value of both inputs.
They are `and`, `or`, `not`.
```python
print(True and True, False or False, not True)
```
#### 3.4.5 - Other operators
There are other operators in Python, such as identity (`is`, `is not`) or membership (`in`, `not in`).
I am 100% sure you will be able to guess what is their effect on variables/containers!
{{% alert note %}}
Note this subtle difference between ``==`` and ``is``: ``==`` tests whether objects have the same value, whereas ``is`` 
tests whether objects have the same identity. Try it with ``a=[1,2]`` and ``b=[1,2]``. 
{{% /alert %}}


### 3.5 - Sequences and Object Containers

#### 3.5.1 - Python Sequences
A sequence is an **ordered** collection of objects. In Python, you can find three types of sequences: Lists, Tuples, and Range Objects.


Let us focus on the first two of them. Lists and tuples can be accessed by indexing and can be sliced in several ways:
```python
# A tuple
t = (0,True)
# A list l
l = [0,True]
```
Note that there is a relevant difference between tuples and lists: tuples are **immutable**, while lists are not.
This means that you won't be able to modify the content stored at `t`. We will explain this in a second.
Note also that both lists and tuples allow you to mix different data types.

#### Note: Mutable and immutable objects
The value of some objects can change in the course of program execution.
Objects whose value can change are said to be mutable objects,
whereas objects whose value is unchangeable after they've been created
are called immutable.

Questions for the slide/quizzes:
What does it mean for an object to be immutable?
Its contents cannot be modified by the programmer.
Its contents cannot be modified by the programmer after the object has been created. correct


Continuing with sequences, in order to access the elements that a tuple/list holds, you use **square brackets, not parenthesis**:
```python
# the first element of the tuple t
t_first = t[0]
```
Also note that, the same as e.g. C (and different from e.g. Matlab), **in Python indexing starts at 0**.
Be careful with this, because it is a common source of confusion in the beginning.

Questions for the slide/quizzes:
Consider the following tuple and index (1,2,3)[0]. What will this return?
0
1
3
This code contains an error.

Sequences can be accessed by indexing, which supports negatives indexes:
```python
t = (0,1,'hola',3,4.0)
l = [0,1,'hola',3,4.0]
print(t[0])
print(t[-1]) # note the behavior of negative indexes
print(t[0:2]) # slicing first two elements, third is excluded
print(l[2:5]) # slicing last three elements
print(l[2:]) # empty spot after : means up to length-of-list index
print(l[:2]) # empty spot before : means from first index
print(l[0:5:2]) # every element, but use a step size of 2
```

Questions for the slide/quizzes:
Consider the following tuple and index (1,2,3)[0:-1]. What will this return?
(1,2) correct
(2)
() 
This code contains an error.
Python includes all values from the beginning of the first index in the slice up to and not including the second value in the slice

Sequences also support a very handy operation called **slicing**, that enables access to multiple objects at the same time:
```python
print(t[0:2]) # slicing first two elements, third is excluded
print(l[2:5]) # slicing last three elements
print(l[2:]) # empty spot after : means up to length-of-list index
print(l[:2]) # empty spot before : means from first index
print(l[0:5:2]) # every element, but use a step size of 2
```

Questions for the slide/quizzes:
Consider the following tuple and index (1,2,3)[1:1]. What will this return?
(0)
(1)
() correct
This code contains an error.
Python includes all values from the beginning of the first index in the slice up to and not including the second value in the slice

Tuples and lists, as every python object, have several methods that you can use with them. 
However, since lists are mutable, they have methods that can modify their content: 
```python
a = [4,3,2,1]
a.append(5)
print(a)
a.sort()
print(a)
```
Note that list methods are **in-place methods**, they modify the original object that called them and return nothing.
For a complete list of these, see [here](http://faculty.salina.k-state.edu/tim/NPstudy_guide/python/containers.html#list-methods).


There are other generic Python functions that work with sequences and provide useful operations:
```python
a = [4,3,2,1]
b = sorted(a)
n = len(b)
s = sum(a)
print(b, n, s)
```


#### 3.5.2 - Object Containers: Dictionaries
Sequences are a particularly simple example of Object Containers. 
More generally, Python offers several more advanced object containers. A really useful one are dictionaries.

Dictionaries are **unordered sequences** that associate key objects to value objects. 
This means that a dictionary consists of **Key:Value** pairs, and the keys must be immutable while the values can be anything.
Note that dictionaries themselves are mutable objects.

A dictionary is built with curly braces as follows:
```python
ages = {"Me": 33, "You": 22, "Him":24}
```
If now I want to know your age, and then increase it, I would type:
```python
print(ages["You"])
ages["You"] += 1
print(ages["You"])
```
You can add new items to your dictionary as follows:
```python
ages["Her"] = 20
print(ages)
```

Dictionary objects have also their own methods. 
For instance, you can use `keys` to find out what are all the keys in the dictionary, or the `values` method
to retrieve are all of the values in the dictionary:
```python
names = ages.keys()
years = ages.values()
```
Questions for the slide/quizzes:
Which of the following data structures may be used as keys in a dict?
Strings
Lists
Tuples

### 3.6 Statements

### 3.7 Flow Control

### 3.7 Python Functions

### Classes and Scope Rules


## 4. **Complementary Python Scientific Computing Tools**
Numpy, Matplotlib.



------------------------------------------------------------------------------



### 3.3 - Flow Control in Python
Typical flow control structures are implemented as usual in Python.
{{% alert note %}}
Be careful with Python code **indentation**:
the space you leave to the left of your piece of code implicitly delimits code blocks.
{{% /alert %}}
We will learn the behavior of flow control statements in Python by example,
to reinforce the idea of how intuitive Python is.
#### `if`-`else` statements
Observe the following code:
```python
if 3>2:
    print('success')
elif 3==2:
    print('failure')
else:
    print('I do not know')
print('do you know?')
```

#### `for` loops
Observe the following code:
```python
for i in [0,1,2,3]:
    print(i)
```
#### `while` loops
Observe the following code:
```python
i=0
while i < 4:
    print(i)
    i = i+1
```
{{% alert note %}}
Do not forget about the semicolon in the end of control statements!
{{% /alert %}}
#### `break` and `continue`
Observe the following code:
```python
for i in [0,1,2,3,4]:
    if i % 3 == 0:
        continue
    print(i)
```
```python
for i in [0,1,2,3,4]:
    if i % 3 == 0:
        break
    print(i)
```
{{% alert note %}}
Can you give a definition of both statements?
{{% /alert %}}

### 3.4 - Python Variables and Functions:
Variables are simply reserved memory locations to store values.
The moment you create a variable you reserve some space in memory.
Depending on the data type of a variable, the interpreter allocates a certain amount of memory..

As we have seen above, in Python, there is no need of declaring variables before using them.
This is because actually what you are doing is not creating a spot in memory and filling it with an object.
Rather, you are creating a pointer (that occupies a first memory spot), and then making that pointer point to an object in a second memory spot.
For this reason, you can for instance reassign a variable to a different type of object without errors:
```python
a = [0,1,2]
a = (-1,3)
a = True
```
Note that when you assign a variable to another, you are just creating a second pointer to that same memory spot.
```python
a = [0,1,2]
b = a
b[2] = 0
print(a)
```
{{% alert note %}}
What would have happened above, if `a` would  have been a tuple instead of a list? Think and then try!
{{% /alert %}}

Being only able to ``interactively'' play with variables is boring.
To build more complex code, we need functions.
A function in Python is defined as follows:
```python
def compute_sum(a,b)
    c = a+b
    return c
```
The function `compute_sum` will receive two arguments (of unspecified type), compute its sum, and return the result.
Note that functions do not necessarily have input and/or output parameters.

It is simple to specify a default value for some argument:
```python
def compute_sum(a,b=2)
    c = a+b
    return c
```

You can also have keyword arguments, specified by name:
```python
print(1,2, sep=';')
```
Keyword arguments must always go behind non-keyword arguments.

When you want to have a function with an undetermined number of arguments, you can use `*args` and `**kwargs`.
```python
def print_all(*args, **kwargs):
    print("arguments = ", args)
    print("keyword arguments = ", kwargs)
```
This is useful to pass lists and dictionaries to a function. More in the homework.
{{% alert warning %}}
Need to explain this
{{% /alert %}}

### 3.6 - Python Classes
How can you go beyond built-in data types and create new types, with their
associated methods and attributes defined by you?
Python allows you to create new classes, and then define (*instantiate*)
new objects of that class and interact with them. This way, you can
group data and functions operating on it in a more abstract way, and
then instantiate concrete samples and use them.
Classes allow for a simplified modeling of our problems, and enables the
creation of cleaner code that can be more easily extended in the future.

{{% alert note %}}
When dealing with classes, data is usually called *attributes*, and functions *methods*.
{{% /alert %}}

Every class needs to have a special method, called `constructor`, that initializes its attributes.
```python
class Y:
    def __init__(self, v0):
        self.v0 = v0
        self.g = 9.81
```
You will note the presence of the `self` parameter: this is a special inner
reference to the object state. It may take some time to understand the use
of `self`, but do not be afraid, we will see some examples afterwards.

As it stands, an object of the `Y` class has very limited value, as it contains only data (attributes).
Let us add some spice by giving our class a function (method):
```python
class Y:
    def __init__(self, v0):
        self.v0 = v0
        self.g = 9.81
    def value(self, t):
        return self.v0 * t - 0.5*self.g*t**2
```
The utility of `self` starts to become clear now. At this point, you have
created a useful class, and you can instantiate an object of this new type easily:
```python
y = Y(3)
print(type(y))
```
As you can see, we call our class as if it was a normal Python function, and Python
automatically invokes the constructor method. `__init__` requires a parameter to be specified
at instantiation time, in this case `3`. If you do not specify it, you will get an error.

Now, attributes and methods are exposed to the user:
```python
print(y.v0)
print(y.g)
print(y.value(t=0.1)
```

How can you add new methods to your class? Let us add a `formula` method
that print the mathematical function used to compute `value`. This method
does not need input parameters, and outputs a string:
```python
class Y:
    def __init__(self, v0):
        self.v0 = v0
        self.g = 9.81
    def value(self, t):
        return self.v0 * t - 0.5*self.g*t**2
    def print_formula(self):
        return ’v0*t - 0.5*g*t**2; v0=%g’ % self.v0
```
Note that even if the formula method does not need any arguments, we still
must add the `self` argument so that it can access the `v0` attribute.
This is omitted in the method call.

**Homework**:

***Protect data from the user (i.e. you!).***
```python
class Person(object):
    def __init__(self, name, mobile_phone=None, office_phone=None, private_phone=None, email=None):
        self.name = name
        self.mobile = mobile_phone
        self.office = office_phone
        self.private = private_phone
        self.email = email

    def add_mobile_phone(self, number):
        self.mobile = number
    def add_office_phone(self, number):
        self.office = number
    def add_private_phone(self, number):
        self.private = number
    def add_email(self, address):
        self.email = address
```
Note the use of None as default value for various data attributes: the object None
is commonly used to indicate that a variable or attribute is defined, but yet not with
a sensible value.

***Class Inheritance:***
Instead of starting from scratch, you can create a class by deriving it
from a preexisting class by listing the parent class in parentheses after the new class name.

```python
class Parent:        # define parent class
   parentAttr = 100
   def __init__(self):
      print "Calling parent constructor"

   def parentMethod(self):
      print 'Calling parent method'

   def setAttr(self, attr):
      Parent.parentAttr = attr

   def getAttr(self):
      print "Parent attribute :", Parent.parentAttr

class Child(Parent): # define child class
   def __init__(self):
      print "Calling child constructor"

   def childMethod(self):
      print 'Calling child method'

c = Child()          # instance of child
c.childMethod()      # child calls its method
c.parentMethod()     # calls parent's method
c.setAttr(200)       # again call parent's method
c.getAttr()          # again call parent's method
```




































## 5. **Homework :scream:**
Here is what I want you to do for next week.
### Review exercises (mandatory)
Here you can find some exercises to review the concepts explained up to now.

### Numpy (mandatory)
Here you can find some exercises to review the concepts explained up to now.

### Dictionaries (mandatory)
Explanation of what a dictionary is.

Here you can find some exercises for dictionaries.

### Classes (mandatory)
Explanation of how classes work in Python.

Here you can find some exercises for classes.

### Debugging in Python (recommended)
Explanation of how to handle exceptions. Look into page 45 of JvdP.

Here you can find some exercises for exceptions.

### Iterators (recommended)
When we saw the example of a for loop, the looping variable traversed a list:
```python
for i in [0,1,2,3]:
    print(i)
```
Actually, the object to the right of `in` needs to be an `iterator`.
A `list` is a special type of `iterator`.
These can be understood as generalized sequences, and will be important in following lectures.
See page 52 of VdP.

Here you can find some exercises for iterators.

### Generators (recommended)
Here you can find some exercises for generators.

## 6. **Sources and References**
Of course, there are tons of wonderful Python resources in the internet.
The main sources I used to build this lecture were:




EXERCISES:
### 1
Consider the following code:
```python
a=[1,2,3]
a[1]=4
```
What is a?
1.- This code contains an error 2.- [1,2,3] 3.- etc.
### 2
Consider the following code:
```python
a=(1,2,3)
a[1]=4
```
What is a?
1.- This code contains an error 2.- [1,2,3] 3.- etc.
### 3
Consider the code:
```python
x = "Hello, world!"
y = x[5:]
```
What is the value of y?
1.- This code contains an error 2.- 'Hello' 3.- etc.
### 4
Consider the following code and output:
```python
x = 1
def my_function():
  x = 2
  print(x)
print(x)
my_function()
print(x)
```
What will be printed?
1.- 1;2;1
2.- 2;2;2
3.- 1;2;2

Explanation: x is first defined globally, with value 1. Then, my_function
creates a variable x with local scope. Therefore, its value does not extend beyond its use in the function.

### 5
Consider the following code:
```python
import math
print(math.cos(math.pi))
-1.0
```
What type of object is math.pi? And math.cos?
int, float, function, string

### 6
Let's say you want to flip a coin until you get 10 heads. Should you use
a for loop or while loop?

### 7
Let's say you want to flip a coin 10 times and count the number of heads.
Should you use a for loop or a while loop?

### 8
Consider the following code and output:
```python
x = 1
while x < 5:
  x *= 2
```
What is the final value of x?
8

