# Stationary Markov Chain

## Time-homogeneous Markov Chain

With the property&#x20;

$$
\text{Pr}(X_{n+1} = x| X_n = y) = \text{Pr}(X_n = x| X_{n-1}=y)
$$
for all $$n$$. This means the probability distribution is independent of $$n$$. 

Ususally Markov Chain has  a time as a variable and time affects the probability. The Time-homogeneous Markov Chain doesn't depend on time. 

## Stationary Distribution

We have a transition matrix $$P = (P_{ij})$$ where $$P_{ij}$$ is the probability to move to state $$x_j$$ from state $$x_i$$. 

We have a distribution of the states $$\pi$$. The distribution of the next states is $$P\pi$$.

### Irreducible and reducible 

* Irreducible : When there is a positive probability for each transition from $$i$$ to $$j$$. 
* 

## Stationary Markov Chain


for all $$n$$ and $$k$$,

$$
\text{Pr}(X_0 = x_0, X_1 = x_1, \cdots, X_k =x_k) = \text{Pr}(X_n = x_0, X_{n+1} = x_1, \cdots, X_{n+k} =x_k)
$$




## Relationship between Time-homogeneous and Stationary properties. 

* Fact1: Every stationary chain is time-homogeneous 
* Fact2: When $$X_0$$ is a stationary distribution then, Time-homogeneous chain is stationary. 


