# Extreme Value Theory (EVT)

The main idea behind EVT is to model the probabilistic behavior of unusually large or small  observations. The theorems and results derived in EVT are of an asymptotic nature and  can be seen as approximately true for a large sample size given the right circumstances.

There are two main approach when an extreme value analysis is applied to a data set:  
1. Block maxima: This approach involves dividing the data into different blocks and subsequently taking the maxima of each of the blocks as a new sequence of random variables that  could be modeled through the results obtained by the Fischer-Tippett theorem.  
2. Peaks over threshold (POT): This approach aims to model the conditional distribution of  
exceedances over a a specified threshold. The Pickands Balkema de Haan theorem gives that the limiting result is a generalized Pareto distribution (GPD).  
These two approaches aim to answer the same question : “How does the far tail of the distribution of the data behave?”.

A major advantage of EVT is that the underlying distribution of the data does not have to to specified.

**Fischer Tippet Theorem**:

Let $X_{1}, X_{2}, \ldots, X_{n}$ be weakly dependent, identically distributed, random variables and define $M_{n,n}\equiv \max \left\{X_{1}, \ldots, X_{n}\right\}$, i.e the maximum of sample size n.  If there exist sequences of constants $\left\{a_{n}>0\right\},\left\{b_{n}\right\}$ such that $\left(M_{n}-b_{n}\right) / a_{n}$ has a proper limit distribution, then that distribution is of the form following form:
$$
G_{\gamma}(z)=\exp \left\{-\left[1+\gamma\left(\frac{z-\mu}{\sigma}\right)\right]^{-1 / \gamma}\right\}
$$


where $1+\gamma(z-\mu) / \sigma>0$,  $-\infty<\mu<$ $\infty, \sigma>0$ and $-\infty<\gamma<\infty$.

---
Topics :: [[Statistics]]
Reference ::
Type :: #atom
Creator :: Michael
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-15 08:31
