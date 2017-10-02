+++
date = 2017-09-11
draft = true
tags = ["daco_prac_17"]
title = "DACO - Practical Lecture 1 - Introduction to Python for Scientific Computing"
math = false
summary = """
Where we learn the basics of how set up a Python-based system to develop Machine Learning,
Computer Vision, and Image Processing projects.
"""
+++


EXERCISES:
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

### *kwargs and **kwargs (recommended)


### 1
Consider the following code:
```python4.- We are going to count the frequency of each letter in a given string. 
 
4.1) import the `string` library.
Now create a variable `alphabet` that consists of the lowercase and uppercase letters in the English alphabet. For this, 
use the `ascii_lett4.- We are going to count the frequency of each letter in a given string. 
 
4.1) import the `string` library.
Now create a variable `alphabet` that consists of the lowercase and uppercase letters in the English alphabet. For this, 
use the `ascii_letters` attribute of the string library.

4.2) Now, consider the sentence 'Jim quickly realized that the beautiful gowns are expensive'. 
Create a dictionary `count_letters` with keys consisting of each unique letter in the sentence and values consisting of 
the number of times each letter is used in this sentence. 
Count both upper case and lower case letters separately in the dictionary.

Hint: You can loop (`for`) over each letter in your sentence, check (`if`) if the letter is already among your dictionary keys, and otherwise, update your dictionary with a new key.
For that, you can count the number of occurrences with the method `count`, which you can look up in google. 
Do not forget to omit the blank space in `sentence`!

4.3) Use the code you built in 4.2) to create a function called `counter` that takes a string `input_string` and returns 
a dictionary of letter counts `count_letters`. Test it with `sentence`.

4.4) Use the dictionary created by your function to find out and print the most frequent letter in `sentence`.

5.- The distance between two points `x` and `y` is the square root of the sum of squared differences along each dimension of `x` and `y`. 
Build a function `distance(x, y)` that takes two vectors and outputs the distance between them. 
Use your function to find the distance between `x=(0,0)` and `y=(1,1)`, and between `x=(0,0,0)` and `y=(1,1,1)` 

Hint: To be able to take the square root, import the `math` library. ers` attribute of the string library.

4.2) Now, consider the sentence 'Jim quickly realized that the beautiful gowns are expensive'. 
Create a dictionary `count_letters` with keys consisting of each unique letter in the sentence and values consisting of 
the number of times each letter is used in this sentence. 
Count both upper case and lower case letters separately in the dictionary.

Hint: You can loop (`for`) over each letter in your sentence, check (`if`) if the letter is already among your dictionary keys, and otherwise, update your dictionary with a new key.
For that, you can count the number of occurrences with the method `count`, which you can look up in google. 
Do not forget to omit the blank space in `sentence`!

4.3) Use the code you built in 4.2) to create a function called `counter` that takes a string `input_string` and returns 
a dictionary of letter counts `count_letters`. Test it with `sentence`.

4.4) Use the dictionary created by your function to find out and print the most frequent letter in `sentence`.

5.- The distance between two points `x` and `y` is the square root of the sum of squared differences along each dimension of `x` and `y`. 
Build a function `distance(x, y)` that takes two vectors and outputs the distance between them. 
Use your function to find the distance between `x=(0,0)` and `y=(1,1)`, and between `x=(0,0,0)` and `y=(1,1,1)` 

Hint: To be able to take the square root, import the `math` library. 
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

4.- We are going to count the frequency of each letter in a given string. 
 
4.1) import the `string` library.
Now create a variable `alphabet` that consists of the lowercase and uppercase letters in the English alphabet. For this, 
use the `ascii_letters` attribute of the string library.

4.2) Now, consider the sentence 'Jim quickly realized that the beautiful gowns are expensive'. 
Create a dictionary `count_letters` with keys consisting of each unique letter in the sentence and values consisting of 
the number of times each letter is used in this sentence. 
Count both upper case and lower case letters separately in the dictionary.

Hint: You can loop (`for`) over each letter in your sentence, check (`if`) if the letter is already among your dictionary keys, and otherwise, update your dictionary with a new key.
For that, you can count the number of occurrences with the method `count`, which you can look up in google. 
Do not forget to omit the blank space in `sentence`!

4.3) Use the code you built in 4.2) to create a function called `counter` that takes a string `input_string` and returns 
a dictionary of letter counts `count_letters`. Test it with `sentence`.

4.4) Use the dictionary created by your function to find out and print the most frequent letter in `sentence`.

5.- The distance between two points `x` and `y` is the square root of the sum of squared differences along each dimension of `x` and `y`. 
Build a function `distance(x, y)` that takes two vectors and outputs the distance between them. 
Use your function to find the distance between `x=(0,0)` and `y=(1,1)`, and between `x=(0,0,0)` and `y=(1,1,1)` 

Hint: To be able to take the square root, import the `math` library. 