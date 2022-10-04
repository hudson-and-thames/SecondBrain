# A Study of Cross-Validation and Bootstrap for Accuracy Estimation and Model Selection

Citation::
Type:: #source #academic 
Topics :: [[Model Selection]]
Creator :: Dennis
Date :: 2022-07-07 14:31
Discussion :: Dennis, Michael
Dis_Topic :: Node completion
Resolved :: No 

[[PDF] A Study of Cross-Validation and Bootstrap for Accuracy Estimation and Model Selection | Semantic Scholar](https://www.semanticscholar.org/paper/8c70a0a39a686bf80b76cb1b77f9eef156f6432d)

---
## Key Findings
A review of accuracy estimation methods and comparison of cross-validation and bootstrap. Experimental results on artificial data and theoretical results in restricted settings have shown that for selecting a good classifier from a set of classifiers ([[Model Selection]]), ten-fold cross-validation may be better than the more expensive leave-one-out cross-validation. Report on a large-scale experiment - over half a million runs of C45 and a Naïve-Bayes algorithm - to estimate the effects of different parameters on these algorithms on real-world datasets. For cross-validation, vary the number of folds and whether the folds are stratified or not; for bootstrap, vary the number of bootstrap samples. Results indicate that for real-world datasets, the best method to use for model selection is **10-fold stratified cross validation**, even if computation power allows using more folds.

# Discussion
Michael: Hey Dennis, its fine to add nodes that you want to complete in the future, but rather consider making them particles or adding it to the to-do list. Additionally you could tag yourself to remember to complete it.
Dennis: Hey Michael, thanks for the reminder. I added a bit of context.
