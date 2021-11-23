# Rate Distortion Theorem



{% hint style="info" %}
**Definition (distortion function)**

$$d : \mathcal{X} \times \mathcal{Y} \rightarrow \mathbb{R}$$ denote a distortion function. We define the corresponding distortion between two sequences $$x^n$$ and $$y^n$$ as&#x20;

&#x20;$$d^{(n)}(x^n, y^n) = \frac{1}{n} \sum_{i=1}^n d(x_i, y_i)$$​

This is the empirical average of distortion between the two sequences.
{% endhint %}

{% hint style="info" %}
**Definition (achievable rate-distortion pair) **

if and only if there exits a sequence of $$(n,R)$$ codes such that&#x20;

$$\lim_{n\rightarrow \infty} \mathbb{E}[d^{(n)} (X^n, g_n(f_n(X^n)))] \le D$$​

* $$R(D) = \min\{R:(R,D) \text{~is achievable}\}$$​
{% endhint %}

{% hint style="info" %}
**Theorem (Rate Distortion Theorem)**

For a given $$DMS(P_X)$$ and a distortion function $$d$$,

$$R(D) = \min_{\{P_{Y|X}: \mathbb{E}{P{Y|X}}[d(X,Y)] \le D\}} I(P_X, P_{Y|X})$$&#x20;

* **\[**:ballot\_box\_with\_check:**] :** $$\lim_{n\rightarrow \infty} \mathbb{E}[d^{(n)} [(X^n, Y^n) ] \le D$$​&#x20;
* Sufficient -> $$\exists (n,R)$$ codes $$R > R(D)$$ -> satisfy **\[**:ballot\_box\_with\_check:**]**
* Necessary -> $$R < R(D)$$ -> never satisfy **\[**:ballot\_box\_with\_check:**]**
{% endhint %}



