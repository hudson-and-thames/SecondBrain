# Voting
A voting ensemble (or a “_majority voting ensemble_“) is an ensemble machine learning model that combines the predictions from multiple other models.

It is a technique that may be used to improve model performance, ideally achieving better performance than any single model used in the ensemble.

A voting ensemble works by combining the predictions from multiple models. It can be used for classification or regression. In the case of regression, this involves calculating the average of the predictions from the models. In the case of classification, the predictions for each label are summed and the label with the majority vote is predicted.

- **Regression Voting Ensemble**: Predictions are the average of contributing models.
- **Classification Voting Ensemble**: Predictions are the majority vote of contributing models.

There are two approaches to the majority vote prediction for classification; they are hard voting and soft voting.

Hard voting involves summing the predictions for each class label and predicting the class label with the most votes. Soft voting involves summing the predicted probabilities (or probability-like scores) for each class label and predicting the class label with the largest probability.

- **Hard Voting**. Predict the class with the largest sum of votes from models
- **Soft Voting**. Predict the class with the largest summed probability from models.

A voting ensemble may be considered a meta-model, a model of models.

As a meta-model, it could be used with any collection of existing trained machine learning models and the existing models do not need to be aware that they are being used in the ensemble. This means you could explore using a voting ensemble on any set or subset of fit models for your predictive modeling task.

A voting ensemble is appropriate when you have two or more models that perform well on a predictive modeling task. The models used in the ensemble must mostly agree with their predictions.

> One way to combine outputs is by voting—the same mechanism used in bagging. However, (unweighted) voting only makes sense if the learning schemes perform comparably well. If two of the three classifiers make predictions that are grossly incorrect, we will be in trouble!

— Page 497, [Data Mining: Practical Machine Learning Tools and Techniques](https://amzn.to/2NJT1L8), 2016.

Use voting ensembles when:

-   All models in the ensemble have generally the same good performance.
-   All models in the ensemble mostly already agree.

Hard voting is appropriate when the models used in the voting ensemble predict crisp class labels. Soft voting is appropriate when the models used in the voting ensemble predict the probability of class membership. Soft voting can be used for models that do not natively predict a class membership probability, although may require [calibration of their probability-like scores](https://machinelearningmastery.com/calibrated-classification-model-in-scikit-learn/) prior to being used in the ensemble (e.g. support vector machine, k-nearest neighbors, and decision trees).

-   Hard voting is for models that predict class labels.
-   Soft voting is for models that predict class membership probabilities.

The voting ensemble is not guaranteed to provide better performance than any single model used in the ensemble. If any given model used in the ensemble performs better than the voting ensemble, that model should probably be used instead of the voting ensemble.

This is not always the case. A voting ensemble can offer lower variance in the predictions made over individual models. This can be seen in a lower variance in prediction error for regression tasks. This can also be seen in a lower variance in accuracy for classification tasks. This lower variance may result in a lower mean performance of the ensemble, which might be desirable given the higher stability or confidence of the model.

Use a voting ensemble if:

-   It results in better performance than any model used in the ensemble.
-   It results in a lower variance than any model used in the ensemble.

A voting ensemble is particularly useful for machine learning models that use a stochastic learning algorithm and result in a different final model each time it is trained on the same dataset. One example is neural networks that are fit using stochastic gradient descent.

For more on this topic, see the tutorial:

- [How to Develop a Weighted Average Ensemble for Deep Learning Neural Networks](https://machinelearningmastery.com/weighted-average-ensemble-for-deep-learning-neural-networks/)

Another particularly useful case for voting ensembles is when combining multiple fits of the same machine learning algorithm with slightly different hyperparameters.

Voting ensembles are most effective when:

- Combining multiple fits of a model trained using stochastic learning algorithms.
- Combining multiple fits of a model with different hyperparameters.

A limitation of the voting ensemble is that it treats all models the same, meaning all models contribute equally to the prediction. This is a problem if some models are good in some situations and poor in others.

An extension to the voting ensemble to address this problem is to use a weighted average or weighted voting of the contributing models. This is sometimes called blending. A further extension is to use a machine learning model to learn when and how much to trust each model when making predictions. This is referred to as stacked generalization, or stacking for short.

Extensions to voting ensembles:

-   Weighted Average Ensemble (blending).
-   Stacked Generalization ([[Stacking]]).

---
Topics :: [[Classifier Combination Strategies]]
Reference :: [[Ensemble methods]]
Type :: #atom
Creator :: Dennis
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-18 09:43
