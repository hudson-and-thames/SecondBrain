# K-Fold Cross-Validation
Cross-validation is a resampling procedure used to evaluate machine learning models on a limited data sample.

The procedure has a single parameter called k that refers to the number of groups that a given data sample is to be split into. As such, the procedure is often called k-fold cross-validation. When a specific value for k is chosen, it may be used in place of k in the reference to the model, such as k=10 becoming 10-fold cross-validation.

Cross-validation is primarily used in applied machine learning to estimate the skill of a machine learning model on unseen data. That is, to use a limited sample in order to estimate how the model is expected to perform in general when used to make predictions on data not used during the training of the model.

It is a popular method because it is simple to understand and because it generally results in a less biased or less optimistic estimate of the model skill than other methods, such as a simple train/test split.

The general procedure is as follows:

1.  Shuffle the dataset randomly.
2.  Split the dataset into k groups
3.  For each unique group:
    1.  Take the group as a hold out or test data set
    2.  Take the remaining groups as a training data set
    3.  Fit a model on the training set and evaluate it on the test set
    4.  Retain the evaluation score and discard the model
4.  Summarize the skill of the model using the sample of model evaluation scores

Importantly, each observation in the data sample is assigned to an individual group and stays in that group for the duration of the procedure. This means that each sample is given the opportunity to be used in the hold out set 1 time and used to train the model k-1 times.

> This approach involves randomly dividing the set of observations into k groups, or folds, of approximately equal size. The first fold is treated as a validation set, and the method is fit on the remaining k − 1 folds.

— Page 181, [An Introduction to Statistical Learning](https://amzn.to/2FkHqvW), 2013.

It is also important that any preparation of the data prior to fitting the model occur on the CV-assigned training dataset within the loop rather than on the broader data set. This also applies to any tuning of hyperparameters. A failure to perform these operations within the loop may result in [data leakage](https://machinelearningmastery.com/data-leakage-machine-learning/) and an optimistic estimate of the model skill.

> Despite the best efforts of statistical methodologists, users frequently invalidate their results by inadvertently peeking at the test data.

— Page 708, [Artificial Intelligence: A Modern Approach (3rd Edition)](https://amzn.to/2thrWHq), 2009.

The results of a k-fold cross-validation run are often summarized with the mean of the model skill scores. It is also good practice to include a measure of the variance of the skill scores, such as the standard deviation or standard error.

https://machinelearningmastery.com/k-fold-cross-validation/
---
Topics: [[Machine Learning]]
Reference: [[Model evaluation]]
Type: #atom
Creator :: Jacques
Date: 2022-06-28 13:55