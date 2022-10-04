# Optimal threshold for maximizing 

## Background
The F1-score classification metric is defined as the harmonic mean of precision and recall:

$$
F1 = 2*(\frac{Presicion * Recall}{Presicion + Recall})
$$
The F1-score is used as a statistical measure to rate performance of a classifier. Further more, when the threshold or cutoff chosen to make a certain classification is adjusted, the recall and precision is also adjusted. One is often interested in determining the optimal threshold to maximize the F1-score. 

## Key Result

Well this is in fact quite easy and it turns out that the optimal threshold is exactly half that of the of the maximum F1-score!
This results is presented by Lipton, Elkan and  Naryanaswamy (2014)
in their paper [Optimal Thresholding of Classifiers to Maximize F1 Measure](https://link.springer.com/chapter/10.1007/978-3-662-44851-9_15)

For code an a quick explanation of the math see the following [article](https://hippocampus-garden.com/f1/)[]

---
Topics :: [[Machine Learning]]
Reference :: [Optimal Thresholding of Classifiers to Maximize F1 Measure](https://link.springer.com/chapter/10.1007/978-3-662-44851-9_15)
Type :: #atom
Creator :: Michael
TAF :: 
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-14 13:39
