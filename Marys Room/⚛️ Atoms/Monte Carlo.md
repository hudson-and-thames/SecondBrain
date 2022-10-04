# Monte Carlo


---
Topics :: [[Machine Learning]]  [[Risk Management]]
Reference ::
Type :: #atom
Creator :: Michelle
TAF :: Michelle
Date :: 2022-07-18 10:15

MCMC methods are used to approximate the posterior distribution of a parameter of interest by random sampling in a probabilistic space.

Markov Chain Monte Carlo(MCMC) methods are math heavy and computationally expensive usually.

In Bayesian statistics, the distribution representing our beliefs about a parameter is called the **_prior distribution_**_,_ because it captures our beliefs _prior_ to seeing any data. 

The **_likelihood distribution_** summarizes what the observed data are telling us, by representing a range of parameter values accompanied by the likelihood that each each parameter explains the data we are observing.

Combining the prior and the likelihood distributions gives the **_posterior distribution._** KInd of like an average of the prior and the likelihood distributions.

![[monte-carlo.png]]


MCMC methods allow us to estimate the shape of a posterior distribution in case we can’t compute it directly.

