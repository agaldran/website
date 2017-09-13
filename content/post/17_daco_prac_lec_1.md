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

This year we have decided to move from Matlab to Python for the practical sessions.
Some of you maybe will not have worked with this programming language.
This first lecture is intended to make you aware of the (super-rich) Python ecosystem for scientific computing.

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
And last, there is a **huge** community of contributors to lots of open-source projects that complement it.
This manifests in the form of a large ecosystem of scientific computing tools that grow along with the number of users.

However, to add all this to your toolbelt, the first step is to familiarize yourself with the Python language itself.
Today we will quickly traverse the main notions to get started on that.

But first, let us install Python!

## 2. **Python Installation. Accompanying Tools.**
Conda/Anaconda. Command Line. Package Manager. IDEs. Ipython Notebooks.

## 3. **Introduction to the Python Programming Language**
### 3.1 - Data Types:
The same as in any language, Python also has different types of data.
The same as in e.g Matlab (and different from e.g. C) you do not need to explicitly declare the type of a variable.
Python determines data type of variables by how they are used.
For instance, to create an integer (`int`) variable you simply type:
```python
# An integer variable a
a = 5
print(type(a))
```
`print` and `type` are a built-in Python functions that behave as you would expect.
More on functions later.
Note that in Python 2 you would not use parentheses with `print`
Other basic/common python types are for instance`float`, `string`, or `boolean`, exemplified below:
```python
# A float variable f
f = 5.0
# A boolean
b = True
# A string
c = 'bom dia'
```
In order to create a collection of data, the most basic python objects are `list` and `tuple`:
```python
# A tuple
t = (0,True)
# A list l
l = [0,True]
```
Note that there is a relevant difference between tuples and lists: tuples are **immutable**, while lists aren't.
This means that you won't be able to modify the content stored at `t`. We will see that in a second.
Note also that both allow you to mix different data types.
In order to access the elements that a tuple/list holds, you use **square brackets, not parenthesis**:
```python
# the first element of t
t_first = t[0]
```
Also note that, the same as e.g. C (and different from e.g. Matlab), **in Python indexing starts at 0**.
Be careful with this, because it can be a common source of confusion in the beginning.

Lists and tuples can be accessed by indexing and can be sliced in several ways:
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

{{% alert note %}}
What does mutable/immutable mean?
{{% /alert %}}
[*Try accessing and modifying the second element of `t` and `l` to discover this.*]

Actually, `list` and `tuple` are examples of Python *containers*.
These are data types that can, well, contain other data.
A list is an example of a container, and it can contain integers, floats, or other containers, such as more lists:
```python
# A list of lists
l = [[0],[1],[2,3]]
```
{{% alert note %}}
Which is the type of the first element of `l`? And of `t`?
{{% /alert %}}
[*Find out, using `type` and print*]




Apart from `list` and `tuple`, a very useful container are dictionaries.
You can find information on them for instance in [this page](https://www.tutorialspoint.com/python/python_dictionary.htm).
You will get to practice with them in the homework.

### 3.2 - Python Operators:
Operators are symbols that allow you to use logic and arithmetic in your computations.
Python has several operators, the most prominent ones being **arithmetic**, **comparison**, and **logical**.
#### Arithmetic operators:
They will take two variables and perform simple mathematical operations on them.
They are addition `+`, subtraction `-`, multiplication `*`, division `/`, modulus `%`, floor division `//`, and exponentiation `**`
```python
print(3+2, 3-2, 3*2, 3/2, 3%2, 3//2, 3**2)
```
#### Comparison operators:
They observe two variables and return a boolean value.
They are the usual greater than (`>`,`>=`), equal (`=`), different (`!=`), and lower than (`<`,`<=`) mathematical operators.
```python
print(3>2, 3<2, 3==2, 3!=2, 3>=2, 3<=2)
```
#### Logical operators:
These operators will interpret their input as boolean values, and return a boolean value depending on the truth value of both inputs.
They are `and`, `or`, `not`.
```python
print(True and True, False or False, not True)
```
#### Other operators
There are other operators in Python, such as identity (`is`, `is not`) or membership (`in`, `not in`).
I am 100% sure you will be able to guess what is their effect on variables/containers!

### 3.3 - Flow Control in Python
Typical flow control structures are implemented as usual in Python.
{{% alert note %}}
Be careful with Python code **indentation**:
space left to the left of the code is an implicit encloser of code blocks.
{{% /alert %}}

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
Based on the data type of a variable, the interpreter allocates a certain amount of memory depending on it.

As we have seen above, in Python, there is no need of declaring variables before using them.
This is because actually what you are doing is not creating a spot in memory and filling it with an object.
Rather, you are creating a pointer (that occupies a first memory spot), and then making that pointer point to an object in a second memory spot.
For this reason, you can for instance reassign a variable to a different type of object without errors:
```python
a = [0,1,2]
a = True
a = (-1,3)
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
Note that function does not necessarily have input and/or output parameters.

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

### 3.5- Python Objects
Python is an Object Oriented programming language.
In this paradigm, an object is an entity that contains data along with some metadata and/or functionality.
Objects are the main tool to operate with data, store and reference it.
In Python everything is an object, which means every entity has some metadata (**attributes**) and associated functionality (**methods**).
These attributes and methods are accessed via the dot syntax.

For example, lists have several methods that you can use with them:
```python
a = [4,3,2,1]
a.append(5)
print(a)
a.sort()
print(a)
```
For a complete list of these, see [here](http://faculty.salina.k-state.edu/tim/NPstudy_guide/python/containers.html#list-methods).

Note that even basic types have attributes and methods:
```python
a = 5.0
print(a.is_integer())
```
In Python, even methods themselves are objects of a given type:
```python
print(type(compute_sum))
print(type(compute_sum(1.0,2))
```

### 3.6 - Python Classes
How can you go beyond built-in data types and create new types, with their associated methods and attributes defined by you?
Python allows you to create new classes, and then instantiate new objects of that class and interact with them.

### 3.7 - Modules and Packages
In Python, you have modules and packages.


## 4. **Complementary Python Scientific Computing Tools**
Numpy, Matplotlib. Spyder.

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
