# Multiple Descent: Design Your Own Generalization Curve

### Preliminaries&#x20;

> Classical statistical learning theory supports a U-shaped curve of generalization versus model complexity -> #1. Introduction&#x20;
>
>
>
> 기본적으로 Generalization Error는 모델사이즈에 대해서 U자형태를 띈다 .       &#x20;



> the test error decreases again once model complexity grows beyond the interpolation threshold, resulting in the so called double-descent phenomenon  #1. Introduction&#x20;
>
>
>
> 딥러닝모델은 기본적으로  Double Descent 현상이 발생한다. &#x20;





### Key messages

> For a fixed family of models, a common way to select a model from this family is through empirical risk minimization   # 1. Introduction&#x20;
>
> \-> /

> Indeed, in this paper we show how to construct a model family for which the generalization curve can be fully controlled  # 1. Introduction&#x20;

> In this work, we study the multiple descent phenomenon by addressing the following questions
>
> * Can the existence of a multiple descent generalization curve be rigorously proven?&#x20;
> * Can an arbitrary number of descents occur?&#x20;
> * Can the generalization curve and the locations of descents be designed?



![n+8 까는 Underparametrized Regime으, Generalization Loss가 증가.](<../.gitbook/assets/image (1).png>)

### Underparameterized Regime&#x20;

> for the underparametrized regime, the generalization loss Ld is always non-decreasing as d grows

> in the underparametrized setting, the bias is always zero and as d approaches n, the variance keeps increasing.



### Overparameterized Regime

> One can create a descent (Ld+1 < Ld) by adding a Gaussian feature (Theorem 8)&#x20;

> create an ascent (Ld+1 > Ld) by adding a Gaussian mixture feature (Theorem 9)
