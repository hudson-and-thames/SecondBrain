# Hierarchical Clustering
---
Topics :: [[Machine Learning]]
Reference :: [Nielsen, F., 2016. Hierarchical clustering. In _Introduction to HPC with MPI for Data Science_ (pp. 195-211). Springer, Cham.](https://franknielsen.github.io/Clustering/BookChapter-HierarchicalClustering.pdf)
Type :: #atom
Creator :: Michelle
Date :: 2022-07-15 13:46

Hierarchical clustering forms part of unsupervised clustering. 

This clustering technique is divided into two types: Agglomorative and Divisive. Agglomerative clustering takes each data point as an individual cluster. At each iteration, the similar clusters merge with other clusters until one cluster or K clusters are formed. In Divisive clustering all the data points as a single cluster and in each iteration, we separate the data points from the cluster which are not similar. Each data point which is separated is considered as an individual cluster. In the end, we’ll be left with n clusters.

## How does Hierarchical clustering work?

### Distance Matrix
It creates pairwise distances between observations. This distance matrix contains the distance between each pair of observations.

The dissimilarity metric measures the difference between two clusters according to the distances between the cluster members. Calculating the similarity between two clusters is important to merge or divide the clusters. Common dissimilarity metrics are:

- **Complete linkage** is the maximum distance between observations across all pairs of observations in two clusters. As a result, complete linkage tends to generate clusters with similar members.
- **Single linkage** is the minimum distance between observations across all pairs of observations in two clusters. Single linkage can produce clusters that contain disparate elements.
- **Average linkage** is the average distance between observations across all pairs of observations in two clusters. Average linkage compromises between the strengths and weaknesses of the single and complete linkage methods.

### The Dendrogram
* One advantage to hierarchical clustering is the dendrogram, which visualizes the hierarchy of clusters to which each observation belongs. This makes it easier to interpret the clusters.

![[dendogram.png]]



## How does it work for time-series data?
Clustering different time series into similar groups is a challenging because each data point is an ordered sequence.

### Distance metrics
* Correlation distance - Simply take the correlation between each series pair as a distance metric.
* Dynamic time warping - A technique to measure similarity between two temporal sequences that do not align exactly in time, speed, or length.

### Linkage Matrix
Pass a pre-computed distance matrix to dissimilarity routines for agglomerative clustering and plot a dendrogram. Note that the output of these methods is a linkage matrix — not clusters.

### Create Clusters
Convert your linkage matrix into actual cluster assignments — enter the number of clusters _or_ select a cutoff value on the dendrogram.