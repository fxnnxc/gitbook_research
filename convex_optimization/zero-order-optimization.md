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

Let $$ y = x+ \mu u $$. Then, $$dy = \mu^n du$$  

This is becuase  $$(dy_1, dy_2, \cdots, dy_n) = |det(D_g)| (du_1, du_2, \cdots, dy_n)$$

where $$D_g$$ is the jacobian matrix of the relateion $$y = g(u)$$

https://en.wikipedia.org/wiki/Integration_by_substitution

Therefore, We have 

$$
\begin{aligned}
f_\mu(x) &= \frac{1}{K}\int_{\mathbb{R}^n} f(x+\mu u) e^{-\frac{1}{2}||u||^2 } du \\ 
&=  \frac{1}{\mu^n K} \int f(y) e^{-\frac{1}{2\mu^2} ||y-x||^2} dy 
\end{aligned}
$$


we can compute the derivate of $$f_\mu(x)$$ w.r.t. $$x$$. 

$$
\begin{aligned}
\nabla f_\mu(x) &=  \nabla  \frac{1}{\mu^n K} \int f(y) e^{-\frac{1}{2\mu^2} ||y-x||^2} dy \\
&= \frac{1}{\mu^n K} \int f(y) \frac{y-x}{\mu^2} e^{-\frac{1}{2\mu^2}||y-x||^2 } dy \\
&= \frac{1}{K} \int f(x+\mu u) \frac{u}{\mu} e^{-\frac{1}{2}||u||^2} du \\
&= \mathbb{E}_u \Big[ \frac{f(x +\mu u)}{\mu} u \Big] = \mathbb{E}_u \Big[ \frac{f(x + \mu u) - f(x) }{\mu} u \Big] ~~ \text{(one-point)}
&= \mathbb{E}_u \Big[ \frac{f(x +\mu u) - f(x- \mu u)}{2\mu} u \Big]  ~~ \text{(two-point)}
\end{aligned}
$$








