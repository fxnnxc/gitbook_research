# Greedy Algorithm

## Submodular Function

The submodular function $$f:2^V \rightarrow \mathbb{R}$$ has a property&#x20;

$$
f(A\cup \{i\} ) - f(A)  \ge f(B\cup \{i\} ) - f(B) 
     ~~~~~~~~~~~~~~(1)
$$

\
$$A\subset B \subset V$$and $$i\in V\B$$ $$i\in V\setminus B$$. That is, we have a **diminishing returns** for larger set.&#x20;

The marginal gain is:&#x20;

$$
\Delta (i|A) = f(A\cup \{i\} ) - f(A)
$$

​Hence the (1) becomes&#x20;

$$
\Delta (i|A)  \ge \Delta (i|B) ~~~~~~~~~~~~~~(2)
$$

## Monotone Submodular Function

A submodular function is monotone if $$f(A) \le f(B)$$ for any $$A\subset B$$.

## Maximization with Cardinality Constraint&#x20;

With a monotone submodular function $$f$$, our goal is to maximize $$f$$with a constraint that the cardinality of the set $$A$$ is bounded by some integer $$k$$. Since the function is monotone, it is clear that $$|A|=k$$​ because we loss anything by adding more elements.&#x20;

The formal definition of the maximization with cardinality constraint is:

$$
f(x) = x * e^{2 pi i \xi x}
$$

&#x20;Finding the optimal set of the problem is NP-hard problem. The greedy algorithm solves this problem by iteratively selects the element which gives the most utility by including it to the set. With empty set $$A_0$$, the algorithm repeats the following step for $$i=0,1,\cdots, k-1$$

$$
f(x) = x * e^{2 pi i \xi x}
$$

The algorithm guarantees to find the solution with&#x20;

$$f(A_k) \ge (1- \frac{1}{e}) f(A^*)$$​ where $$e$$ is the natural number and $$1-\frac{1}{e} \approx 0.63$$

## Proof of the Greedy Algorithm guarantee

{% hint style="info" %}
Let&#x20;

* $$f$$
* $$k$$
* $$A$$
* $$A$$
{% endhint %}

For all $$i\le k$$,&#x20;





We have $$\Delta(v_{i+1}|Ai) \ge \frac{1}{k} (f(A^*) - f(A_i))$$​

















### Reference&#x20;

\[1] [The greedy algorithm for monotone submodular maximization](https://homes.cs.washington.edu/\~marcotcr/blog/greedy-submodular/)
