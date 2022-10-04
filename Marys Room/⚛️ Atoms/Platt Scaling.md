# Platt Scaling
A [[Probability Calibration]] method, originally for transforming SVM outputs to posterior probability (Platt, 1999). 

Most effective when the calibration curve has a sigmoid-shape and small data set.

Exhibit 1: Sigmoid Shape
![[Sigmoidal Calibration Curve.png]]

Does transformation by passing model output through a sigmoid function.
$$P(y=1|f) = \frac{1}{1+exp(Af + B)}$$
Models that suffer from sigmoid shape distortions: 
* SVM
* Boosted trees
* Boosted stumps

### Tips
* Not good for Naive Bayes model -> use [[Isotonic Regression]].
* Suggested to fit on data that primary was not trained on, as this introduces a bias (fact check this in Plat 1999).
* Platt scaling has difficulty fitting the predictions in the tails of models that are well-calibrated (Logistic, NNs, Bagged Trees) (See Source)
* [Sklearn has an implementation](https://scikit-learn.org/stable/modules/calibration.html)

### References
* [Probabilistic outputs for support vector machines and comparisons to regularized likelihood methods, 1999](https://www.researchgate.net/file.PostFileLoader.html?id=540479d7d11b8bb1588b459d&assetKey=AS%3A273601008209920%401442242971560)*

---
Topics :: [[Probability Calibration]]
Reference :: 
Type :: #atom
Creator :: Jacques
TAF ::
Date :: 2022-07-07 11:54