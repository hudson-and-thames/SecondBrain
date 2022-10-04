citation: [A Backtesting Protocol in the Era of Machine Learning](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3275654), by Robert D. Arnott, Campbell R. Harvey, and Harry Markowitz.
Type: #source #academic 
Creator:: Jacques
Topics: [[Quantitative Finance]]
Date: 2022-06-28 12:15

---

# 7 Point Backtesting Protocol

As per Exhibit 2, pg.16:

1.  Research Motivation
	1. Does the model have a solid economic foundation?
	2. Did the economic foundation or hypothesis exist before the research was conducted?

2.  Multiple Testing and Statistical Methods
	1. Did the researcher keep track of all models and variables that were tried (both successful and unsuccessful) and are the researchers aware of the multiple-testing issue?
	2. Is there a full accounting of all possible interaction variables if interaction variables are used?
	3. Did the researchers investigate all variables set out in the research agenda or did they cut the research as soon as they found a good model?      
    
3.  Data and Sample Choice
    1. Do the data chosen for examination make sense? And, if other data are available, does it make sense to exclude these data?
    2. Did the researchers take steps to ensure the integrity of the data?
    3. Do the data transformations, such as scaling, make sense? Were they selected in advance? And are the results robust to minor changes in these transformations?
    4. If outliers are excluded, are the exclusion rules reasonable?
    5. If the data are winsorized, was there a good reason to do it? Was the winsorization rule chosen before the research was started? Was only one winsorization rule tried (as opposed to many)?
    
4.  Cross-Validation
    1. Are the researchers aware that true out-of-sample tests are only possible in live trading?
    2. Are steps in place to eliminate the risk of out-of-sample “iterations” (i.e., an in-sample model that is later modified to fit out-of-sample data)?
    3. Is the out-of-sample analysis representative of live trading? For example, are trading costs and data revisions taken into account? 
    
5.  Model Dynamics
    1. Is the model resilient to structural change and have the researchers taken steps to minimize the overfitting of the model dynamics?
    2. Does the analysis take into account the risk/likelihood of overcrowding in live trading?
    3. Do researchers take steps to minimize the tweaking of a live model?
    
6.  Complexity
    1. Does the model avoid the curse of dimensionality?
    2. Have the researchers taken steps to produce the simplest practicable model specification?
    3. Is an attempt made to interpret the predictions of the machine learning model rather than using it as a black box?
    
7.  Research Culture
    1. Does the research culture reward quality of the science rather than finding the winning strategy?
    2. Do the researchers and management understand that most tests will fail?
    3. Are expectations clear (that researchers should seek the truth not just something that works) when research is delegated?