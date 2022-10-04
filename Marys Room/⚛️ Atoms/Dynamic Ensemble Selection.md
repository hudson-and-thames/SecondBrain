# Dynamic Ensemble Selection

**Dynamic ensemble selection** is an [[Ensemble]] learning technique that automatically selects a subset of ensemble members just-in-time when making a prediction.

The technique involves fitting multiple machine learning models on the training dataset, then selecting the models that are expected to perform best when making a prediction for a specific new example, based on the details of the example to be predicted.

This can be achieved using a k-nearest neighbour model to locate examples in the training dataset that are closest to the new example to be predicted, evaluating all models in the pool on this neighbourhood and using the models that perform the best on the neighbourhood to make a prediction for the new example.

As such, the dynamic ensemble selection can often perform better than any single model in the pool and better than averaging all members of the pool, so-called static ensemble selection.

In this way it falls within [[Model Selection]] frameworks.

![[Pasted image 20220715105804.png]]

---
Topics :: [[Machine Learning]]
Reference :: [[Model Selection]]
Type :: #atom
Creator :: Dennis
TAF :: Michael Jacques
Date :: 2022-07-07 10:26