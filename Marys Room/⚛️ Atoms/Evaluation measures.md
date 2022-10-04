# Evaluation measures

---
Topics :: [[Machine Learning]]
Reference :: [Steyerberg, E.W., Van Calster, B. and Pencina, M.J., 2011. Performance measures for prediction models and markers: evaluation of predictions and classifications. _Revista Española de Cardiología (English Edition)_, _64_(9), pp.788-794.](https://www.sciencedirect.com/science/article/abs/pii/S1885585711003604)
Type :: #atom
Creator :: Michelle
Date :: 2022-07-16 20:26

After solving machine learning problems, we need to measure the performance of the model and for that purpose there are 6 measures:

### Confusion matrix
![[Confusion-matrix.png]]

It consists of a summary of the prediction results of a classification problem. The  
number of correct and incorrect predictions are summarized. The confusion matrix shows the ways in which your classification model is confused when it makes a prediction.

Definition of the Terms :

**Positive (P)** : An observation is positive (for example: is an orange).  
**Negative (N)** : An observation is not positive (for example: is not an orange).

**True Positive (TP)** : An observation is positive and is predicted positive.  
**False Negative (FN)** : An observation is positive, but is predicted negative.  
**True Negative (TN)** : An observation is negative, and is predicted negative.  
**False Positive (FP)** : An observation is negative, but is predicted positive.

### Accuracy
Accuracy is simply a ratio of the correctly predicted observations to the total  number of
observations. Accuracy is a great measure but only when dataset is symmetric where the values of false positive and false negatives are almost the same.

![[accuracy.png]]


### Recall
Recall is defined as the ratio of the total number of correctly classified positive examples divided by the total number of positive examples.

![[recall.png]]


### Precision
To get the value of precision we divide the total number of correctly classified positive examples by the total number of predicted positive examples. High Precision indicates an example labeled as positive is indeed positive (small number of FP).


### F1-Score
We calculate an F-measure which uses Harmonic Mean in place of Arithmetic Mean as it punishes the extreme values more.

![[f1-score.png]]


### Decision Boundary Plot
The Decision Boundary separates the data-points into regions, which are  
actually the classes in which they belong.

![[decision-boundry-plot.png]]
