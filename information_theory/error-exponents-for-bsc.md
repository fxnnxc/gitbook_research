# Error Exponents for BSC

## 1. Setup

* consider $$\text{BSC}(\epsilon)$$ with $$\epsilon <1/2$$
* consider an i.i.d. $$\text{Bernoulli}(1/2)$$ rnadom code, with $$M= 2^{nR}$$ codewords.
* we choose message $$m$$ and transmit $$X^n(m)$$ and receives $$Y^n$$.

## 2. What we want

Given the ouptput $$Y^n$$, we should choose the correct $$m$$ among $$1,2, \cdots, 2^{nR}$$ messages. However, the orginal message $$X^n(m)$$ is perturbed by the BSC channel and we want to analyse an error.

Note that the error decreases exponentially as $$n$$ increases and the exponential term depends on epsilon.

## 3. Methods

### Output Centered Analysis

$$
X^n(m) = X^n(m) \oplus Y^n
$$

where $$\oplus$$ dentoes binary addition (XOR).

With XOR operator, we just have to find the message which achieves minimum magnitude

$$
\hat m = \arg\min_m |\hat X^n(m)|
$$

W.L.O.G, we assume that $$X^n(1)$$ is the original message. We have the following properties

* $$\hat X^n (1) = X^n(1) \oplus Y^n$$ is a sequence with i.i.d. $$\text{Bernoulli}(\epsilon)$$ symbols
* For all $$m=2,3,\cdots, M,$$, $$\hat M^n(m) is a length-$$n$$sequence with i.i.d.$$\text{Bernoulli}(1/2)\$$ symbols
* All $$\hat{X}^n(m)$$ are independent of each other

Note that $$\text{Bernoulli}(1/2)$$ comes from the set up. Because 0 and 1 are distributed randomly with equal probability, the distribution after applying BSC channel is same.

Now we have the following properties

* $$|\hat{X}^n (1)| = n \epsilon$$
* $$|\hat{X}^n (m)| = n \frac{1}{2}$$, $$m \ne 1$$.

Remark: when $$\epsilon = 1/2$$ we cannot distinguish the orginal message and others. On the other hand, we can easily find the orginal message as much as it is smaller than $$1/2$$.

### Error Types

We consider two types of errors. For a given $$\gamma \in (\epsilon, 1/2)$$

1. The orginal message changed more than $$n\gamma$$.
2. There is other code words $$m \ne 1$$such that $$|\hat X^n (m)|$$ is smaller $$n\gamma$$.

We can compute $$Pr(\mathcal{E}_\gamma)$$ easily by independence.

$$
\mathrm{Pr}(\mathcal{E}_\gamma) \overset{\cdot}{\le} 2^{-n E(\gamma)}
$$

where \$$E(\gamma) = D(\gamma || \epsilon) + \[D(\gamma||1/2) - R]^{+}

The overall error probability is dominate by the smallest one.

$$
P_e = \mathrm{Pr}\Big( \cup_\gamma \mathcal{E}_\gamma \Big) \overset{\cdot}{=} 2^{-\min_\gamma E(\gamma)}
$$

where $$E_\gamma (R) = \min_{\gamma \in \epsilon, 1/2)} (D(\gamma||\epsilon)+ [D(\gamma||1/2) -R]^+)$$

Remark

### Exponential Term analysis

It is clear that when there are less messages, we can easily find the original message. Therefore, the error term is a decreasing function of the ratio. Also, for given rate $$R$$ there is appropriate gamma $$\gamma_{GV}(R)$$ such that $$D_B(\gamma_{GV}(R)||1/2) = R$$.

First, let $$\gamma_{crit} = \arg \min_\gamma [D(\gamma||\epsilon) + D(\gamma ||1/2)]$$

We can compute it exactly, $$\gamma_{critc} = \frac{\sqrt{\epsilon}}{\sqrt{\epsilon} + \sqrt{1 -\epsilon}}$$

![](<../.gitbook/assets/image (3).png>)

#### Case1: $$\gamma_{crit} < \gamma_{GV}(R)$$

In this case, $$D_B(\gamma_{GV}(R)||1/2) > R$$ and $$E_\gamma (R) = \min_{\gamma \in \epsilon, 1/2)} (D(\gamma||\epsilon)+ D(\gamma||1/2) -R)$$

$$E_\gamma (R) = \log 2 - \log(1 + 2 \sqrt{\epsilon (1- \epsilon)}) -R$$

It is a linear function of $$R$$.

#### Case2: $$\gamma_{crit} > \gamma_{GV}(R)$$

In this case, $$D_B(\gamma_{GV}(R)||1/2) < R$$ and $$E_\gamma (R) = \min_{\gamma \in \epsilon, 1/2)} D(\gamma||\epsilon)$$$$D_B(\gamma_{GV}(R)||1/2) < R$$ and $$E_\gamma (R) = D(\gamma||\epsilon)$$

![](<../.gitbook/assets/image (2).png>)



\---
