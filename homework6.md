## Homework 6
### Akash 

### Problem 1

To calculate being  covid positive given the pool tested positive, we need to understand bayesian statistics.

so let's start with the baye's theorem,

   $P(A/B) = \frac{P(B/A) P(A)}{P(B)}$
   
Here we can think of 

* $P(A/B)$ as probability of being positive given the pool is positive.
* A is a statement saying the individual is covid-19 positive. 
* B is a statement saying pool tested positive. 
* $P(B)$ says the probability of pool being positive.
* $P(A)$ says the probability of the individual being positive.
* $P(B/A)$ says the given the individual is positive, chances of pool being positive.

There are also ways to think of it interms of the prior, likelyhood and posterior as well.

Here, we can calculate $P(B/A)$ which says given that I am covid positive what are the chances of pool being positive as well.Over here I will add some data to it to calculate the probabiltiy. currently saliva test is being done at the university, whose accuracy is 83%, also in the pool i don't know how many people are being tested in a single pool, there are 12 people in the pool so i am going to assume that two people are being tested. so am I going to get tested or not has 1 in 12 chances. also if I get then the chances of me giving positive is 83%. Hence $P(B/A) = \left(1 /12 \right) (0.83) = 0.069$.  One more thing to notice is I didn't account the information were other people in the pool could be positive. 

Now for $P(B)$, since there is no data on it, we will write it in terms of $P(B) = P(B/A)P(A) + P(B/A')P(A')$. here $P(A)$ is the probability of the given person is infected which in the errie county is 11%. while $P(A')$ would be $1 - P(A)$. while $P(B/A')$ can be calculated using the binomial distribution. it tells us the probability of getting the positive pool given i am not positive,  it also means there could be somebody else in the pool who is positive.  

Now for the $P(A)$, the individual is positive given he has tested is 11%.  

In the end after doing the final calculation we got the result, which says the chances of me getting the positive result given the pool is positive, is around 1.11%, which is comparitively very low. I am not sure if that is correct.


### Problem 2

In this problem i have mostly followed the example notebook. foloowing are the references.

### References

Blog :  https://blog.tensorflow.org/2019/03/structural-time-series-modeling-in.html

Example file : https://github.com/tensorflow/probability/blob/master/tensorflow_probability/examples/jupyter_notebooks/Structural_Time_Series_Modeling_Case_Studies_Atmospheric_CO2_and_Electricity_Demand.ipynb
