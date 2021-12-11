# Information-theoretic Limits

What is the information-theoretic Limits?

It is an important issue for many data scientist.&#x20;

### :heavy\_check\_mark:Preliminaries&#x20;

**Two important inequalities**&#x20;

{% tabs %}
{% tab title="Fano's inequalities" %}
$$H(X|Y) \le \log 2 + P_e \cdot \log (|\mathcal{X}| -1 )$$
{% endtab %}

{% tab title="Data Processing Ineqaulity " %}
If $$X\rightarrow Y \rightarrow Z$$.

$$I(X;Y) \ge I(X;Z)$$ with equality iff $$I(X;Y|Z) = 0$$ or equivalently, $$X\rightarrow Z \rightarrow Y$$
{% endtab %}
{% endtabs %}

**Detection of a single hidden community**  given information $$\mathcal{G}(n, s, p, q)$$

There are two communities $$C$$ and $$B$$.

* $$n$$: number of nodes
* $$s$$: number of nodes in a community $$C$$
* $$p$$: the probability of a pair of nodes in community $$C$$
* $$q$$: other pairs of nodes. ($$B-B$$ and $$C-B$$ community pairs)

****:star:**Goal: Recover** $$s$$ **nodes in community** $$A$$**, given the edge data.** &#x20;

### Information-theoretic limit&#x20;

Question: when is the recovery possible?

* Let the community $$C \subset [n]$$ be uniformly drawn from all subsets of $$[n]$$ of cardinality $$s$$.
* Observation: the adjacency matrix $$A$$, $$A_{ij} \sim Bern(p)$$if $$i,j \in C$$ and $$Bern(q)$$ otherwise.&#x20;
* Goal: recover the hidden community $$C$$ almost perfectly, i.e., achieving $$\mathbb{E}[|\hat C \Delta C|] = o(s)$$
  * $$\hat C \Delta C = (\hat C - C) \cup (C -\hat C)$$
  * $$o(s)$$ :  increasing slower than linear . $$o(s) = \sqrt(s), o(s) = \log s, o(s) \ne ks$$

#### (Converse) Information-theoretic limits&#x20;

{% hint style="info" %}
(Theorem)\
To guarantee $$\mathbb{E}[|\hat C \Delta C|] = o(s)$$, it is necessary to have\
$$s \cdot D_B(p||q) \rightarrow \infty$$ and $$\lim \inf_{n \rightarrow \infty} \frac{s DB (p||q)}{\log \frac{n}{s}} \ge 2$$
{% endhint %}

Proof&#x20;







### Upper bound of Mutual Information&#x20;

{% hint style="info" %}
(Theorem) Golden formula



For $$\forall Q_Y$$ such that $$D(PY|| QY) < \infty$$, \
$$I(X;Y) = \mathbb{E}{Px} [ D(P{Y|X} | QY)] - D(PY ||QY)$$.\
\
Corollary (Upper bound on the mutual information) \
\
For all \forall Q_Y such that D(P_Y ||Q_Y) \le \infty_ \
_I(X;Y) \le \mathbb{E}\_{P\_X} \[ D(P\_{Y|X} || Q\_Y )]_

__
{% endhint %}































### Update&#x20;

\[2021.12.11] Make the script

