# K-Means Clustering


---
Topics :: [[Machine Learning]]
Reference :: [Bruce, P., Bruce, A. and Gedeck, P., 2020. _Practical statistics for data scientists: 50+ essential concepts using R and Python_. O'Reilly Media.](https://books.google.co.za/books?hl=en&lr=&id=k2XcDwAAQBAJ&oi=fnd&pg=PP1&dq=Practical+Statistics+for+Data+Scientists&ots=dDLkhkUeBX&sig=-qTlzRa3JlP9tbAVDyIYdw-S1Ck&redir_esc=y#v=onepage&q=Practical%20Statistics%20for%20Data%20Scientists&f=false)
Type :: #atom
Creator :: Michelle
TAF :: Michelle
Date :: 2022-07-17 21:19

K-means was the first clustering method to be developed.

![[k-means-clustering.png]]

* K-means divides the data into K clusters by minimizing the sum of the squared dis‐ tances of each record to the mean of its assigned cluster. 
* This is referred to as the within-cluster sum of squares or within-cluster SS. 
* K-means does not ensure the clusters will have the same size but finds the clusters that are the best separated.
* In clustering records with multiple variables (the typical case), the term cluster mean refers not to a single number but to the vector of means of the variables.
* K-means finds the assignment of records that minimizes within-cluster sum of squares across all clusters.
* K-means algorithm uses randomized starting points.
* K-means will assign records to clusters, even if those clusters are not well separated.

![[k-means-graph.png]]


The algorithm starts with a user-specified K and an initial set of cluster means and then iterates the following steps: 

1. Assign each record to the nearest cluster mean as measured by squared distance. 
2. Compute the new cluster means based on the assignment of records.

The algorithm converges when the assignment of records to clusters does not change.


### Interpreting the Clusters
* Interpreting the Clusters and tyhe sized of the clusters.
* Imbalanced clusters can result from distant outliers, or from groups of records very distinct from the rest of the data—both may warrant further inspection.


### Selecting the Number of Clusters
* The K-means algorithm requires that you specify the number of clusters.
* Elbow method is used to identify when the set of clusters explains “most” of the variance in the data.