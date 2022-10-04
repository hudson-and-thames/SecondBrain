# Probability Calibration

The process of **Mapping model predictions to posterior probabilities** - i.e., model output -> frequentist probability.

Some techniques include [[Platt Scaling]] and [[Isotonic Regression]], and calibration curves are used guide the process.

Sklearn provides an [implementation](https://scikit-learn.org/stable/modules/calibration.html). If the model is well calibrated then the points fall on the diagonal line.

![[CalibrationCurves Sklearn.png]]

---
Topics :: [[Machine Learning]]
Reference ::
Type :: #atom
Creator :: Jacques
TAF ::
Date :: 2022-07-07 17:24