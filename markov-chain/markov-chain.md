# Markov Chain

## Preliminary

The probability of moving to the next state **depends only on the present state** and not on the previous state.

* **State space** $$\mathcal{X}=\{\text{all possible states} \}$$ (we need it to define the Markov Chain! )
* Assume that we are at the time $$t=n$$
* We have a transition history $$(X_1 = x_1, X_2 = x_2, \cdots, X_n = x_n)$$
* $$X_i$$ is a random variable and $$x_i$$ is a realization of the random variable.

## Markov Property

$$
\begin{aligned} \text{Pr}(X_{n+1} =x | \text{transition history}) &= \text{Pr}(X_{n+1} =x | X_1 = x_1, X_2 = x_2, \cdots, X_n = x_n) \\ &=\text{Pr}(X_{n+1}=x | X_n =x_n) \end{aligned}
$$

{% hint style="info" %}
It means the probability solely depends on the current state.&#x20;

Therefore, when you compute the transition probability $$\text{Pr}(X{n+1} = x_{n+1})$$, you can consider only the current state. **It has same result with the probability that you compute the probability conditioned on the full history** (which will be quite long!) :grin:
{% endhint %}

## Markov Chain

_**Markov Chain** _ is a sequence of random variables $$(X_1, X_2, \cdots, X_n)$$ with the **Markov property**.

### Example

![](../.gitbook/assets/image.png)

Consider the internet web pages. You may navigate several pages but the transition probability to the next page is only depends on the current page.

1. Assume that you are at **Page A**
2. You can go to **page D** and **page C**. With some probability.
3. This probability depends only on the page A. We don't consider the previous history.

{% hint style="info" %}
This hypothesis doesn't match the true situation because in most cases we select page depends not only the current page but also the previous history.
{% endhint %}

Source: [https://en.wikipedia.org/wiki/Markov\_chain](https://en.wikipedia.org/wiki/Markov\_chain)
