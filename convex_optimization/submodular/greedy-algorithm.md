# \[2.2.1] Greedy Algorithm \[Proof]

## Submodular Function

The submodular function $$f:2^V \rightarrow \mathbb{R}$$ has a property

$$
f(A\cup \{i\} ) - f(A) \ge f(B\cup \{i\} ) - f(B) ~~~~~~~~~~~~~~(1)
$$

\
$$A\subset B \subset V$$and  $$i\in V\setminus B$$. That is, we have a **diminishing returns** for larger set.

The marginal gain is:

$$
\Delta (i|A) = f(A\cup \{i\} ) - f(A)
$$

​Hence the (1) becomes

$$
\Delta (i|A) \ge \Delta (i|B) ~~~~~~~~~~~~~~(2)
$$

## Monotone Submodular Function

A submodular function is monotone if for any $$A,B$$ with $$A\subset B$$

$$
f(A) \le f(B)~~~~~~~~~~~~(2.1)
$$

## Maximization with Cardinality Constraint

With a monotone submodular function $$f$$, our goal is to maximize $$f$$with a constraint that the cardinality of the set $$A$$ is bounded by some integer $$k$$. Since the function is monotone, it is clear that $$|A|=k$$​ because we loss anything by adding more elements.

The formal definition of **the maximization with cardinality constraint** is:

$$
A^* = \arg\max_{A\subset V, |A|\le k} f(A) ~~~~~~~~~ (3)
$$

Finding the optimal set of the problem is NP-hard problem. The greedy algorithm solves this problem by iteratively selects the element which gives the most utility by including it to the set. With empty set $$A_0$$, the algorithm repeats the following step for $$i=0,1,\cdots, k-1$$

$$
A_{i+1} = A_i \cup \{ \arg\max_{v\in V\setminus A_i} f(A_i\cup \{v\}) \} ~~~~~~ (4)
$$

**The algorithm guarantees to find the solution with**

$$f(A_k) \ge (1- \frac{1}{e}) f(A^*)$$​ where $$e$$ is the natural number and $$1-\frac{1}{e} \approx 0.63$$

## Proof of the Greedy Algorithm guarantee

{% hint style="info" %}
Let

* $$f$$ be a monotone submodular function with $$f\ge0$$​
* $$k$$ be a integer such that $$k\le |V|$$
*   $$A_i = (v_1, v_2, \cdots, v_i)$$ be the chain formed by the greedy algorithm&#x20;

    with the property the Equation (4)
* $$A^* =(v_1^*, v_2^*, \cdots, v_k^*)$$ be the optimal solution which satisfies the Equation (3)
{% endhint %}

For all $$i\le k$$,

$$
\begin{aligned} f(A^*) &\le f(A^* \cup A_i) ~~~~~\text{From}~ (2.1) \\ &= f(A_i) - \Big[f(A_i) - f(A_i\cup\{v_1^*\})\Big] - \Big[f(A_i\cup\{v_1^*\}) - f(A_i\cup\{v_1^*, v_2^*\})\Big] \\&~~~~~~- \cdots - \Big[f(A_i\cup\{v_1^*,\cdots, v_{k-1}^*\}) - f(A_i\cup\{v_1^*,\cdots , v_k^*\})\Big]\\ &= f(A_i) + \sum_{j=1}^k \Delta (v_j^*| A_i \cup \{v_1^*, c\dots, v_{j-1}^* \})\\ &\le f(A_i) + \sum_{j=1}^k \Delta(v_j^*|A_i) ~~~~~~~\text{From}~(2) \\ &\le f(A_i) + \sum_{j=1}^k \Delta(v_{i+1}|A_i) ~~~~~\text{From}~ (4) \\&=f(A_i) + k \Delta(v_{i+1}|A_i) \end{aligned}
$$

Now we have $$\Delta(v_{i+1}|A_i) \ge \frac{1}{k} (f(A^*) - f(A_i))$$​.

Since $$\Delta(v_{i+1}|A_i) = f(A_{i+1})- f(A_i)$$, by rearranging this term, we have

$$
f(A^*) - f(A_{i+1}) \le (1- \frac{1}{k}) (f(A^*) - f(A_{i}))
$$

which means that, the gap between the utility achieved by the optimal solution and the greedy algorithm is increased by  $$(1-\frac{1}{k})$$​.&#x20;

{% hint style="info" %}
Consider k=1,&#x20;

the greedy algorithm has no error at all

Consider k=2,&#x20;

the greedy algorithm selects the best one first, and the second error becomes less than &#x20;

$$(1-1/2) = 1/2$$ factor
{% endhint %}

and iteratively, we have

$$
\begin{aligned}
f(A^*) - f(A_{k}) &\le (1- \frac{1}{k}) (f(A^*) - f(A_{k-1})) \\
&\le (1- \frac{1}{k})^2 (f(A^*) - f(A_{k-2}))  \\
&\le \vdots \\
&\le (1- \frac{1}{k})^k (f(A^*) - f(A_{0})) \\
&\le (1- \frac{1}{k})^k f(A^*) \\
&\le  \frac{1}{e} f(A^*) ~~~~~~~~~~~~~~~~~~~~~~~~~~ (\because (1-x) \le 
e^{-x}) \end{aligned}
$$


$$\therefore f(A_{k}) \ge \Big( 1 - \frac{1}{e} \Big) f(A^*)$$​.

## References

\[1] [The greedy algorithm for monotone submodular maximization](https://homes.cs.washington.edu/\~marcotcr/blog/greedy-submodular/)



**You can contact me via**

* bumjin@kaist.ac.kr&#x20;
* [https://open.kakao.com/me/fxnnxc](https://open.kakao.com/me/fxnnxc)



