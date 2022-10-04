# Region of competence
Define the local region surrounding the query in which the competence level of the base classifiers is estimated.

The definition of a local region is of fundamental importance to Dynamic Selection (DS) methods, since the performance of all DS techniques is very sensitive to the distribution of this region.
Usually, the local regions are defined using the K-NN technique, via clustering methods (e.g. K-Means), using the decisions of the base classifier or a competence map that is defined through the use of a potential function. In all cases, a set of labeled samples, which can be either the training or validation set, is required. This set is called the dynamic selection dataset (DSEL).

---
Topics :: [[Dynamic Ensemble Selection]]
Reference :: [[Model Selection]]
Type :: #atom
Creator :: Dennis
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-15 16:39
