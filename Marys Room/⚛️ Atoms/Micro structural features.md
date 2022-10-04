# Micro structural features
Microstructural datasets include primary information about the auctioning process, like order cancellations, double action book, queues, partial fills, aggressor side, corrections, and replacements. These datasets provide researchers with the ability to understand how market participants conceal and reveal their true preferences, making them incredibly useful for engineering features of an ML model.

This module concerns itself with the so-called “first generation” of microstructural models and a series of transformations of their outputs - namely:

- The Tick Rule   
-   _The Roll Model_
-   _Fractional Differentiation_
-   _Wald-Wolfowitz Runs Randomness_


Second generation models explain trading as a strategic interaction between informed and uninformed traders leading to a stronger theoretical framework than first generation models. These models emphasize the importance of signed volume and order flow imbalance. Most of the parameters of interest (such as lambda) are estimated by applying regression. Inter-bar microstructural features can be obtained when bars are created such as time, volume, imbalance and run bars. There are mainly three second generation models described in this section are:

-   _Kyle’s Lambda_    
-   _Amihud’s Lambda_
-   _Hasbrouck’s Lambda_


Third generation models look at microstructures through the lens of randomly selected traders that arrive at the market sequentially and independently. Sequential trade models have become very popular among market makers. One reason is, they incorporate the sources of uncertainty faced by liquidity providers, namely the probability that an informational event has taken place, the probability that such event is negative, the arrival rate of noise traders, and the arrival rate of informed traders. With those variables, market makers must update quotes dynamically, and manage their inventories.
 [Easley et al. (1998)](https://www.sciencedirect.com/science/article/pii/S1386418198000020) use trade data to determine the probability of information-based trading (PIN) of individual securities. This microstructure model views trading as a game between market makers and position takers that is repeated over multiple trading periods.

![[close_prices_vpn.jpg]]

---
Topics :: [[Risk Management]]
Reference :: [[Advances in Financial Machine Learning]]
Type :: #atom
Creator :: Michael 
TAF ::
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-18 10:49
