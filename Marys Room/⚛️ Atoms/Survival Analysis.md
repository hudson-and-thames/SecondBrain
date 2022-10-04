# Survival Analysis


---
Topics ::[[Machine Learning]]
Reference ::  [Jing, B., Zhang, T., Wang, Z., Jin, Y., Liu, K., Qiu, W., Ke, L., Sun, Y., He, C., Hou, D. and Tang, L., 2019. A deep survival analysis method based on ranking. _Artificial intelligence in medicine_, _98_, pp.1-9.](https://www.sciencedirect.com/science/article/pii/S0933365718305992)
Type :: #atom
Creator :: Michelle
Date :: 2022-07-16 18:51


![[survival-analysis.png]]

Survival Analysis is a set of statistical tools, which addresses questions such as ‘how long would it be, before a particular event occurs’; in other words we can also call it as a ‘time to event’ analysis. It is used to estimate the lifespan of a particular population under study. It has been used in various other applications such as predicting churning customers/employees, estimation of the lifetime of a Machine, etc.


### Data
In survival analysis, we do not need the exact starting points and ending points. All the observation do not always start at zero. A subject can enter at any time in the study. 

All the subjects are bought to a common starting point where the time t is zero (t = 0) and all subjects have the survival probabilities equal to one, i.e their chances of not experiencing the event of interest (death, churn, etc) is 100%.


### Survival Function
Survival Function defines the probability that the event of interest has not occurred at time t. It can also be interpreted as the probability of survival after time t.


### Hazard Function
The Hazard Function also called the intensity function, is defined as the probability that the subject will experience an event of interest within a small time interval, provided that the individual has survived until the beginning of that interval.


### Kaplan-Meier Estimate
There are two main methods to estimate the survival curve. The ﬁrst method is a parametric approach. This method assumes a parametric model, which is based on certain distribution such as exponential distribution, then we estimate the parameter, and then finally form the estimator of the survival function. A second approach is a powerful non-parametric method called the Kaplan-Meier estimator.

Kaplan-Meier Estimate is used to measure the fraction of subjects who survived for a certain amount of survival time t under the same circumstances. It is used to give an average view of the population.


### Nelson Aalen Fitter
Like the Kaplan-Meier Fitter, Nelson Aalen Fitter also gives us an average view of the population. It is a non-parametric model.


### Censorship
Not every member of the population will experience the Event of Interest (death, churn, etc) during the study period.

**Right Censoring:** This happens when the subject enters at the start of the study and terminates before the event of interest occurs.

**Left Censoring:** This happens when the event wasn’t observed.

**Interval Censoring:** This happens when the follow-up period, i.e time between observation, is **not continuous**. This can be weekly, monthly, quarterly, etc.

**Left Truncation:** It is referred to as **late entry**.


