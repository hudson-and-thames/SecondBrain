# Cross Entropy
## What Is Cross-Entropy?

Cross-entropy is a measure of the difference between two probability distributions for a given random variable or set of events.

You might recall that **information** quantifies the number of bits required to encode and transmit an event. Lower probability events have more information, higher probability events have less information.

In information theory, we like to describe the “_surprise_” of an event. An event is more surprising the less likely it is, meaning it contains more information.

-   **Low Probability Event** (_surprising_): More information.
-   **Higher Probability Event** (_unsurprising_): Less information.

Information _h(x)_ can be calculated for an event _x_, given the probability of the event _P(x)_ as follows:

-   h(x) = -log(P(x))

**Entropy** is the number of bits required to transmit a randomly selected event from a probability distribution. A skewed distribution has a low entropy, whereas a distribution where events have equal probability has a larger entropy.

A skewed probability distribution has less “surprise” and in turn a low entropy because likely events dominate. Balanced distribution are more surprising and turn have higher entropy because events are equally likely.

-   **Skewed Probability Distribution** (_unsurprising_): Low entropy.
-   **Balanced Probability Distribution** (_surprising_): High entropy.

Entropy _H(x)_ can be calculated for a random variable with a set of _x_ in _X_ discrete states discrete states and their probability _P(x)_ as follows:

-   H(X) = – sum x in X P(x) * log(P(x))

If you would like to know more about calculating information for events and entropy for distributions see this tutorial:

-   [A Gentle Introduction to Information Entropy](https://machinelearningmastery.com/what-is-information-entropy/)

**Cross-entropy** builds upon the idea of entropy from information theory and calculates the number of bits required to represent or transmit an average event from one distribution compared to another distribution.

> … the cross entropy is the average number of bits needed to encode data coming from a source with distribution p when we use model q …

— Page 57, [Machine Learning: A Probabilistic Perspective](https://amzn.to/2xKSTCP), 2012.

The intuition for this definition comes if we consider a target or underlying probability distribution P and an approximation of the target distribution Q, then the cross-entropy of Q from P is the number of additional bits to represent an event using Q instead of P.

The cross-entropy between two probability distributions, such as Q from P, can be stated formally as:

-   H(P, Q)

Where H() is the cross-entropy function, P may be the target distribution and Q is the approximation of the target distribution.

Cross-entropy can be calculated using the probabilities of the events from P and Q, as follows:

-   H(P, Q) = – sum x in X P(x) * log(Q(x))

Where P(x) is the probability of the event x in P, Q(x) is the probability of event x in Q and log is the base-2 logarithm, meaning that the results are in bits. If the base-e or natural logarithm is used instead, the result will have the units called nats.

This calculation is for discrete probability distributions, although a similar calculation can be used for continuous probability distributions using the integral across the events instead of the sum.

The result will be a positive number measured in bits and will be equal to the entropy of the distribution if the two probability distributions are identical.

**Note**: this notation looks a lot like the joint probability, or more specifically, the [joint entropy](https://en.wikipedia.org/wiki/Joint_entropy) between P and Q. This is misleading as we are scoring the difference between probability distributions with cross-entropy. Whereas, joint entropy is a different concept that uses the same notation and instead calculates the uncertainty across two (or more) random variables.

## Cross-Entropy as a Loss Function

Cross-entropy is widely used as a loss function when optimizing classification models.

Two examples that you may encounter include the logistic regression algorithm (a linear classification algorithm), and artificial neural networks that can be used for classification tasks.

> … using the cross-entropy error function instead of the sum-of-squares for a classification problem leads to faster training as well as improved generalization.

— Page 235, [Pattern Recognition and Machine Learning](https://amzn.to/2JwHE7I), 2006.

Classification problems are those that involve one or more input variables and the prediction of a class label.

Classification tasks that have just two labels for the output variable are referred to as binary classification problems, whereas those problems with more than two labels are referred to as categorical or multi-class classification problems.

- **Binary Classification**: Task of predicting one of two class labels for a given example.
- **Multi-Class Classification**: Task of predicting one of more than two class labels for a given example.

We can see that the idea of cross-entropy may be useful for optimizing a classification model.

Each example has a known class label with a probability of 1.0, and a probability of 0.0 for all other labels. A model can estimate the probability of an example belonging to each class label. Cross-entropy can then be used to calculate the difference between the two probability distributions.

As such, we can map the classification of one example onto the idea of a random variable with a probability distribution as follows:

- **Random Variable**: The example for which we require a predicted class label.
- **Events**: Each class label that could be predicted.

In classification tasks, we know the target probability distribution P for an input as the class label 0 or 1 interpreted as probabilities as “_impossible_” or “_certain_” respectively. These probabilities have no surprise at all, therefore they have no information content or zero entropy.

Our model seeks to approximate the target probability distribution Q.

In the language of classification, these are the actual and the predicted probabilities, or _y_ and _yhat_.

- **Expected Probability** (_y_): The known probability of each class label for an example in the dataset (P).
- **Predicted Probability** (_yhat_): The probability of each class label an example predicted by the model (Q).

We can, therefore, estimate the cross-entropy for a single prediction using the cross-entropy calculation described above; for example.

-   H(P, Q) = – sum x in X P(x) * log(Q(x))

Where each _x_ in _X_ is a class label that could be assigned to the example, and _P(x)_ will be 1 for the known label and 0 for all other labels.

The cross-entropy for a single example in a binary classification task can be stated by unrolling the sum operation as follows:

-   H(P, Q) = – (P(class0) * log(Q(class0)) + P(class1) * log(Q(class1)))

You may see this form of calculating cross-entropy cited in textbooks.

If there are just two class labels, the probability is modeled as the [Bernoulli distribution](https://machinelearningmastery.com/discrete-probability-distributions-for-machine-learning/) for the positive class label. This means that the probability for class 1 is predicted by the model directly, and the probability for class 0 is given as one minus the predicted probability, for example:

-   **Predicted P(class0)** = 1 – yhat
-   **Predicted P(class1)** = yhat

When calculating cross-entropy for classification tasks, the base-e or natural logarithm is used. This means that the units are in nats, not bits.

We are often interested in minimizing the cross-entropy for the model across the entire training dataset. This is calculated by calculating the average cross-entropy across all training examples.

https://www.youtube.com/watch?v=ErfnhcEV1O8

---
Topics :: [[Machine Learning]]
Reference :: [[Model Selection]] [[Model evaluation]]
Type :: #atom
Creator :: Dennis
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-28 17:22
