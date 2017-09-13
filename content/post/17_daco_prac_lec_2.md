+++
date = 2017-09-11
draft = false
tags = ["daco_prac_17"]
title = "DACO - Practical Lecture 2 - Bayesian Classification and Linear Regression"
math = false
+++
Where we introduce the scikit-learn library for Machine Learning.
We will code from scratch a Naive Bayes classifier and a Linear Regressor,
and compare them with sk-learn implementations.

This year we have decided to move from Matlab to Python for the practical sessions.
Some of you maybe will not have worked with this programming language.
This first lecture is intended to make you aware of the (super-rich) Python ecosystem for scientific computing.

I really hope that by the end of this course you will be a Python fan, and consider abandoning Matlab once and forever!
This is an overview of what you will be learning today:

1. Motivation and Goals. What is Python?

2. Python Installation. Accompanying Tools.

3. A Swift Introduction to the Python Programming Language

4. Complementary Python Scientific Computing Tools

5. Homework :scream:

6. Sources and References

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

1. **first**
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
Other basic/common python types are for instance`float` or `boolean`, exemplified below:
```python
# A float variable f
f = 5.0
# A boolean
b = True
```
2. second

3. third

Python has lots of operators, the most prominent ones being **arithmetic**, **comparison**, and **logical**.
-- Arithmetic operators will take two variables and perform simple mathematical operations on them.
They are addition, subtraction, multiplication, division, modulus, floor division, and exponentiation.
```python
# A list of lists
l = [[0],[1],[2,3]]
```
-- Comparison operators observe two variables and return a boolean value.
