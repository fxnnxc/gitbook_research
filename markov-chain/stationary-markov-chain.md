# Stationary Markov Chain

## Time-homogeneous Markov Chain

With the property

$$
\text{Pr}(X_{n+1} = x| X_n = y) = \text{Pr}(X_n = x| X_{n-1}=y)
$$

for all $$n$$. This means the probability distribution is independent of $$n$$.

{% hint style="info" %}
Usually Markov Chain has a time as a variable and time affects the probability. The Time-homogeneous Markov Chain doesn't depend on time.
{% endhint %}

## Stationary Distribution

We have a transition matrix  $$P_{ij}$$ , the probability to move to state $$x_j$$ from state $$x_i$$.

We have a distribution of the states $$\pi$$. The distribution of the next states is $$P\pi$$ (Matrix x Vector)

### Irreducible and reducible

* **Irreducible** :A Markov chain is irreducible if there is some integer k > 1 such that all the elements of Pk are nonzero.
* **Reducible** : there exists a state, once we visit it, there exists a non-reachable state

{% hint style="info" %}
**reducible example**

The fish is free to swim at any location as dictated by the currents, food, or presence of predators. Once the fish is caught in a net, it cannot escape and it has limited space where it can swim

**irreducible example**

Swimming fish in the ocean without caught.
{% endhint %}

![](<../.gitbook/assets/image (1).png>)

* (a) Irreducible: We can go anywhere starting from any state
* (b) Reducible: We can not go on of \[1,2,3] when we are at \[4,5]

**Source**: [https://link.springer.com/chapter/10.1007%2F978-0-387-74437-7\_5](https://link.springer.com/chapter/10.1007%2F978-0-387-74437-7\_5)

## Stationary Markov Chain

for all $$n$$ and $$k$$,

$$
\text{Pr}(X_0 = x_0, X_1 = x_1, \cdots, X_k =x_k) = \text{Pr}(X_n = x_0, X_{n+1} = x_1, \cdots, X_{n+k} =x_k)
$$

## Relationship between Time-homogeneous and Stationary properties.

* **Fact1**: Every stationary chain is time-homogeneous
* **Fact2**: When $$X_0$$ is a stationary distribution then, Time-homogeneous chain is stationary.
