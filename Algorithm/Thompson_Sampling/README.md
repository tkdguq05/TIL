[![HitCount](http://hits.dwyl.io/tkdguq05/Algorithm / Thompson_Sampling.svg)](http://hits.dwyl.io/tkdguq05/Algorithm / Thompson_Sampling)

# This Repository is
 - Programming Thompson Sampling Algorithm
 - Calculating Bayesian Probability
 
 
## Thompson Sampling
- 50% - Exploration
- 50% - Exploitation

The Thompson Sampling exploration part is more sophisticated than e-Greedy algorithm. We have been using Beta distribution* here, however Thompson Sampling can be generalized to sample from any distributions over parameters.

* In probability theory and statistics, the beta distribution is a family of continuous probability distributions defined on the interval [0, 1] parametrized by two positive shape parameters, denoted by  α  and  β , that appear as exponents of the random variable and control the shape of the distribution.

If you want to know more about Beta distribution here is an article I found extremely useful.

#### Logic:

1) Choose prior distributions for parameters  α  and  β .
2) Calculate the  α  and  β  values as:  α=prior+hits ,  β=prior+misses . In our case hits = number of clicks, misses = number of impressions without a click. Priors are useful if you have some prior information about the actual CTR’s of your ads. Here, we do not, so we’ll use 1.0.
3) Estimate actual CTR’s by sampling values of Beta distribution for each variant  B(αi,βi)  and choose the sample with the highest value (estimated CTR).
4) Repeat 2-3.


<a href="https://www.kaggle.com/ruslankl/how-to-deal-with-multi-armed-bandit-problem">Main Source From Kaggle</a>
