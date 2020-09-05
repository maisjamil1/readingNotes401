# Machine learning
## Machine learning is a comprehensive approach to solving problems.
### What makes machine learning so special?
Machine learning is the practice of teaching computers how to learn patterns from data, often for making decisions or predictions.
For true machine learning, the computer must be able to learn patterns that it's not explicitly programmed to identify.
### Machine Learning Tasks
Academic machine learning starts with and focuses on individual algorithms. However, in applied machine learning, you should first pick the right machine learning task for the job.

### The two most common categories of tasks are supervised learning and unsupervised learning. (There are other tasks as well, but the concepts you'll learn in this course will be widely applicable.)

* Supervised Learning
Supervised learning includes tasks for "labeled" data (i.e. you have a target variable).


* Unsupervised Learning
Unsupervised learning includes tasks for "unlabeled" data (i.e. you do not have a target variable).

### The Blueprint
Our machine learning blueprint is designed around those 3 elements.

There are 5 core steps:

1- Exploratory Analysis

First, "get to know" the data. This step should be quick, efficient, and decisive.

2- Data Cleaning

Then, clean your data to avoid many common pitfalls. Better data beats fancier algorithms.

3- Feature Engineering

Next, help your algorithms "focus" on what's important by creating new features.

4- Algorithm Selection

Choose the best, most appropriate algorithms without wasting your time.

5- Model Training

Finally, train your models. This step is pretty formulaic once you've done the first 4.

## Start with Basics
First, you'll want to answer a set of basic questions about the dataset:

How many observations do I have?
How many features?
What are the data types of my features? Are they numeric? Categorical?
Do I have a target variable?

## Data cleaning
Data cleaning is one those things that everyone does but no one really talks about. Sure, it’s not the "sexiest" part of machine learning. And no, there aren’t hidden tricks and secrets to uncover.

However, proper data cleaning can make or break your project. Professional data scientists usually spend a very large portion of their time on this step.

Why? Because of a simple truth in machine learning:

Better data beats fancier algorithms.

## What is Feature Engineering?
Feature engineering is about creating new input features from your existing ones.

In general, you can think of data cleaning as a process of subtraction and feature engineering as a process of addition.

This is often one of the most valuable tasks a data scientist can do to improve model performance, for 3 big reasons:

You can isolate and highlight key information, which helps your algorithms "focus" on what’s important.
You can bring in your own domain expertise.
Most importantly, once you understand the "vocabulary" of feature engineering, you can bring in other people’s domain expertise!
## Model Training
- Split Dataset

Think of your data as a limited resource.
You can spend some of it to train your model (i.e. feed it to the algorithm).
You can spend some of it to evaluate (test) your model.
But you can’t reuse the same data for both!
If you evaluate your model on the same data you used to train it, your model could be very overfit and you wouldn’t even know! A model should be judged on its ability to predict new, unseen data.

