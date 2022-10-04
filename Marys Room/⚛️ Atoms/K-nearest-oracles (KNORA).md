# K-nearest-oracles (KNORA)
The concept of the *K*-nearest-oracles (KNORA) consider the neighbourhood of test patterns to find the best ensemble for a given sample. For any test data point, KNORA simply finds its nearest *K* neighbours in the validation set, figures out which classifiers correctly classify those neighbours in the validation set and uses them as the ensemble for classifying the given pattern in that test set.

There are two different main schemes:
1. **KNORA-E** (Eliminate)
	Selects all classifiers that achieve perfect predictions on the neighborhood of k examples in the neighborhood. If no classifier achieves 100 percent accuracy, the neighborhood size is reduced by one and the models are re-evaluated. This process is repeated until one or more models are discovered that has perfect performance, and then used to make a prediction for the new example.
	
	![[Pasted image 20220715161236.png]]
On the left side, test pattern is shown as a hexagon, validation data points are shown as circles and the 5 nearest validation points are darkened. On the right side, the used classifiers - the intersection of correct classifiers - are darkened.

2. **KNORA-U** (Union)
	Selects all classifiers that make at least one correct prediction in the neighbourhood. The predictions from each classifier are then combined using a weighted average, where the number of correct predictions in the neighbourhood indicates the number of votes assigned to each classifier.
	
![[Pasted image 20220715161328.png]]
On the left side, test pattern is shown as a hexagon, validation data points are shown as circles, and the 5 nearest validation points are darkened. On the right side, the used classifiers—the union of correct classifiers—are darkened.

@article{ko2008dynamic,
  title={From dynamic classifier selection to dynamic ensemble selection},
  author={Ko, Albert HR and Sabourin, Robert and Britto Jr, Alceu Souza},
  journal={Pattern recognition},
  volume={41},
  number={5},
  pages={1718--1731},
  year={2008},
  publisher={Elsevier}
}


Topics :: [[Dynamic Ensemble Selection]]
Reference :: [[Ensemble methods]]
Type :: #atom
Creator :: Dennis
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-15 15:36
