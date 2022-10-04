# Modeling for False Positives

Modeling for False Positives is the 2nd of [[3 Sources of Advantage (MLA)]] in [[Meta-Labeling]].

Useful features for identifying false positives can be split into two groups: model evaluation statistics and market state statistics. The former focus on measuring the health of the primary model’s recent performance. Relevant concepts include rolling accuracy, F1, recall, precision, and AUC scores. It is also possible to measure for structural breaks in the error terms, apply a Kalman filter to the log loss, and evaluate the acceleration of various statistics. If the primary model is also an ML algorithm, then the model output can be added as a measure of the model’s confidence.

Market state statistics, on the other hand, reflect that the primary model is likely to perform differently in various market regimes. A toy example is the trend-following strategy of crossing moving averages. These are known to suffer when volatility increases and markets stop trending, leading to many false signals (whipsaws) and a loss in profits. The secondary model could identify that an increase in volatility and a lack of autocorrelation may be a poor environment. Gu, Kelly, and Xiu (2020) found that the most successful predictors are price trends, liquidity, and volatility; we recommend starting with those. 

A market state can also be represented by the four moments of distribution: mean, variance, skew, and kurtosis, as well as momentum and acceleration. We also recommend testing market regime statistics by employing, for example, structural break tests (Phillips, Shi, and Yu 2015), change point detection (Aminikhanghahi and Cook 2017), and directional change and regime tracking frameworks (Chen and Tsang 2020).

López de Prado and Fabozzi (2020) noted that macroeconomic variables are also useful for regime detection

---
Topics :: [[Risk Management]], Machine Learning
Reference ::
Type :: #molecule #novel 
Creator :: Jacques
Rating :: 8
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-09 19:44
