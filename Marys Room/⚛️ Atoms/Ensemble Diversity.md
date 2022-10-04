# Ensemble Diversity
Ensemble diversity refers to differences in the decisions or predictions made by the ensemble members.

> Ensemble diversity, that is, the difference among the individual learners, is a fundamental issue in ensemble methods.

— Page 99, [Ensemble Methods](https://amzn.to/2XZzrjG), 2012.

Two ensemble members that make identical predictions are considered not diverse.

Ensembles that make completely different predictions in all cases are maximally diverse, although this is most unlikely.

> Making different errors on any given sample is of paramount importance in ensemble-based systems. After all, if all ensemble members provide the same output, there is nothing to be gained from their combination.

— Page 5, [Ensemble Machine Learning](https://amzn.to/2C7syo5), 2012.

Therefore, some level of diversity in predictions is desired or even required in order to construct a good ensemble. This is often simplified in discussion to the desire for diverse ensemble members, e.g. the models themselves, that in turn will produce diverse predictions, although diversity in predictions is truly what we seek.

Ideally, diversity would mean that the predictions made by each ensemble member are independent and uncorrelated.

> … classifier outputs should be independent or preferably negatively correlated.

— Page 5, [Ensemble Machine Learning](https://amzn.to/2C7syo5), 2012.

Independence is a term from probability theory and refers to the case where one event does not influence the probability of the occurrence of another event. Events can influence each other in many different ways. One ensemble may influence another if it attempts to correct the predictions made by it.

As such, depending on the ensemble type, models may be naturally dependent or independent.

- **Independence**: Whether the occurrence of an event affects the probability of subsequent events.

Correlation is a term from statistics and refers to two variables changing together. It is common to calculate a normalized correlation score between -1.0 and 1.0 where a score of 0.0 indicates no correlation, e.g. uncorrelated. A score of 1.0 or -1.0 one indicates perfect positive and negative correlation respectively and indicates two models that always predict the same (or inverse) outcome.

> … if the learners are independent, i.e., [correlation] = 0, the ensemble will achieve a factor of T of error reduction than the individual learners; if the learners are totally correlated, i.e., [correlation] = 1, no gains can be obtained from the combination.

— Page 99, [Ensemble Methods](https://amzn.to/2XZzrjG), 2012.

In practice, ensembles often exhibit a weak or modest positive correlation in their predictions.

- **Correlation**: The degree to which variables change together.

As such, ensemble models are constructed from constituent models that may or may not have some dependency and some correlation between the decisions or predictions made. Constructing good ensembles is a challenging task.

For example, combining a bunch of top-performing models will likely result in a poor ensemble as the predictions made by the models will be highly correlated. Unintuitively, you might be better off combining the predictions from a few top-performing individual models with the prediction from a few weaker models.

> So, it is desired that the individual learners should be accurate and diverse. Combining only accurate learners is often worse than combining some accurate ones together with some relatively weak ones, since complementarity is more important than pure accuracy.

— Page 100, [Ensemble Methods](https://amzn.to/2XZzrjG), 2012.

Sadly, there is no generally agreed upon measure of ensemble diversity and ideas of independence and correlation are only guides or proxies for thinking about the properties of good ensembles.

> Unfortunately, though diversity is crucial, we still do not have a clear understanding of diversity; for example, currently there is no well-accepted formal definition of diversity.

— Page 100, [Ensemble Methods](https://amzn.to/2XZzrjG), 2012.

Nevertheless, as guides, they are useful as we can devise techniques that attempt to reduce the correlation between the models.

## Methods for Increasing Diversity

The objective for developing good ensembles is considered through the lens of increasing the diversity of ensemble members.

Models in an ensemble may be more dependent if they share the same algorithm used to train the model and/or the same dataset used to train the model. Models in an ensemble may have higher correlation between their predictions for the same general reasons.

Therefore, approaches that make the models and/or the training data more different are desirable.

> Diversity may be obtained through different presentations of the input data, as in bagging, variations in learner design, or by adding a penalty to the outputs to encourage diversity.

— Page 93, [Pattern Classification Using Ensemble Methods](https://amzn.to/2zxc0F7), 2010.

It can be helpful to have a framework for thinking about techniques for managing the diversity of ensembles, and there are many to choose from.

For example, Zhi-Hua Zhou in Chapter 5 of his 2012 book titled “[Ensemble Methods: Foundations and Algorithms](https://amzn.to/2XZzrjG)” proposes a framework of four approaches to generating diversity. In summary, they are:

- **Data Sample Manipulation**: e.g. sample the training dataset differently for each model.
- **Input Feature Manipulation**: e.g. train each model on different groups of input features.
- **Learning Parameter Manipulation**: e.g. train models with different hyperparameter values.
- **Output Representation Manipulation**: e.g. train models with differently modified target values.

Perhaps the most common approaches are changes to the training data, that is data samples and input features, often combined in a single approach.

For another example of a taxonomy for generating a diverse ensemble, [Lior Rokach](https://www.linkedin.com/in/liorrokach) in Chapter 4 his 2010 book titled “[Pattern Classification Using Ensemble Methods](https://amzn.to/2zxc0F7)” suggest a similar taxonomy, summarized as:

- **Manipulating the Inducer**, e.g. manipulating in how models are trained.
    -   Vary hyperparameters.
    -   Varying starting point.
    -   Vary optimization algorithm.
- **Manipulating the Training Sample**, e.g. manipulating the data used for training.
    -   Resampling.
- **Changing the target attribute representation**, e.g. manipulating the target variable.
    -   Vary encoding.
    -   Error-correcting codes.
    -   Label switching.
- **Partitioning the search space**, e.g. manipulating the number of input features.
    -   Random subspace.
    -   Feature selection.
- **Hybridization**, e.g. varying model types or a mixture of the above methods.

The hybridization approach is common both in popular ensemble methods that combine multiple approaches at generating diversity in a single algorithm, as well as simply varying the algorithms (model types) that comprise the ensemble.

> Bundling competing models into ensembles almost always improves generalization – and using different algorithms as the perturbation operator is an effective way to obtain the requisite diversity of components.

— Page 89, [Ensemble Methods in Data Mining](https://amzn.to/3frGM1A), 2010.

This highlights that although we could investigate quantifying how diverse an ensemble is, that instead, most effort is on developing techniques that generate diversity.

We can harness this knowledge in developing our own [[Ensemble methods]], first trying standard and well-understood ensemble learning methods, then tailoring them for our specific dataset with model independence and correlation of predictions in mind in an effort to get the most out of them.

---
Topics :: [[Ensemble methods]]
Reference ::
Type :: #atom
Creator :: Dennis
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-18 11:23
