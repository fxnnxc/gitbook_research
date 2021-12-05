# Metropolis-Hastings Algorithm

Markov chain Monte Carlo method for obtaining a sequence of random samples from a probability  distribution from which direct sampling is difficult. 


Let $$f(x)$$ be a function that is proportional to the desired probability density function $$P(x)$$ 

## Steps 

1. Initialization 
2. Generate a candidate $$x^'$$ for the next sample by picking from the distribution $$g(x^' | x_t)$$
3. Calculate the acceptance ratio $$\alpha = f(x')/f(x)$$ which will be used to decide whether to accept or reject the candidate. 
4. Accept or Reject
   1. Generate a uniform random number $$u\in [0,1]$$ 
   2. If $$u \le \alpha$$, then accept the candidate by setting $$x_{t+1} = x'$$ 
   3. If $$u > \alpha$$, then reject the candidate and set $$x_{t+1} = x_t$$ 

## 1. Initialization 

Let $$g(x|y)$$ be an arbitrary probability density for the next sample value $$x$$, given the previous sample value $$y$$. Also $$g$$ is assumed to be symmetric, $$g(x|y) = g(y|x)$$. A usual choise to let $$g(x|y)$$ be a Gaussian distribution centered at $$y$$, so that the closer points to $$y$$ are likely to visited more. 
Let $$f(x)$$ be a function that is proportional to the desired probability density $$P(x)$$. 

## 2. Generate a sample 

 Generate a candidate $$x^'$$ for the next sample by picking from the distribution $$g(x'|x_t)$$. 

## 3. Accept or Reject

By using $$f$$, calculate the acceptance ratio $$f(x')/f(x)$$. 


* Accept: If $$u \le \alpha$$, then accept the candidate by setting $$x_{t+1} = x'$$ 
* Reject: If $$u > \alpha$$, then reject the candidate and set $$x_{t+1} = x_t$$ 

Therefore, if the newly generated sample has higher probability than the previos one, it is more likely to be accepted. 
However, even though the probability of the newly generated sample has lower probability, it can be chosen with low probability. 





# Reference 
* https://en.wikipedia.org/wiki/Metropolis%E2%80%93Hastings_algorithm
* https://people.duke.edu/~kh269/teaching/notes/MetropolisExplanation.pdf