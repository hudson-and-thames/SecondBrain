# Ensemble Clustering

## The similarity matrix
Unlike supervised approaches, where the ensemble can be done straightforwardly by stacking learners above others, clustering is not so simple.

In clustering, the final label of the data has no meaning alone, does not matter if a point is in cluster 1 or 2, what matters is who is also in this cluster with it. So, joining the information of two different clustering results is not as simple as comparing if the final labels are the same, as in classification. Some way to compute how much agreement exists on the different partitions is required.

The similarity Matrix is a simple way to translate this information into a data structure. It is built as follows:

Considering that we have _n_ points on our dataset, the similarity matrix will be a _n_ x _n_ matrix, where the position (_i,j)_ contains how many times the points i and j have fallen in the same cluster. The following image shows an example of this matrix.

![](https://miro.medium.com/max/1400/1*9FYX8ZjaPwIuwWSxba--ZA.png)

Example of **Similarity Matrix**.

A better way to represent this information is using percentages instead of solid counts. In this normalized form, each position (_i,j_) represents the probability of i and j falling together in the same cluster. This normalization is obtained by dividing each row by its diagonal value (total count).

![](https://miro.medium.com/max/1400/1*TKTstvx07yzcoy10Ehs5iw.png)

Example of **Normalized Similarity Matrix**.

This approach is better for machine learning, as all the values fall in the range [0,1]. The normalized similarity matrix will be our basic building block for the following sections.

## Ensemble with Graph connected components

This approach considers that two points that appear together (in the same cluster) more than X% of the time (for example, 10% or 50%) should be in the same final cluster.

If we consider the similarity matrix as a graph, where each point is a node and the edge from (i,j) has a weight equal to the value of (i,j) in the matrix, what this approach essentially makes is removing the edges that have values below our threshold (X%), disconnecting the nodes. The node groups that remained connected are our final clusters. This is why this approach is called “connected components”.

![](https://miro.medium.com/max/1400/1*iPDooHJ5KESti3sNn6nxcw.png)

Removing edges from the graph.

As it creates new clusters based on a simple threshold, it can be considered equivalent to simple bagging ensemble methods for supervised models.

---
Topics :: [[Ensemble methods]]
Reference ::
Type :: #atom
Creator :: Dennis
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-18 12:16
