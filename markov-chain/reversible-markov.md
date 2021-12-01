# Reversible Markov

When the joint probability is same with inverse order. 

$$
\text{Pr}(X_0=x_0, X_1=x_1, \cdots, X_n=x_n) = \text{Pr}(X_0=x_n, X_1=x_{n-1}, \cdots, X_n=x_0)  
$$ 

or equivalently, 

$$ 
\pi_{x_0} P_{x_0x_1} P_{x_1x_2} \cdots P_{x_{n-1}x_n} = \pi_{x_n} P_{x_nx_{n-1}} P_{x_{n-1}x_{n-2}} \cdots P_{x_{1}x_0}
$$


## Detailed Balance 

$$
\text{Pr}(X_0 = x_0, X_1, = x_1)  = \text{Pr}(X_0 = x_1, X_1, = x_0) 
$$


## Theorem 1

$$ 
\pi, P \text{satisfy detailed balance if and only if the Markov chain is reversible}
$

## Theorem 2 

$$
\text{If} \pi, P \text{satisfy detailed balance, then } \pi \text{is a stationary distribution}
$$

This is due to $$\pi_x = \pi_y P_{yx} = \pi_x P_{xy} \Rgitarrow \pi = \pi P$$