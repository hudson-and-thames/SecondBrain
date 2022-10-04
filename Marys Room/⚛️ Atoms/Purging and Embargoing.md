# Purging and Embargoing
Helps to solve the problem of [[Cross-Validation Leakage]] and is a suggested solution in [[10 Reasons Most Machine Learning Funds Fail]].

## Purging
* Eliminating all observations from the training set that overlapped in time with the labels in the test set.
* This is the last portion of data in the train set for CV.

## Embargo
* Eliminating all observations from the training set that immediately follow an observation in the testing set.
* This is the fist portion of data in the train set for CV.


---
Topics: [[Quantitative Finance]], [[Machine Learning]]
Reference: [[Advances in Financial Machine Learning]], [[10 Reasons Most Machine Learning Funds Fail]]
Creator:: Jacques
Type: #atom
Date: 2022-06-28 12:47