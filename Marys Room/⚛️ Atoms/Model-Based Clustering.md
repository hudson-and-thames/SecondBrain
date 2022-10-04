# Model-Based Clustering


---
Topics :: [[Machine Learning]]
Reference :: [Bruce, P., Bruce, A. and Gedeck, P., 2020. _Practical statistics for data scientists: 50+ essential concepts using R and Python_. O'Reilly Media.](https://books.google.co.za/books?hl=en&lr=&id=k2XcDwAAQBAJ&oi=fnd&pg=PP1&dq=Practical+Statistics+for+Data+Scientists&ots=dDLkhkUeBX&sig=-qTlzRa3JlP9tbAVDyIYdw-S1Ck&redir_esc=y#v=onepage&q=Practical%20Statistics%20for%20Data%20Scientists&f=false)
Type :: #atom
Creator :: Michelle
TAF :: Michelle
Date :: 2022-07-17 21:30

The most widely used model-based clustering methods rest on the multivariate nor‐ mal distribution.

### Multivariate Normal Distribution

* The covariance matrix is a measure of how the variables correlate with each other.
* This is a symbolic way of saying that the variables are all normally distributed, and the overall distribution is fully described by the vector of variable means and the covariance matrix.

### Mixtures of Normals
* Each record is assumed to be distributed as one of K multivariate normal distributions.
* Each normal distribution represents a cluster.

![[model-based-clustering-graph.png]]


### Selecting the Number of Clusters
* Chooses the number of clusters for which the Bayesian Information Criteria (BIC) has the largest value.
* BIC works by selecting the best-fitting model with a penalty for the number of parameters in the model.
* Adding more clusters will always improve the fit at the expense of introducing additional parameters in the model.