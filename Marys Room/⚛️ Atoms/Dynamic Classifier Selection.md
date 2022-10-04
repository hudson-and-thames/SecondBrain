# Dynamic Classifier Selection
Multiple Classifier Systems refer to a field of machine learning algorithms that use multiple models to address classification predictive modeling problems.

The first class of multiple classifier systems to find success is referred to as Dynamic Classifier Selection, or DCS for short.

**Dynamic Classifier Selection**: Algorithms that dynamically choose one from among many trained models to make a prediction based on the specific details of the input.

Dynamic Classifier Selection algorithms generally involve partitioning the input feature space in some way and assigning specific models to be responsible for making predictions for each partition. There are a variety of different DCS algorithms and research efforts are mainly focused on how to evaluate and assign classifiers to specific regions of the input space.

> After training multiple individual learners, DCS dynamically selects one learner for each test instance. […] DCS makes predictions by using one individual learner.

— Page 93, [Ensemble Methods: Foundations and Algorithms](https://amzn.to/32L1yWD), 2012.

A natural extension to DCS is algorithms that select one or more models dynamically in order to make a prediction. That is, selecting a subset or ensemble of classifiers dynamically. These techniques are referred to as [[Dynamic Ensemble Selection]], or DES.

---
Topics :: [[Model Selection]]
Reference :: [[Dynamic Ensemble Selection]]
Type :: #atom
Creator :: Dennis
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-15 17:10
