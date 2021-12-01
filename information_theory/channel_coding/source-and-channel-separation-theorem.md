# \[1.2.3] Source and Channel Separation Theorem

These are some underlying circumstances.&#x20;

1. We have a **source of a length-**$$n$$ **sequence** $$V^n$$ with i.i.d. symbols following the distribution $$P_V$$
2. We use a $$\text{DMC}(W)$$​with input alphabet $$\mathcal{X}$$ and output alphabet $$\mathcal{Y}$$to transmit $$V^n$$
3. We use the channel total $$n$$-times to transmit the source sequence $$V^n$$
4. We reconstruct $$\hat{V}^n$$ from $$Y^n$$

{% hint style="info" %}
**Obvious Solution to the Channel Coding** (when $$H(P_V)\le C$$)

1. Lossless source coding on $$\text{DMS}(P_v)$$ to reduce $$n$$symbols to $$nR$$ bits.&#x20;
2. Channel coding to reliably transmit those $$nR$$ bits.&#x20;
3. Transmit and recover the bits.&#x20;



****:grimacing: **Channel Coding: identity**

1. We have $$V^n$$, directly maps $$V^n \rightarrow X^n$$&#x20;
2. get the channel output $$Y^n$$ and decode it&#x20;
{% endhint %}









