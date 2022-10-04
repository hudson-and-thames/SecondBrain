# Cross-Validation Leakage

* [[K-Fold Cross-Validation]] fails in time series (finance) because observations cannot be assumed to be drawn from an IID process.
* Leakage takes place when the training set contains information that also appears in the testing set.
	* Serial correlation is a good example.
	* Overlapping data (labelling)
* Leads to False Discoveries!
* [[Purging and Embargoing]] can help to resolve this.

---
Topics:: [[Quantitative Finance]], [[Machine Learning]]
Reference:: [[10 Reasons Most Machine Learning Funds Fail]], [[Advances in Financial Machine Learning]]
Type:: #atom 
Creator :: Jacques
Date:: 2022-06-28 12:36