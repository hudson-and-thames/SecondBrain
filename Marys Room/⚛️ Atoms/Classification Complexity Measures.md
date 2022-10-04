# Classification Complexity Measures
Estimate the level of difficulty of a classification problem:
- use low correlated measures which are supported by different concepts
- low Pearson correlation among measures suggest complementary benefit

Categories of complexity measures:
(a) classes overlapping
(b) classes separability
(c) classes geometry, topology and density

Selected measures for each category:
1. Fisher's Discriminant Ration *F1* (a)
	measures how separable two classes are considering a particular feature
2. Ratio of intra/inter class nearest neighbor distance *N2* (b)
	estimates the separability of two classes taking into account an analyse of the border between them
3. Nonlinearity of the one-nearest neighbor classifier *N4* (c)
	error rate of the 1*NN* classifier on a test set created by the linear interpolation between randomly drawn pairs of samples from the same class
---
Topics :: [[Machine Learning]]
Reference :: [[Dynamic Ensemble Selection]]
Type :: #atom
Creator :: Dennis
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-15 11:39
