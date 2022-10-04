# Strategy Risk Template

Before applying [[Meta-Labeling]] to a strategy, the first step is to understand the strategy’s risks ([[Advances in Financial Machine Learning]], Chapter 15) and to determine what the impact on the Sharpe ratio will be of increasing the precision at the cost of reducing the number of trades. 

The Sharpe ratio is a function of precision rather than accuracy, as true positives are rewarded, false positives are punished, and negatives are not rewarded as a position was never taken. Each strategy will have its own risk profile, and not all strategies will benefit from this trade off; however, strategies with a high number of trades will generally be more sensitive to a change in precision.

Exhibit 5 ([[Meta-Labeling Theory and Framework]]) illustrates this relationship for different numbers of trades, given symmetric payouts. Note that as the number of trades increases, the slope steepens, indicating a higher sensitivity to a change in precision. The relationship between the Sharpe ratio, precision, payouts, and the number of trades is recreated in the equations below (Lopez de Prado 2018a).

![[StrategyRisk.png]]

The number of positions are determined by the [[Primary Model]].

---
Topics: [[Risk Management]]
Reference: [[Advances in Financial Machine Learning]], [[Meta-Labeling Theory and Framework]]
Type: #atom 
Creator :: Jacques
Date: 2022-06-28 01:18

