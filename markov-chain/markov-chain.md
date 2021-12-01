# Markov Chain

The probability of moving to the next state **depends only on the present state** and not on the previous state.&#x20;

* To define the Markov Chain we need a state space \$$\mathcal{X}=\\{\text{all possible states} \\}
* Assume that we are at the timestep $$t=n$$
* We have a transition history $$X_1 = x_1, X_2 = x_2, \cdots, X_n = x_n$$ 
* $$X_i$$ is a random variable and $$x_i$$ is a realization of the random variable. 

$$
\begin{aligned}
 \text{Pr}(X_{n+1}  &=x | \text{previos history}) = \text{Pr}(X_{n+1}  =x | X_1 = x_1, X_2 = x_2, \cdots, X_n = x_n) \\ 
 &=\text{Pr}(X_{n+1}=x | X_n =x_n)
\end{aligned}
$$

### Example

![](../.gitbook/assets/image.png)

Consider the internet web pages.  You may navigate several pages but the transition probability to the next page is only depends on the current page.

1. Assume that you are at **Page A**
2. You can go to **page D** and **page C**. With some probability.&#x20;
3. This probability depends only on the page A. We don't consider the previous history.&#x20;

{% hint style="info" %}
This hypothesis doesn't match the true situation because in most cases we select page depends not only the current page but also the previous history.&#x20;
{% endhint %}

Source: [https://en.wikipedia.org/wiki/Markov\_chain](https://en.wikipedia.org/wiki/Markov\_chain)
