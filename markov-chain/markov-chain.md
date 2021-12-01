# Markov Chain

The probability of moving to the next state **depends only on the present state** and not on the previous state.&#x20;

$$
\ Pr(X_{n+1}  =x |
$$

* where $$X_i$$ is a random variable form the sequence $$(X_1, X_2, \cdots, X_n)$$
* To define the Markov Chain we need a state space \$$\mathcal{X}=\\{\text{all possible states} \\}

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
