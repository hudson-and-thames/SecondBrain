# Boosting
**Boosting** is a machine learning ensemble technique that reduces bias and variance by converting weak learners into strong learners. The weak learners are applied to the dataset in a sequential manner. The first step is building an initial model and fitting it into the training set. 

A second model that tries to fix the errors generated by the first model is then fitted. Here’s what the entire process looks like:

- Create a subset from the original data,
- Build an initial model with this data,
- Run predictions on the whole data set,
- Calculate the error using the predictions and the actual values,
- Assign more weight to the incorrect predictions,
- Create another model that attempts to fix errors from the last model,
- Run predictions on the entire dataset with the new model,
- Create several models with each model aiming at correcting the errors generated by the previous one,
- Obtain the final model by weighting the mean of all the models.

---
Topics :: [[Ensemble]]
Reference ::
Type :: #atom
Creator :: Dennis
TAF ::
Date :: 2022-07-07 16:58