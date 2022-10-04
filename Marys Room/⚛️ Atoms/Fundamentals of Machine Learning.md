# Fundamentals of Machine Learning
## Summary

Machine Learning (ML) is a form a statistical learning where one tries to extract meaningful conclusions from data by using novice to advanced mathematical and statistical tools. In essence the data to be analysed is feature space $X$ of $p$ input variables, $X = (X_1,X_2,\ldots, X_p)$ , and the aim is try to estimate a function $f$ that captures certain relationships of the feature space. That is we want estimate a function or model model $\hat{f}(X)$ that capture valuable information about the data. 

## Supervised vs Unsupervised

Broadly speaking there are two categories of ML: Supervised and Unsupervised Learning.

*Supervised Learning* is where there is a *target variable,* $Y$, that is related to a $X$ through some function $f$ :

$$ Y = f(X) + \epsilon $$
where $\epsilon$ is the *irreducible error*, since we are never able to catch the exact relationship due to sampling bias or the unmeasurable variation. The *irreducible error* can not be lowered since it can not be predicted by *X*. 

Say we have an estimated function: $$\hat{Y} =\hat{f}(X) $$
where $\hat{Y}$ is the predicted output, and we measure the prediction error through the expected squared difference between $Y$ and $\hat{Y}$:

$$
E[(Y-\hat{Y})^2] = E[(f(X) + \epsilon - \hat{Y})^2] = [f(X) - \hat{f}(X)] + Var(\epsilon)

$$
For each observation of the predictor measurement(s) $x_i , i = 1, . . . , n$ there is an associated response measurement $y_i$ . We wish to fit a model that relates the response to the predictors, with the aim of accurately predicting the response for future observations (prediction) or better understanding the relationship between the response and the predictors (inference). 

*Unsupervised learning* describes the somewhat more challenging situation in which for every observation $i = 1, . . . , n$ we observe
a vector of measurements $x_i$ but no associated response $y_i$. In this setting, we are in some sense working blind; the situation is referred to as unsupervised because we lack a response variable that can supervise our analysis.


## Bias Variance trade-off
The *mean squared error* (MSE) a measure to test the quality of fit for a estimated model. It is defined as

$$
MSE = \frac{1}{n}\sum^n_{i=1}(y_i - \hat{f}(x_i))^2
$$
The MSE can be decomposed into the three terms:
  - Bias
  - Reducible error
  - Irreducible

Variance refers to the amount by which $\hat{f}$ would change if we
estimated it using a different training data set
On the other hand, bias refers to the error that is introduced by approxi-
mating a real-life problem, which may be extremely complicated, by a much
simpler model.

## Regression vs Classification

Variables can be characterised as either quantitative or qualitative (also
known as categorical). Quantitative variables take on numerical values.In contrast, qualitative variables take on values
in one of K different classes, or categories. We tend to refer to problems
with a quantitative response as regression problems, while those involving a qualitative response are often referred to as classification problems.
 
## Prediction vs Inference

There is a trade-off between prediction accuracy and model
interpretability. Sometime this interest only lies in only predicting the model as accurately without carrying too much about *how* the model works. In this case the model treated as a **black box**, where we don't care about how the inner mechanics exactly work but only the accuracy of the final output.

In inference or model interpretability the interested lies in understanding the association between $Y$ and
$X_1 , . . . , X_p$ . In this situation we wish to estimate $f$ , but our goal is not
necessarily to make predictions for $Y$ . Now $\hat{f}$ cannot be treated as a black box. Some general questions relating to inference are:

- Which predictors are associated with the response?
- What is the relationship between the response and each predictor? 
- Can the relationship between Y and each predictor be adequately summarised using a linear equation, or is the relationship more complicated?


## Parameteric vs Unparametric


Parametric modelling is when the functional form of the target model is specified. It reduces the problem of estimating $f$ down to one of estimating a set of parameters. Assuming a parametric form for $f$ simplifies the problem of estimating f because it is generally much easier to estimate a set of parameters.

The potential disadvantage of a parametric approach is that the model we choose will usually not match the true unknown form of $f$ . If the chosen model is too far from the true $f$ , then our estimates will be poor. We can try to address this problem by choosing flexible models that can fit many different possible functional forms
flexible for $f$ . But in general, fitting a more flexible model requires estimating a greater number of parameters. These more complex models can lead to a phenomenon known as overfitting the data, which essentially means they overfitting follow the errors, or noise, too closely.

Non-parametric methods do not make explicit assumptions about the functional form of $f$ . Instead they seek an estimate of f that gets as close to the data points as possible without being too rough or wiggly. Such approaches can have a major advantage over parametric approaches: by avoiding the assumption of a particular functional form for f , they have the potential to accurately fit a wider range of possible shapes for $f$ .  

In contrast, non-parametric approaches completely avoid this danger, since essentially no assumption about the form of f is made. But non-parametric approaches do suffer from a major disadvantage: since they do not reduce the problem of estimating $f$ to a small number of parameters, a very large number of observations (far more than is typically needed for a parametric approach) is required in order to obtain an accurate estimate for f 

Fully parametric  methods make much more efficient use of the information contained in the sample but are sensitive   to the assumed distribution. Non-parametric methods, on the other hand, make few assumptions  
but yield wildly variable estimates as they try to study a region of the empirical distribution that  contains practically no observations


---
Topics :: [[Machine Learning]]
Reference :: [An Inroduction to Statistical Learning in R](https://www.statlearning.com/)
Type :: #atom
Creator :: Michael
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-12 13:59
