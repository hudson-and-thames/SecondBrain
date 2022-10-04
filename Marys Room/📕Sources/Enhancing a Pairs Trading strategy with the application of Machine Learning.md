# Enhancing a Pairs Trading strategy with the application of Machine Learning  


Citation:: [Sarmento, S.M. and Horta, N., 2020. Enhancing a pairs trading strategy with the application of machine learning. _Expert Systems with Applications_, _158_, p.113490.](http://premio-vidigal.inesc.pt/pdf/SimaoSarmentoMSc-resumo.pdf)
Type:: #source #academic 
Topics :: [[Machine Learning]]
Creator :: Michelle
Date :: 2022-07-15 11:31

---
Pairs trading is a relative value investment strategy which trades related assets by using statistical arbitrage. The basic idea behind pairs trading is that assets are in a long-run equilibrium. When these assets deviate from this equilibrium in the short term, a profit can be made by shorting one asset and buying the other asset and spread between will converge. In essence it is based on the notation that cointegrated pairs are mean reverting.

The proposed framework to select these assets is given in following three steps:

1.  Dimensionality reduction
2.  Unsupervised Learning clustering
3.  Pairs selection criteria

### Concepts

* DImensionality reduction
	* A high dimensional time series data set leads to the curse of dimensionality, which is a phenomenom that appears when analyzing data in high dimensions which causes problems for statistical analyses. We therefore need a technique to represent the data in a more compact way. A technique commonly used to achieve this [[Principle Component Analysis]].

* Unsupervised Learning
	* Now that we have a compact representation of that data we can use unsupervised learning techniques to cluster the data. The proposed technique for this is the Ordering points to identify the clustering structure(OPTICS) algorithm. This a algorithm for finding density-based clusters in spatial data. The basic idea is that the algorithm orders based on reachability distance of the sample points while expanding the clusters at the same time. The output of the OPTICS algorithm is therefore an ordered list of reachability distances, which by means of thresholds or different techniques we can split into clusters.
	* The algorithm takes two arguments:
		-  The maximum distance between two samples for one to be consider in the neighborhood of the other.
		- The minimum number of points to form a cluster.


![[OPTICS-clustering.png]]

* Pairs selection Criteria

	The framework proposes using the following four conditions to check for suitable pairs.
	 * Cointergration: Cointegration tests identify scenarios where two or more non-stationary time series are integrated together in a way that they cannot deviate from equilibrium in the long term. The tests are used to identify the degree of sensitivity of two variables to the same average price over a specified period of time.
	* Hurst exponent test: The Hurst exponent is a measure of long-term memory of time series. Used to check if is a series is mean-reverting (<0.5),  random walk (=0.5) or treding (>5). In our case we shoud specify the hurst threshold as lower than 0.5 so that it is mean reverting.
	* Half life: The half-life measures how long it would take a time series to revert back to half it’s initial deviation away from the mean. we can specify a maxium value so that the spread does not take to long to converge, and a minimum value so that the spread does not converge to quickly. We can specify for example 250 so that is reverts at least yearly.
	* Spread crossings: Measure to test how many times the spread is crossed (across zero) for the testing period. We want a least a minium number of times that the spread crosses zero in order for us to trade the pairs. Say we want the spread to cross at least quartlery then we can specify this parameter as 4*(years of data)



### References
[Sarmento, S.M. and Horta, N., 2020. Enhancing a pairs trading strategy with the application of machine learning. _Expert Systems with Applications_, _158_, p.113490.](http://premio-vidigal.inesc.pt/pdf/SimaoSarmentoMSc-resumo.pdf)