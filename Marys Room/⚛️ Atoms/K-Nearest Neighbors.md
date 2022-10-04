# K-Nearest Neighbors


---
Topics :: [[Machine Learning]]
Reference :: [Bruce, P., Bruce, A. and Gedeck, P., 2020. _Practical statistics for data scientists: 50+ essential concepts using R and Python_. O'Reilly Media.](https://books.google.co.za/books?hl=en&lr=&id=k2XcDwAAQBAJ&oi=fnd&pg=PP1&dq=Practical+Statistics+for+Data+Scientists&ots=dDLkhkUeBX&sig=-qTlzRa3JlP9tbAVDyIYdw-S1Ck&redir_esc=y#v=onepage&q=Practical%20Statistics%20for%20Data%20Scientists&f=false)
Type :: #atom
Type :: #atom
Creator :: Michelle
TAF :: Michelle
Date :: 2022-07-17 21:07

The idea behind K-Nearest Neighbors (KNN) is very simple.

1. For each record to be classified or predicted: 1. Find K records that have similar features (i.e., similar predictor values). 
2. For classification, find out what the majority class is among those similar records and assign that class to the new record. 
3. For prediction (also called KNN regression), find the average among those similar records, and predict that average for the new record.

![[KNN.png]]

* The prediction results depend on how the features are scaled, how similarity is measured, and how big K is set.
* All predictors must be in numeric form.


### Distance Metrics
* KNN mostly uses Euclidean distance.
* Manhattan distance is anothe rone.
* In measuring distance between two vectors, variables (features) that are measured with comparatively large scale will dominate the measure.


### Choosing K
* The simplest choice is to set K= 1, known as the 1-nearest neighbor classifier.
* Generally speaking, if K is too low, we may be overfitting.
* Higher values of K provide smoothing that reduces the risk of overfitting in the training data.


### KNN as a Feature Engine

1. KNN is run on the data, and for each record, a classification (or quasi-probability of a class) is derived. 
2. That result is added as a new feature to the record, and another classification method is then run on the data. The original predictor variables are thus used twice.

