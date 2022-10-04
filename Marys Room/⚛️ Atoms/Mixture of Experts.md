# Mixture of Experts
**Mixture of experts**, MoE or ME for short, is an ensemble learning technique that implements the idea of training experts on subtasks of a predictive modeling problem.

> In the neural network community, several researchers have examined the decomposition methodology. […] Mixture–of–Experts (ME) methodology that decomposes the input space, such that each expert examines a different part of the space. […] A gating network is responsible for combining the various experts.

— Page 73, [Pattern Classification Using Ensemble Methods](https://amzn.to/2zxc0F7), 2010.

There are four elements to the approach, they are:

-   Division of a task into subtasks.
-   Develop an expert for each subtask.
-   Use a gating model to decide which expert to use.
-   Pool predictions and gating model output to make a prediction.

The figure below, taken from Page 94 of the 2012 book “[Ensemble Methods](https://amzn.to/2XZzrjG),” provides a helpful overview of the architectural elements of the method.

![Example of a Mixture of Experts Model with Expert Members and A Gating Network](https://machinelearningmastery.com/wp-content/uploads/2020/07/Example-of-a-Mixture-of-Experts-Model-with-Expert-Members-and-A-Gating-Network.png)

Example of a Mixture of Experts Model with Expert Members and a Gating Network

### Subtasks

The first step is to divide the predictive modeling problem into subtasks. This often involves using domain knowledge. For example, an image could be divided into separate elements such as background, foreground, objects, colors, lines, and so on.

> … ME works in a divide-and-conquer strategy where a complex task is broken up into several simpler and smaller subtasks, and individual learners (called experts) are trained for different subtasks.

— Page 94, [Ensemble Methods](https://amzn.to/2XZzrjG), 2012.

For those problems where the division of the task into subtasks is not obvious, a simpler and more generic approach could be used. For example, one could imagine an approach that divides the input feature space by groups of columns or separates examples in the feature space based on distance measures, inliers, and outliers for a standard distribution, and much more.

> … in ME, a key problem is how to find the natural division of the task and then derive the overall solution from sub-solutions.

— Page 94, [Ensemble Methods](https://amzn.to/2XZzrjG), 2012.

### Expert Models

Next, an expert is designed for each subtask.

The mixture of experts approach was initially developed and explored within the field of artificial neural networks, so traditionally, experts themselves are neural network models used to predict a numerical value in the case of regression or a class label in the case of classification.

> It should be clear that we can “plug in” any model for the expert. For example, we can use neural networks to represent both the gating functions and the experts. The result is known as a mixture density network.

— Page 344, [Machine Learning: A Probabilistic Perspective](https://amzn.to/2YrVLmp), 2012.

Experts each receive the same input pattern (row) and make a prediction.

### Gating Model

A model is used to interpret the predictions made by each expert and to aid in deciding which expert to trust for a given input. This is called the gating model, or the gating network, given that it is traditionally a neural network model.

The gating network takes as input the input pattern that was provided to the expert models and outputs the contribution that each expert should have in making a prediction for the input.

> … the weights determined by the gating network are dynamically assigned based on the given input, as the MoE effectively learns which portion of the feature space is learned by each ensemble member

— Page 16, [Ensemble Machine Learning](https://amzn.to/2C7syo5), 2012.

The gating network is key to the approach and effectively the model learns to choose the type subtask for a given input and, in turn, the expert to trust to make a strong prediction.

> Mixture-of-experts can also be seen as a classifier selection algorithm, where individual classifiers are trained to become experts in some portion of the feature space.

— Page 16, [Ensemble Machine Learning](https://amzn.to/2C7syo5), 2012.

When neural network models are used, the gating network and the experts are trained together such that the gating network learns when to trust each expert to make a prediction. This training procedure was traditionally implemented using [expectation maximization](https://machinelearningmastery.com/expectation-maximization-em-algorithm/) (EM). The gating network might have a softmax output that gives a probability-like confidence score for each expert.

> In general, the training procedure tries to achieve two goals: for given experts, to find the optimal gating function; for a given gating function, to train the experts on the distribution specified by the gating function.

— Page 95, [Ensemble Methods](https://amzn.to/2XZzrjG), 2012.

### Pooling Method

Finally, the mixture of expert models must make a prediction, and this is achieved using a pooling or aggregation mechanism. This might be as simple as selecting the expert with the largest output or confidence provided by the gating network.

Alternatively, a weighted sum prediction could be made that explicitly combines the predictions made by each expert and the confidence estimated by the gating network. You might imagine other approaches to making effective use of the predictions and gating network output.

> The pooling/combining system may then choose a single classifier with the highest weight, or calculate a weighted sum of the classifier outputs for each class, and pick the class that receives the highest weighted sum.

— Page 16, [Ensemble Machine Learning](https://amzn.to/2C7syo5), 2012.

---
Topics :: [[Classifier Combination Strategies]]
Reference :: [[Ensemble methods]]
Type :: #atom
Creator :: Dennis
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-18 11:03
