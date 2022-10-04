# Meta-Labeling

Meta-Labeling is a machine learning (ML) layer that sits on top of a base primary strategy, to help size positions, filter out false-positive signals, and improve metrics such as the Sharpe ratio and maximum drawdown.

![[MLA Base Architecture.png]]

Meta-labeling is the process of fitting a secondary model to determine whether a primary exogenous model is correct and to size positions accordingly. The target variable in this model are meta-labels, which are defined as a binary label {0, 1} that indicates whether the primary model’s forecast was profitable or not. Thus, it makes a meta prediction.

The output of this model is the probability of a positive outcome and is used to size positions where the greater the probability, the larger the position size. It represents a trade-off, in which recall is traded for precision, leading to a better model efficiency, represented by a higher F1-score (the harmonic mean between precision and recall).

![[precision_recall_tradeoff.png]]

Exhibit 7 illustrates the change in classification metrics between the secondary and primary models. A net positive change indicates an increase in performance and a negative change a decrease. Most notably, we can observe a considerable increase in the F1-score, indicating a more efficient classifier, capable of filtering out false positives; this is done by trading some recall for a higher precision (López de Prado 2020).t 7 illustrates the change in classification metrics between the secondary and primary models. A net positive change indicates an increase in performance and a negative change a decrease. Most notably, we can observe a considerable increase in the F1-score, indicating a more efficient classifier, capable of filtering out false positives; this is done by trading some recall for a higher precision (López de Prado 2020).

The technique also differs fundamentally from the use of an [[Ensemble]] model with new features or the use of stacking in the primary model. This is because the target variable of the secondary model are the meta-labels and not a side prediction, and it offers the opportunity to benefit from the trade-off between precision and recall to size positions.

Sources:
* Jacques wrote in-depth about this technique in [[Meta-Labeling Theory and Framework]]
* First introduced as a concept by Marcos Lopez de Prado, in [[Advances in Financial Machine Learning]].

---
Topics: [[Risk Management]], [[Machine Learning]]
Reference: [[Advances in Financial Machine Learning]]
Type: #atom
Creator :: Jacques
Date: 2022-06-28 00:40