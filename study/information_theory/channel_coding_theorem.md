# Channel Coding Theorem

The minimum achievable rate is $$C= \max_{P_X} I(P_X , W)$$. To be precise, if $$R< C$$, then $$R$$ is achievable, and if $$R>C$$, then it is not achievable.

### What is the meaning of achievable?

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
