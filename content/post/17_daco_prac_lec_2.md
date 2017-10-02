+++
date = 2017-09-11
draft = false
tags = ["daco_prac_17"]
title = "DACO - Practical Lecture 2 - Bayesian Classification and Linear Regression"
math = false
summary = """
Where we introduce the scikit-learn library for Machine Learning. We learn about Classification with 
the Naive Bayes classifier, and Regression with a simple Linear Regression model.
"""
+++

This practical lecture is again based on Jupyter Notebooks, but for the theory bits you can also find some supporting 
material in the slides mentioned above. Note that we discuss Linear Regression in Theoretical Lecture 6, see [here](). 
For this reason, we will only be using them as a black-box today, to familiarize ourselves with sk-learn for regression tasks. 

Here is the plan for today:

1. **Motivation and Goals. Machine Learning for Supervised Classification and Regression**
    1. Difference between Classification and Regression
    2. Difference between Generative and Discriminative models
    3. Quick overview of scikit-learn

2. **Bayesian Classification: a bit of theory**

3. **Naive Bayes Classifier Implementation**
    1. From scratch
    2. Using scikit-learn

4. **Linear Regression: a (tiny) bit of theory**
    
5. **Linear Regression Implementation**
    1. From scratch
    2. Using scikit-learn

6. **Homework :scream:**

7. **Sources and References**
 
# 1.- **Motivation and Goals. Machine Learning for Supervised Classification and Regression**
As you will know, this course is all about about making predictions out of data and annotations. 
But there are several different kinds of predictions, and hence several tasks that we can solve.
Among the most fundamental ones are Supervised Classification and Supervised Regression.

**Note:** The term **supervised** refers to the fact that we assume we have data with annotations. 
A different kind of models exist related to the situation where there is no annotations, and the goal is to extract some 
useful information out of the available (unlabeled) data. 
For instance, we could think of a dataset with customer preferences regarding certain products. 
Could we group a given pool of users into several subgroups that behave similar among them, but differently with respect to the other subgroups?
This task is known as clustering, and we will be working on it in future lectures. 
But for now, we assume for each example in our dataset, we know the corresponding quantity of interest. 

## 1.1 - **Difference between Classification and Regression**
This is better understood by example.

## 1.2 - **Difference between Generative and Discriminative models**
See [here](https://www.cs.toronto.edu/~duvenaud/courses/csc2541/index.html) for a definition of Generative models.

## 1.3 - **Quick overview of scikit-learn**
See [here](scikit-learn.org) for an introduction to scikit-learn.

-----------------------------------------------------------------------------

# 2.- **Bayesian Classification: a bit of theory**
You have already seen this in class.

-----------------------------------------------------------------------------

# 3.- **Naive Bayes Classifier Implementation**
How do we implement those ideas?


## 3.1 - **From scratch**
Without relying on external libraries, so that you understand what is going on.


## 3.2 - **Using scikit-learn**
sk-learn implementation, that you can bet is better than the above.

-----------------------------------------------------------------------------

# 3.- **Linear Regression: a (tiny) bit of theory**
You have already seen this in class, or will see it. See [here](google.es)

-----------------------------------------------------------------------------

# 4.- **Linear Regression Implementation**
How do we implement those ideas?

## 4.1 - **From scratch**
This is covered in the theory class, see [here](google.es).

## 4.2 - **Using scikit-learn**
sk-learn implementation, that you can bet is better than the above.

-----------------------------------------------------------------------------

# 6. **Homework**
For now, you can access a notebook with an exercise on Python classes [here](google.es). I will be adding another problem in the next days.



# 7. **Sources and References**