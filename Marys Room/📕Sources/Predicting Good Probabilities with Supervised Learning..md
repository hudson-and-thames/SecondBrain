Citation: [Niculescu-Mizil, Alexandru, and Rich Caruana. "Predicting good probabilities with supervised learning." In _Proceedings of the 22nd international conference on Machine learning_, pp. 625-632. 2005.](https://dl.acm.org/doi/pdf/10.1145/1102351.1102430?casa_token=HcaR2WQsYUgAAAAA:SWAQ8czp0K7u-loksCqeWddNNLPCSc-oLQ32Hc50aE2NtAEOwogRXcfB6Q-0bAeMoDDNKcjRHnds)
Type: #source #academic 
Creator :: Jacques
Topics: [[Probability Calibration]]
Date: 2022-07-07 11:09


---

Paper describes different models and their calibration curves. It looks into the relationship between model output and true posterior probabilities.

The output of a classification model is not actually a frequentist probability but rather a Bayesian probability, i.e., that its more of a model confidence that a freq probability.

The model output can be transformed into a more frequentist interpretation by using  [[Platt Scaling]] and [[Isotonic Regression]]. This process is known as [[Probability Calibration]] (binary classification setting).

Analyses 10 models:
* Sigmoid-shaped distortion (Use Platt):
	* Typical of maximum margin methods:
		* SVM
		* Boosted trees
		* Boosted stumps
* Opposite bias 0 and 1
	* Naive bayes
* Very little Bias:
	* NN
	* Logistic regression
	* Bagged trees
* Unclassified
	* Decision tree
	* Memory-based learning
	* Random forests
 
### Concepts
* Different models have different shapes and depending on the shape, you need to apply a specific type of calibration.
* Model Calibration can be visualized with reliability diagrams (DeGroot & Fienberg, 1982). These are CalibrationCurves from sklearn.

### Great points
* "Maximum margin methods such as boosted trees and boosted stumps push probability mass away from 0 and 1 yielding a characteristic sigmoid shaped distortion in the predicted probabilities."
* "Methods such as bagging and random forests that average predictions from a base set of models can have difficulty making predictions near 0 and 1 because variance in the underlying base models will bias predictions that should be near zero or one away from these values"
* "Models such as Naive Bayes, which make unrealistic independence assumptions, push probabilities toward 0 and 1."
* "Other models such as neural nets and bagged trees do not have these biases and predict well calibrated probabilities."
* "boosted trees, random forests, and SVMs predict the best probabilities"


Exhibit 1: Typical Model Output Distributions
![[ModelOutputDistributions.png]]

## References
[Niculescu-Mizil, Alexandru, and Rich Caruana. "Predicting good probabilities with supervised learning." In _Proceedings of the 22nd international conference on Machine learning_, pp. 625-632. 2005.](https://dl.acm.org/doi/pdf/10.1145/1102351.1102430?casa_token=HcaR2WQsYUgAAAAA:SWAQ8czp0K7u-loksCqeWddNNLPCSc-oLQ32Hc50aE2NtAEOwogRXcfB6Q-0bAeMoDDNKcjRHnds)

DeGroot, M., & Fienberg, S. (1982). The comparison and evaluation of forecasters. Statistician, 32, 12–22.
