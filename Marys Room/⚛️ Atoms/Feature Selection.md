# Feature Selection

The process of finding and selecting the most useful features in a dataset. Having irrelevant features in your data can decrease the accuracy of the models, make the model learn based on irrelevant features, decrease model interpretability, and decrease training speed.

## Benefits of performing feature selection :
* **Reduces Overfitting**: Less redundant data means less opportunity to make decisions based on noise.
* **Improves Accuracy**: Less misleading data means modelling accuracy improves.
* **Reduces Training Time**: fewer data points reduce algorithm complexity and algorithms train faster.

![[cures-of-dim.png]]
 
## Feature Selection Methods:
Broad categories exist for feature selection:
- **Filter based:** We specify some metric and based on that filter features. An example of such a metric could be correlation/chi-square.
- **Wrapper-based:** Wrapper methods consider the selection of a set of features as a search problem. Example: Recursive Feature Elimination.
- **Embedded:** Embedded methods use algorithms that have built-in feature selection methods. For instance, Lasso and [[Random Forests]] have their own feature selection methods.

## Filter-based methods:
### Univariate Selection
Statistical tests are used to select those features that have the strongest relationship with the output variable.

### Feature Importance
You can get the feature importance of each feature of your dataset by using the feature importance property of the model. Feature importance gives you a score for each feature of your data, the higher the score more important or relevant is the feature towards your output variable.

There are several [[Feature Importance Algorithms]]. Some examples include:
* Model Fingerprint
* Clustered MDA and MDI
* Shapley Values

### Chi-Squared
In this method, we calculate the chi-square metric between the target and the numerical variable and only select the variable with the maximum chi-squared values.

![[Chi-squared.png]]

## Wrapper-based methods:
### Recursive Feature Elimination
The goal of recursive feature elimination (RFE) is to select features by recursively considering smaller and smaller sets of features.

## Embedded-based methods:
### Lasso
![[Lasso.png]]

---
Topics :: [[Machine Learning]]
Reference ::  [Dokeroglu, T., Deniz, A. and Kiziloz, H.E., 2022. A Comprehensive Survey on Recent Metaheuristics for Feature Selection. _Neurocomputing_.](https://www.sciencedirect.com/science/article/abs/pii/S092523122200474X)
Type :: #source 
Creator :: Michelle
Date :: 2022-07-16 17:11


