# Classifier Combination Strategies
Once an ensemble is built a strategy to combine those classifiers is employed. Combination rules are often grouped as
(i) trainable vs. non-trainable combination rules or,
(ii) combination rules that apply to class labels vs. to class-specific continuous outputs.

In trainable combination rules, the parameters of the combiner, usually called *weights*, are determined through a separate training algorithm. The Expectation-Maximisation (EM) algorithm used by the mixture-of-experts model is such an example. The combination parameters created by trainable rules are usually instance specific, and hence are also called dynamic combination rules. Conversely, there is no separate training involved in non-trainable rules beyond that for generating the ensembles. Weighted majority voting is an example of such non-trainable rules, since the parameters become immediately available as the classifiers are generated.

In the second taxonomy, combination rules that apply to class labels need the classification decision only (that is, one of ωj,j=1,... ,C), whereas others need the continuous-valued outputs of individual classifiers. These values often represent the degrees of support the classifiers give to each class, and they can estimate class conditional posterior probabilities P(ωj|x) if (i) they are appropriately normalized to add up to 1 for all classes, and (ii) if the classifiers are trained with sufficiently dense data. Many classifier models, such as the Multilayer percepton (MLP) and the Radial basis function (RBF) networks, provide continuous-valued outputs, which are often interpreted as posterior probabilities—despite the sufficiently dense training data requirement rarely being met in practice.

Examples for classifier combination strategies are:
- algebraic combiners
- voting methods
- decision templates

@article{polikar2006ensemble,
  title={Ensemble based systems in decision making},
  author={Polikar, Robi},
  journal={IEEE Circuits and systems magazine},
  volume={6},
  number={3},
  pages={21--45},
  year={2006},
  publisher={IEEE}
}
p.33

---
Topics :: [[Ensemble methods]]
Reference ::
Type :: #atom
Creator :: Dennis
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-15 17:32
