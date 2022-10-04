# Particle Swarm based feature selection

Citation:: [Xue, B., Zhang, M. and Browne, W.N., 2014. Particle swarm optimisation for feature selection in classification: Novel initialisation and updating mechanisms. _Applied soft computing_, _18_, pp.261-276.](https://homepages.ecs.vuw.ac.nz/~xuebing/Papers/ASOC2076.pdf)
Type:: #source #academic 
Topics :: [[Feature Selection]]
Creator :: Michelle
Date :: 2022-07-15 09:52

---
![[pso-convergence.gif]]

### Concepts
* Particle Swarm Optimization(PSO):

	A stochastic search technique that solves continuous optimization problems. It was developed after the social behavior of animals in their search for food. This behavior is modeled by initializing randomly selected solutions called particles in a search space. These particles form a swarm. Each particle updates its position by recalling its distance from where it was previously successful and where the swarm has already been successful in finding food. The distance needed to move closer to a successful answer is called the velocity. The velocity of all the particles will converge to approximately zero when a final solution has been reached.


![[pso-hyperparms.gif]]


* Binary Particle Swarm Optimization(BPSO):

	BPSO was developed for discrete binary variables. This is useful for feature selection because features can be seen as discrete binary variables. A selected feature can be seen as a one when selected and a zero when de-selected. This binary representation of PSO is still based on standard PSO and therefore experiences the same shortcomings of PSO. BPSO suers from early convergence towards a feature subset that could have had a higher model accuracy or been more parsimonious.


* Analyses 3 models:
	* Modied BPSO(MBPSO)
	* Improved Novel BPSO(INBPSO)
	* BPSO 4-2


### Great Points

* Meta-heuristic feature selection uses a stochastic approach to find approximate feature subset solutions within a reasonable time frame. Meta-heuristics are inspired by nature where a population of units work together to optimize a function over a number of iterations.
* Evaluating a large number of features at once creates a large search space. Meta-heuristic strategies have a global search ability which can evaluate a large feature space.
* The model accuracy is evaluated with a tness function. This evaluation together with hyper and stochastic parameters drive this population of particles closer to an optimal feature subset solution.


### References
[Xue, B., Zhang, M. and Browne, W.N., 2014. Particle swarm optimisation for feature selection in classification: Novel initialisation and updating mechanisms. _Applied soft computing_, _18_, pp.261-276.](https://homepages.ecs.vuw.ac.nz/~xuebing/Papers/ASOC2076.pdf)

[Vieira, S.M., Mendonça, L.F., Farinha, G.J. and Sousa, J.M., 2013. Modified binary PSO for feature selection using SVM applied to mortality prediction of septic patients. _Applied Soft Computing_, _13_(8), pp.3494-3504.](https://www.sciencedirect.com/science/article/abs/pii/S1568494613001361)

[Nezamabadi-pour, H., Rostami-Shahrbabaki, M. and Maghfoori-Farsangi, M., 2008. Binary particle swarm optimization: challenges and new solutions. _CSI J Comput Sci Eng_, _6_(1), pp.21-32.](http://www.cs.us.es/~fsancho/ficheros/IA2019/INBPSO.pdf)

