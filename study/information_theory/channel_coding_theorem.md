# Channel Coding Theorem

In this page, we'll study the channel coding theorem.

> **Thm. (Channel Coding Theorem)** The minimum achievable rate is $$C= \max_{P_X} I(P_X , W)$$. To be precise, if $$R< C$$, then $$R$$ is achievable, and if $$R>C$$, then it is not achievable.

### What is given?

{% tabs %}
{% tab title="Given!" %}
* The fixed length of n
* The fixed rate R
* The channel W = p\_{Y|X}
* The channel capacity C = max_{p|X} I(P_\_X, W)&#x20;
{% endtab %}
{% endtabs %}

#### Background&#x20;

* What is (n, R) codes
* Fanno's inequality
* Data processing inequality&#x20;

{% tabs %}
{% tab title="(n, R) codes" %}

{% endtab %}

{% tab title="Fanno's inequality" %}

{% endtab %}

{% tab title="Data Processing inequality" %}

{% endtab %}
{% endtabs %}

### :pen\_fountain: What is the meaning of achievable?

$$R$$ is achievable means that the error probability goes to zero with the rate $$R$$.

We are given, fixed $$(n, R)$$ codes.

$$
P_{e,m}^{(n)} = \text{Pr}(g_n(y^n)) \ne m| x^n(m))
$$

and the maximum error probability is&#x20;

$$P_{e, \text{max}}^{(n)} = \max_m P_{e,m}^{(n)}$$&#x20;

We say a rate $$R$$ is achievable if there exists, a sequence of $$(n, R)$$ codes such that $$P_{e, \text{max}}^{(n)} \rightarrow 0$$

Therefore with _achievable rate_, we can construct $$(n, R)$$ codes such that the maximum error goes to zero as $$n$$ goes to the infinity.

$$
\begin{aligned} nR = H(M) &= H(M|Y^n) + I(M;Y^n)\\ &= H(M|Y^n) + I(X^n(M); Y^n) ~~ \text{data processing inequality}\\ &= \log{2} + P_e^{(n)} nR + I(X^n(M);Y^n) ~~ \text{Fano's inequality}\\ &= \log{2} + P_e^{(n)}nR + nC ~~\text{By the definition of } C \end{aligned}
$$

Therefore we have,

$$
P_n^{(n)} \ge 1- \frac{C}{R} - \frac{1}{nR}
$$

### :white\_check\_mark: Meaning of the Channel Coding Theorem



