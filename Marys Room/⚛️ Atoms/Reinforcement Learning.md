# # Reinforcement Learning


---
Topics :: [[Machine Learning]] [[Portfolio optimization]]
Reference :: [Liu, X.Y., Yang, H., Gao, J. and Wang, C.D., 2021, November. FinRL: Deep reinforcement learning framework to automate trading in quantitative finance. In _Proceedings of the Second ACM International Conference on AI in Finance_ (pp. 1-9).](https://www.sciencedirect.com/science/article/abs/pii/S0957417422013082)
Type :: #atom
Creator :: Michelle
Date :: 2022-07-15 15:30

![[reinforcement-learning.gif]]


An agent learns how to behave in a environment by performing actions and seeing the results. This agent will learn from the environment by interacting with it and receiving rewards for performing actions. The goal of the agent is to maximize the expected cumulative reward. Some rewards are more probable others less. An agent can care more about short term(more probable) reward or about long term(less probable) reward. This is determened by a discount rate. 

## Tasks
We can have two types of tasks: episodic and continuous. 

### Episodic task
You have a list of States, Actions, Rewards, and New States that all have a starting and ending point.

### Continuous task
The agent has to learn how to choose the best actions and simultaneously interacts with the environment as the task has no startong or ending point.


## Learning methods

### Monte Carlo
Learning by collecting the rewards at the end of the task and then calculating the maximum expected future reward. In other words the rewards are only received at the end of the task. When the new task or state begins the knowledge from the previous task remains. The agent will make better decisions after each task is completed.

### Temporal Difference Learning
Learning by estimating the rewards at each step.


## Exploitation trade off
* Exploration is finding more information about the environment. 
* Exploitation is exploiting known information to maximize the reward.

An agent will only explore th nearest region with reward if there is no exploration trade-off.

## 3 Methods for Reinforcement learning

### Value Based



The value function is a function that tells us the maximum expected future reward the agent will get at each state. The value of each state is the total amount of the reward an agent can expect to accumulate over the future, starting at that state. The agent will use this value function to select which state to choose at each step. The agent takes the state with the biggest value.

### Policy Based
In policy-based RL, we want to directly optimize the policy function without using a value function.

### Model Based
In model-based RL, we model the environment. This means we create a model of the behavior of the environment.