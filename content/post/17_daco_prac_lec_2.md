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
    3. Aside: Working from Spyder
    4. Quick overview of scikit-learn

2. **Bayesian Classification: a bit of theory**

3. **Naive Bayes Classifier Implementation**
    1. From scratch
    2. Using scikit-learn

4. **Linear Regression: a (tiny) bit of theory**
    
5. **Linear Regression Using scikit-learn**

6. **Homework :scream:**

7. **Sources and References**
 
# 1.- **Motivation and Goals. Machine Learning for Supervised Classification and Regression**
As you will know, this course is all about about making predictions out of data and annotations. 
But there are several different kinds of predictions, and hence several tasks that we can solve.
Among the most fundamental ones are Supervised Classification and Supervised Regression.

**Note:** The term **supervised** refers to the fact that we assume we have data with annotations. 
A different kind of models exist related to the situation where there is no annotations, and the goal is to extract some useful information out of the available (unlabeled) data. This is called **unsupervised** learning.

For instance, we could think of a dataset with customer preferences regarding certain products. 
Could we group a given pool of users into several subgroups that behave similar among them, but differently with respect to the other subgroups?
This task is known as clustering, and we will be working on it in future lectures. 
But for now, we assume for each example in our dataset, we know the corresponding quantity of interest. 

## 1.1 - **Difference between Classification and Regression**
**Classification**: in your data every examples is associated to two or more classes. You want to learn from this labeled data how to predict the class of new unlabeled data. 

Example: Given a set of lung CT scans, a doctor has annotated each of them after examination, specifying whether they show or not signs of lung cancer.

**Regression**: In this case, the output of your model is is not a discrete label, but a real number. 

Example: given a training set in which you have examples of red and white globule concentration, predict the amount of blood pressure. In this case, the output (blood pressure) is not a single label, but a number.

Both classification and regressoin are supervised learning problems, since there is labeled data available. However, the discrete nature of classification, as opposed to continuous for regression, require different types of learning models.


## 1.2 - **Difference between Generative and Discriminative models**
In (supervised) learning we always have a dataset of examples with associated labels. 
However, we do not usually feed our models with the raw data (with a super-relevant exception that we will see later in this course). 

For instance, imagine I have a dataset of all the movies I watched in 2016 and 2017, and each movie is tagged with a label indicating whether I liked it or not. 
If I want to build a model that takes a new movie and predicts if I will like it or not, I am not going to give to my classifier every frame of the movie and let it process it. Rather I am going to extract some key information summarizing the movie, such as genre, actors and actresses, duration, soundtrack, etc. 
We call these key informative traits of our data **features**, and their selection is

Imagine now that I decided that with the duration and rating of the movie in IMDB, I can already describe the movie in such a way that I can build a classifier for my problem. 
We can build the following plot:

```python
import numpy as np
import matplotlib.pyplot as plt
from sklearn.datasets import make_blobs
%matplotlib inline

# create some synthetic data
n_samples = 100
n_features = 2
movies_mean = [[1.5, 7], [2, 8]] # [mean_movie_duration, mean_IMDB_score]
movies_std = (0.25, 0.25) # [std_movie_duration, std_IMDB_score]
movies, like_it_or_not = make_blobs(n_samples, n_features, movies_mean, movies_std)


movies_I_liked = movies[like_it_or_not==1]
movies_I_disliked = movies[like_it_or_not==0]

# plot data points
plt.scatter(movies_I_liked[:,0],movies_I_liked[:,1], marker = 'o', color = 'g', label = 'Liked');
plt.scatter(movies_I_disliked[:,0],movies_I_disliked[:,1], marker = 'o', color = 'r', label = 'Disliked');
plt.xlabel('duration');
plt.ylabel('IMDB rating');
plt.legend();
plt.show()
```


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