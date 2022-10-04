# Long-Short MLA

The long-short model extends the long only model model by incorporating additional label for shorting so that $\dot{Y} \in \{-1,0,1\}$. An easy way to account for this is to simply have one M2 model as previously, which is trained on all the labels. However if the features driving a long or short position respectively, is fundamentally different , a better possible solution is to fit separate M2 models to each of the labels. The idea is that each of the models can pick up on characteristics that are more relevant to the position taken. \ref{fig:ls} displays this type of architecture where $M2_{1}$ represents the the MLA model trained on the long positions, and $M_2{-1}$, the MLA model trained on the short position. $X_1$ and $X_{-1}$ are input data related to the long and short positions. 

![[Long_Short.drawio.png]]

---
Topics :: [[Meta-Labeling]] [[MLA Architecture]]
Reference ::
Type :: #molecule #novel
Creator :: Michael
Rating :: 8
TAF :: Jacques
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-11 08:44

