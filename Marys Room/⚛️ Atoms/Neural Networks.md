# Neural Networks

Neural networks (NN) are statistical models or algorithms developed from research into the function of the nature of the brain where the models "borrow" certain key concepts such as that of how neurons interact with each other. These algorithms are adapted to suite the purpose of learning and optimization for a given problem and have become very popular in recent years for an array of tasks.
The broad fundamental mathematical framework for a NN model is a directed graph which consists of the following properties:
1. A state variable $n_{i}$ is associated with each node $i$.
2. A real-valued weight $w_{i k}$ is associated with each link $(i k)$ between two nodes $i$ and $k$.
3. A real-valued bias $\vartheta_{i}$ is associated with each node $i$.
4. A transfer function $f_{i}\left[n_{k}, w_{i k}, \vartheta_{i},(k \neq i)\right]$ is defined, for each node $i$, which determines the state of the node as a function of its bias, of the weights of its incoming links, and of the states of the nodes connected to it by these links.


The term neural network (NN) has evolved to encompass a large class of models
and learning methods. The discussion that follows explains the most fundamental aspects of "vanilla" NNs, which is called the single hidden layer back-propagation network,
or single layer perceptron. There has been a great deal of hype surrounding
neural networks, making them seem almost magical and mysterious while in fact they are just nonlinear statistical models 
A neural network is a two-stage regression or classification model, typically represented by a network diagram . This network applies both to regression or classification. For regression, typically K = 1 and there is only one output unit Y1 at the top. However, these networks can handle multiple quantitative responses in a seamless fashion,  the general case is dealt with. An example of a single layer neural network is given in figure below.

![[Neural_network_example.svg.png]]

---
Topics :: [[Machine Learning]]
Reference ::
Type :: #atom
Creator :: Michael
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-15 16:32
