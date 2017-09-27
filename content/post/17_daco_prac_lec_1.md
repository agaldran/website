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
    1. Anaconda Python Distribution
    2. Executing Python code
3. **Introduction to the Python Programming Language**
    1. Fundamental Python data types
    2. Everything is an object
    3. Python Modules
    4. Python Basic Operators
    5. Sequences and Object Containers
    6. Python typing
    7. Flow Control
    8. Python Functions
    9. Classes and Object-Oriented Programming
    

4. **Complementary Python Scientific Computing Tools: Numpy**
    1. Introduction to NumPy Arrays
    2. Slicing NumPy Arrays
    3. Indexing NumPy Arrays
    4. Other numpy arrays manipulation techniques

5. **Complementary Python Scientific Computing Tools: Matplotlib**
    1. Basic Matplotlib usage
    2. Plot Customization

6. **Homework :scream:**

7. **Sources and References**

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
The Anaconda Python distribution can be found [here](https://www.continuum.io/downloads). Please install Python 3. 
For windows users, if you are finding troubles, let me know asap.
{{% /alert %}}


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

{{% alert note %}}
For the contents of this lecture, starting from Section 3, a notebook version of this lecture is available [here](https://github.com/agaldran/daco_2017_practicals/blob/master/lecture_1_python/Practical%20Lecture%201%20-%20Introduction%20to%20Python%20for%20Scientific%20Computing.ipynb). 
Download and open it!
{{% /alert %}}

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
Other basic/common python types are for instance `float`, `string`, or `boolean`, exemplified below:
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
Object **type** tells Python what kind of an object it's dealing with.
A type could be a number, or a string, or a list, or something else.
Object **value** is the data value is contained by the object.
This could be a specific number, for example.
Finally, you can think of object **identity** as an identity number for the object.
Each distinct object in the computer's memory will have its own identity number.

Most Python objects have either data or functions or both associated with them.
These are known as **attributes**.
The name of the attribute follows the name of the object, and they are separated by a dot in between them.
The two types of attributes are called either **data attributes** or **methods**.
A data attribute is a value that is attached to a specific object.
In contrast, a method is a function that is attached to an object.
And typically a method performs some function or some operation on that object.
Object type always determines the kind of operations that it supports.
In other words, depending on the type of the object,
different methods may be available to you as a programmer.
Finally, an **instance** is one occurrence of an object.
For example, you could have two strings.
They may have different values stored in them,
but they nevertheless support the same set of methods.


### 3.3 - Python Modules
Python contains builtin functions, such as ``print`` that can be used by all Python programs.
However, while the Python library consists of all core elements, such as data types and built-in functions,
the bulk of the Python library consists of **modules**.
In order for you to be able to make use of modules in your own code,
you first need to import those modules using the `import` statement.

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
Note this subtle difference between ``==`` and ``is``: 

``==`` tests whether objects have the same value, whereas ``is`` 
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

Continuing with sequences, in order to access the elements that a tuple/list holds, you use **square brackets, not parenthesis**:
```python
# the first element of the tuple t
t_first = t[0]
```
Also note that, the same as e.g. C (and different from e.g. Matlab), **in Python indexing starts at 0**.
Be careful with this, because it is a common source of confusion in the beginning.

Sequences can be accessed by indexing, which supports negatives indexes:
```python
t = (0,1,'hola',3,4.0)
l = [0,1,'hola',3,4.0]
print(t[0])
print(t[-1]) # note the behavior of negative indexes
```

Sequences also support a very handy operation called **slicing**, that enables access to multiple objects at the same time:
```python
print(t[0:2]) # slicing first two elements, third is excluded
print(l[2:5]) # slicing last three elements
print(l[2:]) # empty spot after : means up to length-of-list index
print(l[:2]) # empty spot before : means from first index
print(l[0:5:2]) # every element, but use a step size of 2
```


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

### 3.6 - Python typing
Objects in Python are composed by their name, their content, and a reference that points the name to the content.
When an object is created, Python tells the computer to reserve memory locations to store the corresponding data.
Depending on the data type of a variable, the interpreter allocates a certain amount of memory.

As we have seen above, in Python, there is no need of declaring objects nor their type before using them.
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

### 3.7 Flow Control
Typical flow control structures are implemented as usual in Python.
{{% alert note %}}
Be careful with Python code **indentation**:
the space you leave to the left of your piece of code implicitly delimits code blocks.
{{% /alert %}}
We will learn the behavior of flow control statements in Python by example,
to reinforce the idea of how intuitive Python is.
#### 3.7.1 - `if`-`else` statements
Observe the following code:
```python
if 3>2:
    print('success')
elif 3==2:
    print('failure')
else:
    print('I do not know')
print('This will be printed either way')
```
{{% alert note %}}
Do not forget about the semicolon in the end of control statements!
{{% /alert %}}

#### 3.7.2 - `for` loops  
Observe the following code and try to predict its output:
```python
for i in [0,1,2,3]:
    print(i)
```

#### 3.7.3 - `while` loops
Observe the following code and try to predict its output:
```python
i=0
while i < 4:
    print(i)
    i = i+1
```

#### 3.7.4 - Other statements: `break` and `continue`
Observe the following two pieces of code and try to predict their output:
```python
for i in [1,2,3,4,5,6,7]:
    if i % 3 == 0:
        continue
    print(i)
```
```python
for i in [1,2,3,4,5,6,7]:
    if i % 3 == 0:
        break
    print(i)
```
{{% alert note %}}
Can you give a definition of both statements based on these experiments?
{{% /alert %}}



### 3.8 Python Functions
Being only able to ``interactively'' play with variables is boring.
To build more complex code, we need functions.
Functions are tools for grouping statements so that they can be executed more than once in the same program.
They are useful maximize code reuse and minimize code redundancy, therefore contributing to avoid errors.

Functions are written using the `def` statement.
You can send objects created inside your function back to where it was called with the `return` statement.
```python
def compute_sum(a,b):
    c = a+b
    return c
```
To use this function, we simply call it passing appropriate parameters:
```python
a = 5
b = -2
print(compute_sum(a,b))
```
Arguments to Python functions are matched by position. 
Tuples are typically used to return multiple values.
Note that functions themselves are objects:
```python
print(type(compute_sum))
```

In general, variables created or assigned in a function are local of that function and exist only while the function runs.
```python
L = [0,1,2]
def modify(my_list):
    c = 3
    my_list[0] += 20
modify(L)
print(L)
print(c)
```

It is also possible to specify a **default** value for some argument:
```python
def compute_sum(a,b=2):
    c = a+b
    return c
```

Likewise, you can have keyword arguments.
A keyword argument is an argument which is supplied to the function by explicitly naming each parameter and specifying its value:
```python
print(1, 2, 3, 4, sep=';')
```
Keyword arguments must always go behind non-keyword arguments.



### 3.9 Classes and Object-Oriented Programming
How can you go beyond built-in data types and create **new object types**, with their
associated methods and attributes defined by you?

Python allows you to create new classes, and then define (*instantiate*)
new objects of that class and interact with them. This way, you can
group data and functions operating on it in a more abstract way, and
then instantiate concrete samples and use them.
Classes allow for a simplified modeling of our problems, and enables the
creation of cleaner code that will be more easily extended in the future.

{{% alert note %}}
When dealing with classes, data is usually called *attributes*, and functions *methods*.
{{% /alert %}}

#### 3.9.2 - Building a new Class from scratch
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
print(y.value(t=0.1))
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
        return 'v0*t - 0.5*g*t**2'
```
Note that even if the formula method does not need any arguments, we still
must add the `self` argument so that it can access the `v0` attribute.
This is omitted in the method call.

We know an object consists of both internal data and methods that perform operations on the data.
At some point you may find that existing object types do not fully suit your needs. 
Classes are the tool that allows you to create new types of objects.

#### 3.9.2 - Class Inheritance
Sometimes, even if you have the need for a new type, it may happen that this new object type resembles,
in some way, an existing one.
Classes have the ability to inherit from other classes, and this is a fundamental aspect of OOP.

Let us see an example of how to build a new class, inheriting from the built-in Python `list` class. 
We will add more functionality to it.
 ```python
class MyList(list):
    
```
this definition ensure that our new class, derived from `list`, will inherit the attributes of the base class. 
However, now we can extend, or redefine those attributes!

For instance, we are going to improve the built-in `remove` methods, implemented by Python for lists in this way:
```python
L = [0,1,2,5,5]
L.remove(5)
```
We will add new methods to also be able to remove the maximum and minimum element of a list. 
For this, we complete the definition of our extended class as follows:
```python
class MyList(list):
    def remove_min(self):
        self.remove(min(self))
    def remove_max(self):
        self.remove(max(self))
```
Now we can make use of our class:
```python
L2 = MyList(L)
dir(L)
dir(L2)
print(L2.remove_min())
```

## 4. **Complementary Python Scientific Computing Tools: Numpy**
As mentioned in the introduction, one of the most important strengths of Python is the large ecosystem of tools available.
One of the most important libraries for scientific computing in general (and for this course in particular) is **NumPy**, 
which is designed to perform matrix computations. 
Here you will learn the fundamental concepts related to Numpy. 
### 4.1 - Introduction to NumPy Arrays
Python allows you to create nested lists, that you could use to work with n-dimensional arrays:
```python
zero_matrix = [[0,0,0],[0,0,0]]
print(len(zero_matrix),len(zero_matrix[0]))
```
However, you can see this is quite inconvenient, and complexity will grow a lot with high dimensions. 
Also, Python lists are not designed for linear algebra. For instance, `+` acting on lists means concatenation:
```python
print([1,2]+[0,0])
```

NumPy arrays are n-dimensional array objects which conform the core component of scientific computing in Python.
They are an additional data type provided by NumPy for representing vectors and matrices.
Unlike Python lists, elements of NumPy arrays are all of the same data type, and their size is fixed once defined.
By default, the elements are floating point numbers.

This is a first example of how to build a vector and a matrix with all elements zero.
```python
import numpy as np

zero_vector = np.zeros(4)
zero_matrix = np.zeros((2,3))
```
Note that in the matrix case, we need to specify the dimensions through a tuple. 
In order to build an array of ones, you can use the `numpy.ones` function, with the same syntax:
```python
ones_matrix = np.ones((3,2))
```
Finally, you can manually initialize them using `np.array` and a Python list:
```python
my_matrix = np.array([[2,1],[3,2],[5,4]])
```

`numpy` supports the usual standard matrix operations, such as matrix transposition;
```python
my_transposed_matrix = my_matrix.transpose()
```
Arithmetic operations work as expected also:
```python
my_matrix + ones_matrix
```

Note that unlike MATLAB, `*` is elementwise multiplication, not matrix multiplication. 
You need to use the `dot` function to compute products of vectors, to multiply a vector by a matrix, and to multiply matrices. 
`dot` is available both as a function in the numpy module and as an instance method of array objects:

```python
x = np.array([[1,2],[3,4]]) # 2x2 Matrix
y = np.array([[5,6],[7,8]]) # 2x2 Matrix

v = np.array([9,10]) # 1x2 vector
w = np.array([11, 12]) # 1x2 vector

# Matrix / vector product; both produce a 1x2 vector
print(x.dot(v))
print(np.dot(x, v))

# Matrix / matrix product; both produce a 2x2 matrix
# [[19 22]
#  [43 50]]
print(x.dot(y))
print(np.dot(x, y))
```

Finally, you can find out the dimensions of a given `numpy` array through its `shape` data attribute:
```python
print(my_matrix.shape)
```
### 4.2 - Slicing NumPy Arrays
The same way you can slice Python lists, you can do the same with `numpy` arrays.
Remember the indexing logic.
Start index is included but stop index is not, so `Python` stops just before it reaches the stop index.
```python
my_first_column = my_matrix[:,0]
my_last_row = my_matrix[-1,:]
print(my_first_column.shape)
```

### 4.3 - Indexing NumPy Arrays
NumPy arrays can also be indexed with other arrays or other sequence-like objects like lists. For example:
```python
z1 = np.array([2,4,6,8,10])
z2 = z1+1
indexes_arr = np.array([0,1])
indexes_list = [0, 4]
print(z2, z2[indexes_arr], z2[indexes_list])
```
Another way of indexing `numpy` arrays is with logical indices:
```python
indexes_logical = [True, True, True, False, False]
print(z2[indexes_logical])
```
Note the potential of this operation!
```python
print(z2>5)
print(z2[z2>5])
```

#### Important difference between slicing and indexing
When you slice an array with the colon operator, you obtain a **view** of the object. 
This means that if you modify that view, you will also modify the original array.
In contrast, when you index an array, what you obtain is a (new) object, a copy independent of the original one.
```python
z1 = np.array([2,4,6,8,10])
w_view = z1[0:3] # sliced z1
print(z1)
print(w_view)
w_view[0] = 50
print(z1)
```
Compare the above code snippet with this one:
```python
z1 = np.array([2,4,6,8,10])
indexes = [0,1,2,3,4]
w_copy = z1[indexes] # indexed z1
print(z1)
print(w_copy)
w_copy[0] = 50
print(z1)
```



### 4.4 - Other numpy arrays manipulation techniques
In `numpy`, if you want to build an array with fixed start and end values, such that the other elements are uniformly
spaced between them, you can do the following:
```python
np.linspace(0, 100, 10) # stop point is included
```

We have already seen an example of the attribute `shape` of a `numpy` array. You can also check the total `size` of it:
```python
my_matrix = np.array([[2,1],[3,2],[5,4]])
print(my_matrix.shape)
print(my_matrix.size)
```
Notice that neither `shape` nor `size` are followed by a parenthesis. 
This is because they are not method attributes for the `numpy` array class, but rather data attributes.

There are a couple of handy logical operations that work on top of `numpy` arrays. 
For instance, you often will want to check if any/all of the elements in an array verifies a given condition. 
This can be accomplished with the methods `any()` and `all()`:
```python
x = np.random.random(10)
print(x)
print(np.any(x>0.5))
print(np.all(x>0.5))
```
In this case, instead of using the Python `random` library, we used the `numpy.random` module.

## 5. **Complementary Python Scientific Computing Tools: Matplotlib**
Matplotlib is the standard Python plotting library. 
Even if `matplotlib` is a very large library, it contains a module called `pyplot`.
Pyplot is a collection of functionalities that make matplotlib work in a similar way as Matlab. 
In this course, we will use `pyplot` for our data visualizations. 

### 5.1 - **Basic Matplotlib usage**
Let us import it:
```python
import matplotlib.pyplot as plt
```
The most basic function inside `pyplot` is `plot`. 
Its simplest use case takes only one argument, specifying  the y-axis values that are to be plotted.
In this case, each y-axis value is plotted against its corresponding index value on the x-axis:
```python
y = np.random.random(10)
plt.plot(y)
```
If you use `plot` outside the iPython shell, the plot is created but not shown. 
To tell Python to show the plot, you just need to add `plt.show()` to your code.

When you give to `plot` two arguments, the first argument specifies the x-coordinates and the second the y-coordinates.
```python
x = np.linspace(0,10,100)
y = np.cos(x)
plt.plot(x,y)
```
You can also supply a third argument to `plot` in order to give some cosmetic specifications on your plot, like color, line type or marker.
They work with key-word arguments.
```python
x = np.linspace(0,10,20)
y = np.cos(x)
plt.plot(x, y, 'ro-')
plt.show()
plt.plot(x, y, 'gs-', linewidth=5, markersize=15)
```
Note that in this case `plt.show()` forces Python to show the first plot, which otherwise would be ommited.

### 5.2 - **Plot Customization**
Let us see some more advanced plot customization techniques.
To add a legend to an already created (even if still not shown) plot, you can use `legend()`, which takes a string as an argument:
```python
x = np.linspace(-3,3,20)
y = x**2
plt.plot(x, y, 'ro-')
```
If you want to add information on which quantities are specified on each axis, you can do it as follows:
```python
x = np.linspace(-3,3,20)
y = x**2
plt.plot(x, y, 'ro-')
plt.xlabel('The x axis')
plt.ylabel('The y axis')
```
You can also customize what part of your plot you want to display with `axis()`:
```python
x = np.linspace(-3,3,20)
y = x**2
plt.plot(x, y, 'ro-')
plt.axis([-0.5, 2, -2, 4]) #xmin, xmax, ymin, ymax
```

It is also quite easy to overlay several plots:
```python
x = np.linspace(-3,3,20)
y1 = x**2
y2 = x**3
plt.plot(x, y1, 'ro-')
plt.plot(x,y2, 'b+-')
```
If you need to add an independent legend to each of these, you need to label each of them separately:
```python
x = np.linspace(-3,3,20)
y1 = x**2
y2 = x**3
plt.plot(x, y1, 'ro-', label = 'square')
plt.plot(x,y2, 'b+-', label = 'cubic')
plt.legend(loc = 'upper left')
```
Note that `legend()` can take a keyword argument specifying location.

Finally, to save your figure, you simple use `savefig`. 
The extension of the file name you choose will determine the format of the output.
```python
x = np.linspace(-3,3,20)
y1 = x**2
plt.plot(x, y1, 'ro-', label = 'square')
plt.savefig('my_plot.png')
```

Finally, let us illustrate the use of histogram plotting tools in matplotlib, as well as how to build several subplots in the same plot.
First, we create a normally distributed array of numbers around zero using numpy as follows:
```python
x = np.random.normal(size = 1000)
```
To build a histogram plot in pyplot we type:
```python
plt.hist(x)
```
Now, if you want to plot the same histogram with two different colors in two different subplots, you can use the `plt.subplot()` function.
This function takes three arguments: the first two specify the number of rows and columns in the subplot, and the third one is the plot number.
```python
plt.subplot(1,2,1)
plt.hist(x, color = 'r');
plt.subplot(1,2,2)
plt.hist(x, color = 'b');
```
Note the use of a semicolon after each plot execution, in order to avoid printing the value returned by `matplotlib`.




## 6. **Sources and References**
Of course, there are tons of wonderful Python resources in the internet.
The main sources I used to build this lecture were:

1. Jake Van der Plas' book *A Whilrwind Tour of Python*, available [here](http://www.oreilly.com/programming/free/files/a-whirlwind-tour-of-python.pdf) 
in pdf, and [here](https://github.com/jakevdp/WhirlwindTourOfPython) in iPython notebook format.

2. Harvard's online course *Using Python for Research*, hosted at [edX](https://courses.edx.org/courses/course-v1:HarvardX+PH526x+3T2016/course/)

3. Stanford's CS231n short Python tutorial [here](http://cs231n.github.io/python-numpy-tutorial/)

In general, most of the material and presentation is shamelessly inspired in 2.

Regarding the `numpy` part, if you are a Matlab user, you could find this resource very useful:
- Numpy for Matlab users - [link](http://scipy.github.io/old-wiki/pages/NumPy_for_Matlab_Users)

If you need or want more practice with Python and the tools presented today, I would recommend following the free course 
at [datacamp](https://www.datacamp.com/courses/intro-to-python-for-data-science), and doing all the exercises proposed there.
Codeacademy exercises, hosted [here](https://www.codecademy.com/learn/learn-python), can also be very useful to get more experience.



