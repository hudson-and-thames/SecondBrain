# Principle Component Analysis(PCA)


---
Topics :: [[Machine Learning]] [[Time-Series]]
Reference :: [Shlens, J., 2014. A tutorial on principal component analysis. _arXiv preprint arXiv:1404.1100_.](https://arxiv.org/pdf/1404.1100.pdf)
Type :: #atom
Creator :: Michelle
Date :: 2022-07-15 13:03


Principal component analysis is a technique that forms part of feature extraction. It combines our input variables in a specific way, then we can drop the “least important” variables while still retaining the most valuable parts of all of the variables. 

#### When is PCA applicable?
1.  Difficult to identify variables to completely remove from consideration.
2.  Want variables to not be colinnear.
3.  You can afford to loose interpretability of your target variable.

#### How does PCA work?
The direction of the data presented is can go on the green and red direction but the red direction is more important. By transforming the data to fit the directions to the x-axes and y-axes it is again clear that the red direction is more important. The original data transformed so that our axes are now the principal components. The Principal components are perpendicular to one another. Because our principal components are orthogonal to one another, they are statistically linearly independent of one another.

![[pca.png]]


