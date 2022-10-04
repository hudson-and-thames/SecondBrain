# Random Forests
---
Topics :: [[Machine Learning]] 
Reference :: [[⚛️ Atoms/Bagging]]
Type :: #atom
Creator :: Michelle
TAF :: Michelle
Date :: 2022-07-15 18:41


## Decision trees
A series of yes/no questions asked about our data eventually leading to a predicted class  or continuos value.  What this means is the decision tree tries to form nodes containing a high proportion of samples (data points) from a single class by finding values in the features that cleanly divide the data into classes. It is a non-linear model built by constructing many linear boundaries.

All the nodes, except the leaf nodes (colored terminal nodes), have 5 parts:

1.  Question asked about the data based on a value of a feature. Each question has either a True or False answer that splits the node. Based on the answer to the question, a data point moves down the tree.
2.  `gini`: The Gini Impurity of the node. The average weighted Gini Impurity decreases as we move down the tree.
3.  `samples`: The number of observations in the node.
4.  `value`: The number of samples in each class. For example, the top node has 2 samples in class 0 and 4 samples in class 1.
5.  `class`: The majority classification for points in the node. In the case of leaf nodes, this is the prediction for all samples in the node.

The leaf nodes do not have a question because these are where the final predictions are made.

![[decision-tree.png]]

## Gini Impurity
he [Gini Impurity](https://en.wikipedia.org/wiki/Decision_tree_learning#Gini_impurity) of a node is the probability that a randomly chosen sample in a node would be incorrectly labeled if it was labeled by the distribution of samples in the node.
At each node, the decision tree searches through the features for the value to split on that results in the _greatest reduction_ in Gini Impurity. (An [alternative for splitting nodes is using the information gain](https://datascience.stackexchange.com/questions/10228/gini-impurity-vs-entropy), a related concept).

It then repeats this splitting process in a greedy, [recursive procedure](http://scikit-learn.org/stable/modules/tree.html#tree) until it reaches a maximum depth, or each node contains only samples from one class. The weighted total Gini Impurity at each level of tree must decrease

## Overfitting: Or Why a Forest is better than One Tree
**Overfitting** occurs when we have a [very flexible model](http://qr.ae/TUNozZ) (the model has a high capacity) which essentially **memorizes** the training data by fitting it closely. The problem is that the model learns not only the actual relationships in the training data, but also any noise that is present. A flexible model is said to have high **_variance_** because the learned parameters (such as the structure of the decision tree) will vary considerably with the training data.

The reason the decision tree is prone to overfitting when we don’t limit the maximum depth is because it has unlimited flexibility, meaning that it can keep growing until it has exactly one leaf node for every single observation, perfectly classifying all of them.


## Random Forest 

The [random forest](https://www.stat.berkeley.edu/~breiman/RandomForests/cc_home.htm) is a model made up of many decision trees. Rather than just simply averaging the prediction of trees (which we could call a “forest”), this model uses two key concepts that gives it the name _random_:

1.  Random sampling of training data points when building trees
2.  Random subsets of features considered when splitting nodes

When training, each tree in a random forest learns from a **random** sample of the data points. The samples are [drawn with replacement](https://en.wikipedia.org/wiki/Bootstrapping_(statistics)), known as _bootstrapping,_ which means that some samples will be used multiple times in a single tree. The idea is that by training each tree on different samples, although each tree might have high variance with respect to a particular set of the training data, overall, the entire forest will have lower variance but not at the cost of increasing the bias.