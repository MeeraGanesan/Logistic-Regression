# Logistic-Regression

Note: Code is kept private, can show on a need-to-know basis.

This project implements a logistic regression model as the core of natural language processing system.

It is a sentiment polarity analyzer that uses binary logistic regression. This algorithm helps determine whether a review is positive or negative using movie reviews as data. It uses some basic feature engineering to improve the learner's performance on this task. 

The data provided has a review and a label (0 for negative review and 1 for positive). The dataset has been divided into a training, a validation, and a test dataset. There is also a dictionary containing all vocabulary that is considered in the model. 

The first program converts raw data into formatted training, validation, and test data. There are 2 different feature extraction models used:

1. This model uses a bag-of-words feature vector indicating which words in the dictionary occur at least once in the movie review example. So, there are |dictionary| entries in the indicator vector. An entry is set to 1 if that correspoding word occurs in the movie review.
2. This model makes use of word-to-vector embeddings that are reduced dimension vector representations of words. Given a movie review, the feature vector is the normalized sum of the embeddings of words in the review.

The model uses the negative conditional log-likelihood of the training data as the objective function for gradient descent.

The program also computes the training and test erorr.
