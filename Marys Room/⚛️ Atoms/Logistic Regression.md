# Logistic Regression


---
Topics :: [[Machine Learning]]
Reference ::  [Bruce, P., Bruce, A. and Gedeck, P., 2020. _Practical statistics for data scientists: 50+ essential concepts using R and Python_. O'Reilly Media.](https://books.google.co.za/books?hl=en&lr=&id=k2XcDwAAQBAJ&oi=fnd&pg=PP1&dq=Practical+Statistics+for+Data+Scientists&ots=dDLkhkUeBX&sig=-qTlzRa3JlP9tbAVDyIYdw-S1Ck&redir_esc=y#v=onepage&q=Practical%20Statistics%20for%20Data%20Scientists&f=false)
Type :: #atom
Creator :: Michelle
TAF :: Michelle
Date :: 2022-07-17 20:56


Logistic regression is a structured model approach rather than a data-centric approach.

![[logistic-regression.png]]

## Logistic Response Function and Logit
Normally we have:

![[linear-function.png]]

Apply the inverse logit to the predictors:

![[inverse-logit.png]]

This transform ensures that the p stays between 0 and 1. To get the exponential expression out of the denominator, we consider odds instead of probabilities. Odds, familiar to bettors everywhere, are the ratio of “successes” (1) to “nonsuccesses” (0). In terms of probabilities, odds are the probability of an event divided by the probability that the event will not occur. For example, if the probability that a horse will win is 0.5, the probability of “won’t win” is (1 – 0.5) = 0.5, and the odds are 1.0:

![[odds.png]]

We can obtain the probability from the odds using the inverse odds function:

![[probability.png]]

We combine this with the logistic response function, shown earlier, to get:

![[odds-success.png]]

Finally, taking the logarithm of both sides, we get an expression that involves a linear function of the predictors:

![[log-odds.png]]

