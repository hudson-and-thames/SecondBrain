# Ensemble Pruning and Growing
[[Voting]] and [[Stacking]] ensembles typically combine the predictions from a heterogeneous group of model types.

Although the ensemble may have a large number of ensemble members, it is hard to know that the best combination of members is being used by the ensemble. For example, instead of simply using all members, it is possible that better results could be achieved by adding one more different model type or removing one or more models.

This can be addressed using a weighted average ensemble and using an optimization algorithm to find an appropriate weighting for each member, allowing some members to have a zero weight, which effectively removes them from the ensemble. The problem with a weighted average ensemble is that all models remain part of the ensemble, perhaps requiring an ensemble of greater complexity than is required to be developed and maintained.

An alternative approach is to optimize the composition of the ensemble itself. The general approach of automatically choosing or optimizing the members of ensembles is referred to as ensemble selection.

Two common approaches include ensemble growing and ensemble pruning.

- **Ensemble Growing**: Add members to the ensemble until no further improvement is observed.
- **Ensemble Pruning**: Remove members from the ensemble until no further improvement is observed.

**Ensemble growing** is a technique where the model starts with no members and involves adding new members until no further improvement is observed. This could be performed in a greedy manner where members are added one at a time only if they result in an improvement in model performance.

**Ensemble pruning** is a technique where the model starts with all possible members that are being considered and removes members from the ensemble until no further improvement is observed. This could be performed in a greedy manner where members are removed one at a time and only if their removal results in a lift in the performance of the overall ensemble.

> Given a set of trained individual learners, rather than combining all of them, ensemble pruning tries to select a subset of individual learners to comprise the ensemble.

— Page 119, [Ensemble Methods: Foundations and Algorithms](https://amzn.to/2TavTcy), 2012.

An advantage of ensemble pruning and growing is that it may result in an ensemble with a smaller size (lower complexity) and/or an ensemble with better predictive performance. Sometimes a small drop in performance is desirable if it can be achieved in a large drop in model complexity and resulting maintenance burden. Alternately, on some projects, predictive skill is more important than all other concerns, and ensemble selection provides one more strategy to try and get the most out of the contributing models.

> There are two main reasons for reducing the ensemble size: a) Reducing computational overhead: Smaller ensembles require less computational overhead and b) Improving Accuracy: Some members in the ensemble may reduce the predictive performance of the whole.

— Page 119, [Pattern Classification Using Ensemble Methods](https://amzn.to/2zxc0F7), 2010.

Ensemble growing might be preferred for computational efficiency reasons in cases where a small number of ensemble members are expected to perform better, whereas ensemble pruning would be more efficient in cases where a large number of ensemble members may be expected to perform better.

Simple greedy ensemble growing and pruning have a lot in common with stepwise feature selection techniques, such as those used in regression (e.g. so-called stepwise regression).

More sophisticated techniques may be used, such as selecting members for addition to or removal from the ensemble based on their standalone performance on the dataset, or even through the use of a global search procedure that attempts to find a combination of ensemble members that results in the best overall performance.

> … one can perform a heuristic search in the space of the possible different ensemble subsets while evaluating the collective merit of a candidate subset.

— Page 123, [Pattern Classification Using Ensemble Methods](https://amzn.to/2zxc0F7), 2010.


---
Topics :: [[Ensemble methods]]
Reference ::
Type :: #atom
Creator :: Dennis
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-18 11:59
