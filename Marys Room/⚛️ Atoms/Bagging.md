# Bagging

**Bagging** takes random samples of data, builds learning algorithms, and uses the mean to find bagging probabilities. It’s also called _bootstrap aggregating_. Bagging aggregates the results from several models in order to obtain a generalized result. 

The method involves:

-   Creating multiple subsets from the original dataset with replacement,
-   Building a base model for each of the subsets,
-   Running all the models in parallel,
-   Combining predictions from all models to obtain final predictions.


---
Topics :: [[Ensemble]]
Reference ::
Type :: #atom
Creator :: Dennis
TAF ::
Date :: 2022-07-07 16:58
