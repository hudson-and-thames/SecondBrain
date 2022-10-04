# Stacking

**Stacking** is the process of combining various estimators in order to reduce their biases. Predictions from each estimator are stacked together and used as input to a final estimator (usually called a _meta-model_) that computes the final prediction. Training of the final estimator happens via cross-validation. 

Stacking can be done for both regression and classification problems.

![[Ensemble-learning-techniques.webp]]

Stacking can be considered to happen in the following steps:

1. Split the data into a training and validation set,
2. Divide the training set into K folds, for example 10,
3. Train a base model (say SVM) on 9 folds and make predictions on the 10th fold,
4. Repeat until you have a prediction for each fold, 
5. Fit the base model on the whole training set,
6. Use the model to make predictions on the test set,
7. Repeat step 3 – 6 for other base models (for example decision trees),
8. Use predictions from the test set as features to a new model – _the meta-model,_
9. Make final predictions on the test set using the meta model.

With regression problems, the values passed to the meta-model are numeric. With classification problems, they’re probabilities or class labels.


---
Topics ::
Reference ::
Type :: #atom
Creator :: Dennis
TAF ::
Date :: 2022-07-07 16:57
