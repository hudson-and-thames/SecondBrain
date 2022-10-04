# Sequential MLA (SMLA)

The idea is to fit sequential models that takes into account previous model outputs together with a set of inputs. The fist case would be where $M_{2_1}$ takes in parameters $\tilde{Y}$ and $X_1$, where $X_i$, $i =1, \ldots, n$ represent the information the model is given at each subsequent time. To simplify matters the models could possibly use $X_1 = X_2, = \ldots , X_n$. The output of $M_{2_1}$ , $\hat{Y)_1}$ could be subsequently fed into $M_{2_1}$  along with $\tilde{Y}$ and $X_2$. This procedure could be repeated $N$ times then after which the $\hat{Y}_n$ is produced and the meta labels $F \in {0,1}$ is obtained. 

The choice of the $M_2$ models is up for debate, however it is suggested that different types of models are used to model different characteristics. For example, $M_{2_1}$ could be a logistic regression model while $M_{2_2}$, could be a support vector machine. These models use different principles to generate their output and can therefore be used.  This model architecture will be prone to overfitting if there are too many $M_2$ models and should be handled with care.

![[SMLA.drawio.png]]

This architecture draws parralles to boosting, however there are a few key differences. Firstly, in boosting the data is sequentially given to the models using the same input data, where the input data at each stage is a function of the loss function. Greater weights are given to the  features where the model performance is poor, to increase classifications accuracy in those are of the feature space.  With SMLA, different features could be used if for example, there is a clear disctiontion between the factors driving the linear and non-linear relation to the target variable. 
Secondly, boosting usually entails specifying the same model type at each stage and using the given training data to find the parameters of each model. The process is then repeated untill a suitable stopping criterion is reach. SMLA rather encourages using different models to pick up on the different charecteristics. In this sense, applying a boosting alogorithm architecture could be thought of as a subset of SMLA.  







---
Topics :: [[Meta-Labeling]] Machine Learning
Reference ::
Type :: #molecule #novel
Creator :: Michael
Rating :: 8
TAF :: Jacques
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-11 09:32

