# Zero-Order Optimization

Assume that we can have only the function values but cannot get gradients of $$f$$.

$$
f : \mathbb{R}^n \rightarrow \mathbb{R}
$$

These are the symbols we used in this post,&#x20;

* $$u\in \mathbb{R}^n$$: normally distributed Gaussian vector&#x20;
* $$\mu>0$$: positive value

## Gaussian Smoothing

At each point $$x\in \mathbb{R}^n$$, its _**Gaussian approximation**_ is&#x20;

$$
f_\mu(x) = \frac{1}{K}\int_{\mathbb{R}^n} f(x+\mu u) e^{-\frac{1}{2}||u||^2 } du
$$

where $$K = \int e^{\frac{1}{2} ||u||^2}  du$$

We sample many direction $$u$$ and average the value at the $$x+\mu u$$ position.&#x20;



$$
\begin{alignef_\mu(x) = \frac{1}{K}\int_{\mathbb{R}^n} f(x+\mu u) e^{-\frac{1}{2}||u||^2 } dud} 



\end{aligned}
$$



