# Lower tail depedance as a risk metric

## Key idea

[[Risk Management]] is an essential part of portfolio construction and selection. There are various   risk metrics used by portfolio managers to limit risk in accordance with a specified risk tolerance  range. Common risk measures include alpha, beta, R-squared, standard deviation, and the Sharpe   ratio; which compose the so called five principal risk measures. These give indications of the  risk-return paradigm that portfolio managers use to optimize their return levels given a certain acceptable level of risk. Theses measures are common practice to use in normal market circumstances  but fail to capture some aspects of risk management under extreme events.

A less frequently used risk metric is that of the lower tail dependence, $\chi$. $\chi$ is a risk metric that could be used to describe the comovements between two variables in the far lower tails of their joint distribution. The derivation of $\chi$ comes from the branch of mathematics called [[Extreme Value Theory (EVT)]]. An advantage of $\chi$ is that it can fairly accurately capture the dependence of for example, a stock and the market, at large market downturns that other risk metrics do not necessarily pick up on or consider. $\chi$ can be estimated without needing to specify the underlying joint distribution of the variables in consideration which simplifies assumptions.


## Basic methodology

The Basic methodology for estimating the lower dependence is summarized below:

1. Multiply the returns by negative one and partition the daily returns of the individual stocks and the market index selected into blocks of 22 daily returns. Find the maximum return for each block (greatest loss) and use as the sample maximum for the estimation.
2. Estimate the parameters of the GEV distribution, $\mu, \sigma$, and $\gamma$ by using maximum likelihood on each of the individual stocks and the market index.
3. Transform the sample block maxima of the individual stocks and the market index into a standard Fréchet series by using the estimated parameters from the GEV distrbition. 
4. Specify the logistic family as the relationship of the bivariate sequences of the stocks with market index. Using maixmum likelihood, estimate $\alpha$ and convert it to $\chi$.
5. Rank $\chi$ in ascending order to find the stocks with lowest and highest $\chi$.


The same procedure is done for the portfolios, where the daily returns of the stocks is simply replaced by the daily returns of the portfolio.
Could potentially added to PortfolioLab

Citation::
Type:: #source #academic 
Topics :: [[Risk Management]] [[Extreme Value Theory (EVT)]]
Creator :: Michael
Date :: 2022-07-15 08:40


---
