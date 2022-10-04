# MLA model evaluation

[[Meta-Labeling]] primarly gains advatage as described in [[3 Sources of Advantage (MLA)]]. However these advantages mainly focus on increasing prediction accuracy (or more specifically precision) to increase the Sharpe Ratio.

Rather than using MLA as a tool to aid prediction, it can be used to gain insight into the primary model, i.e for inference . For example using [[Shannon's Entropy]] on the meta labels to show how "suprised" we are about how the model is performing.

In [[Meta-Labeling Theory and Framework]] the author uses a primary strategy that uses the previous days return to forecast the side of the trade. An AR(3) model is then  used to generate the data and then subsequently, the last 3 days returns are used in the meta model to showcase the [[Information Advantage]]. However how can one determine the information not being exploited in the primary model in practice? If one can accomplish then inference could also be gained on deficiencies in the primary model.

---
Topics:: [[Meta-Labeling]]
Reference::
Type:: #molecule #novel
Date: 2022-07-04 16:05
Rating :: 6
Creator :: Michael
Discussion :: 
Dis_Topic :: 
Resolved :: 

