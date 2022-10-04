# Deep Recurrent Modelling of Granger Causality with Latent Confounding
Citation::
Type:: #source #academic 
Topics :: [[Granger Causality]]
Creator :: Dennis
Date :: 2022-07-07 14:57

https://arxiv.org/pdf/2202.11286

---
## Abstract
Inferring causal relationships in observational time series data is an important task when interventions cannot be performed. Granger causality is a popular framework to infer potential causal mechanisms between different time series. The original definition of Granger causality is restricted to linear processes and leads to spurious conclusions in the presence of a latent confounder. In this work, we harness the expressive power of recurrent neural networks and propose a deep learning-based approach to model non-linear Granger causality by directly accounting for latent confounders. Our approach leverages multiple recurrent neural networks to parameterise predictive distributions and we propose the novel use of a dual-decoder setup to conduct the Granger tests. We demonstrate the model performance on non-linear stochastic time series for which the latent confounder influences the cause and effect with different time lags; results show the effectiveness of our model compared to existing benchmarks.