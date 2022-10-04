# Naive Bayes


---
Topics :: [[Machine Learning]] 
Reference ::  [Bruce, P., Bruce, A. and Gedeck, P., 2020. _Practical statistics for data scientists: 50+ essential concepts using R and Python_. O'Reilly Media.](https://books.google.co.za/books?hl=en&lr=&id=k2XcDwAAQBAJ&oi=fnd&pg=PP1&dq=Practical+Statistics+for+Data+Scientists&ots=dDLkhkUeBX&sig=-qTlzRa3JlP9tbAVDyIYdw-S1Ck&redir_esc=y#v=onepage&q=Practical%20Statistics%20for%20Data%20Scientists&f=false)
Type :: #atom
Creator :: Michelle
TAF :: Michelle
Date :: 2022-07-17 20:48

The naive Bayes algorithm uses the probability of observing predictor values, given an outcome, to estimate what is really of interest: the probability of observing outcome Y = i, given a set of predictor values.

![[Naive-bayes.png]]

For each record to be classified: 
1. Find all the other records with the same predictor profile (i.e., where the predictor values are the same). 
2. Determine what classes those records belong to and which class is most prevalent (i.e., probable). 
3. Assign that class to the new record. The preceding approach amounts to finding all the records in the sample that are exactly like the new record to be classified in the sense that all the predictor values are identical.

### The Naive Solution

1. For a binary response Y = i (i = 0 or 1), estimate the individual conditional probabilities for each predictor; these are the probabilities that the predictor value is in the record when we observe Y = i. This probability is estimated by the proportion of variable values among the Y = i records in the training set. 
2. Multiply these probabilities by each other, and then by the proportion of records belonging to Y = i. 
3. Repeat steps 1 and 2 for all the classes. 
4. Estimate a probability for outcome i by taking the value calculated in step 2 for class i and dividing it by the sum of such values for all classes. 
5. Assign the record to the class with the highest probability for this set of predictor values.