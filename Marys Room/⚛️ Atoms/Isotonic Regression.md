# Isotonic Regression
By Zadrozny and Elkan (2002; 2001).

Isotonic means: monotonically increasing. Thus basic assumption: $$y_i = m(f_i) + \epsilon_i$$A [[Probability Calibration]] method that can correct any monotonic distortion. However is more prone to overfitting and performs worse than [[Platt Scaling]], when there are only a few data points (better fit for larger data sets). 


### Tips
* Need > 1000 data points in calibration set (see source).
* Suggested to fit on data that primary was not trained on, as this introduces a bias (fact check this in Plat 1999).


### References
Zadrozny, B., & Elkan, C. (2001). Obtaining calibrated probability estimates from decision trees and naive bayesian classifiers. ICML (pp. 609–616).

Zadrozny, B., & Elkan, C. (2002). Transforming classi- fier scores into accurate multiclass probability estimates. KDD (pp. 694–699).

---
Topics :: [[Probability Calibration]]
Reference :: Zadrozny and Elkan (2002; 2001).
Type :: #atom
Creator :: Jacques
TAF ::
Date :: 2022-07-07 17:17