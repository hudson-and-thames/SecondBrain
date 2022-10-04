# Selection Criteria
*Used to estimate the competence level of classifiers*

Model selection can be either conducted in a **static** or **dynamic** fashion.
The most common selection criteria used for selecting static ensembles are *diversity* and *classification accuracy*.
Many search algorithms have been considered for static selection, such as greedy search, evolutionary algorithms and other heuristic approaches.
In contrast, in dynamic selection, a single classifier or an ensemble is selected specifically to *classify each unknown example*. Based on a pool of classifiers, dynamic selection techniques consist in finding a single classifier, or an ensemble of classifiers, having the most competent classifiers for the classification of a specific query. The rationale for dynamic selection techniques is that each base classifier is an expert in distinct regions of the feature space. The method aims to select the most competent classifiers in the local region where the query is located.

@article{cruz2018dynamic,
  title={Dynamic classifier selection: Recent advances and perspectives},
  author={Cruz, Rafael MO and Sabourin, Robert and Cavalcanti, George DC},
  journal={Information Fusion},
  volume={41},
  pages={195--216},
  year={2018},
  publisher={Elsevier}
}
p.3

---
Topics :: [[Model Selection]]
Reference ::  [[Dynamic Ensemble Selection]] [[Ensemble methods]]
Type :: #atom
Creator :: Dennis
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-15 16:52
