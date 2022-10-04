# Data Fusion

A common problem is to combine multiple heterogeneous data from different sources, to forecast something. 

Lets say you are forecasting gas prices and you have normal time series data and image data. The images are 250 x 250 pixels and a CNN can be trained on those with a random forest on the time series data. The model forecasts can then be combined and passed as input to another model. 

In this way, multiple heterogeneous data can be used.

This is a form of [[Ensemble]] systems.

A detailed study is here: D. Parikh and R. Polikar, “An ensemble-based incremental learning approach to data fusion,” IEEE Transactions on Systems, Man, and Cybernetics, Part B: Cybernetics, vol. 37, no. 2, pp. 437–450, 2007

---
Topics :: [[Machine Learning]]
Reference :: [Zhang, C. and Ma, Y. (2012). Ensemble machine learning: methods and applications. Springer, pg 21](https://link.springer.com/book/10.1007/978-1-4419-9326-7)
Type :: #atom
Creator :: Jacques
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-10 17:12
