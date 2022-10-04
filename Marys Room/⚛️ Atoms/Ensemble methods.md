# Ensemble methods
## Key Concept
Ensemble [[Machine Learning]] is a technique that uses several base models together in order to produce one final output or one final model.
These base models are referred to as ensemble members.

### Ensemble Architecture Pillars

There are three main pillars of any ensemble architecture or system 
(Zang 2012):

1. The selection of the training data for each ensemble member.
2. The criteria chosen to select ensemble members to include in the ultimate architecture.
3. The way in which ensemble members are used in combination with each other to produce the final output.

### General settings to use ensemble methods

Ensemble methods can be deployed in one of two general contexts: 
1. Classifier selection - Classifiers are trained on some local region of the entire feature space and regarded as an "expert" in that region. Given new input features,  some distance metric is used to weigh the ensemble members to determine the final classification decision. 
2. Classifier feature -  All ensemble methods are trained over entire feature space selection and the model outputs are weighed according to some scheme. This will reduce the variance of the final model.

Main types of ensemble methods:
* [[Bagging]]
* [[Boosting]]
* [[Stacking]]

```ad-note
There are other types of ensemble methods; these are just the main types as defined by (Zhang, 2012)
```


---
Topics:: [[Machine Learning]]
Reference:: [Zhang, C. and Ma, Y. (2012). Ensemble machine learning: methods and applications. Springer](https://link.springer.com/book/10.1007/978-1-4419-9326-7)
Type:: #atom
Creator :: Michael
Date:: 2022-07-04 15:14
Discussion :: Dennis
Dis_Topic :: Ensemble Methods
Resolved :: No

## Discussion
Michael : Dennis feel free to add anything you want here, as you are also working on ensemble methods


