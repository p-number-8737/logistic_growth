**Question 1:** 

I used the experiment 1.csv file for this logistic growth data analysis - which is the initial population size (N0), intrinsic rate of growth (r) and carrying capacity (K) of _Escherichia coli_. 

The intrinsic growth rate is the rate  of growth of a population unrestratined by limiting resources. The carrying capacity provides the maximum number of individuals which can be sustained in a given environment. These concepts are fundamental for studying population dynamics.

This is the order of steps for data analysis using each repo provided:
1. _plot the experiment 1 data_
   - the data is plot first to visually interpret overall trends and patterns in the data to help inform subsequent modelling analysis
   - logistic growth should show initial exponential growth phase followed by a plateau as population reaches carrying capacity producing an S-shaped plot
     
2. _fit the linear model for experiment 1_
   - fit first linear model for the exponential growth phase where K > N0
   - summary of linear model gives slope estimate (r), intercept (N0), R2 (biological relevance) and P-value (significance)
        - **r = 0.0095218**
        - **N0 = 1320**
          
   - fit second linear model with N = K
   - summary of linear model estimates carrying capacity by assuming N plateaus at K
        - **K = 5.979e+10**
   
3. _assess the fit of the model to the experiment 1 data graphically_
   - define the logistic growth function and set model parameters of initial population size (N0), growth rate (r) and carrying capacity (K)
   - plot the model data curve, and then the actual data points

The results of the analysis show there is good fit of the logistic model to the actual data. This suggests the logistic model is reliable for describing the population growth dynamics of _Escherichia coli_. 

This means the data has a rapid initial exponential growth phase, followed by a plateau as the population reaches carrying capacity and resources become limited. 

The good fit means the estimated parameters K, N0 and r accurately match the actual data which can be used to accurately predict future population dynamics, and the population size from these parameters over different time steps. An r value of 0.0095218 suggests the population has relatively slow growth rate, despite having a relatively large carrying capacity (K) which suggests there are enough resources to sustain large populations.


**Question 2:** 
- The formula to calculate N at t = 4980 min is N(t) <- N0 * exp(r*t)
- N(t) <- 1320 * exp(0.0095218*4980)
**N(t) = 5.178388e+23**

The population size under exponential growth is significantly larger compared to logistic growth as it assumes no constraints on population growth. As logistic growth includes carrying capacity there are constraints to the population size which can be reached due to limiting resources - this can be applied to more real-world scenarios over longer time periods.


**Question 3:** 
- [comparing_exponential_and_logistic_growth.R](comparing_exponential_and_logistic_growth.R)
- ![plot of exponential and logistic curves](Rplot.png)
