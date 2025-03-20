## Known Variance
This is an example of a [[Conjugacy|conjugate]] [[Bayesian Statistics|prior]] for [[Normal Distribution|normally distributed]] data:
$$
X_{i}\sim N(\mu,\sigma^{2})
$$
With $\mu,\sigma^{2}$ both fixed. The conjugate prior family for the mean $\mu$ is also itself normal. We assume $\sigma^{2}$ is known and constant. To use the [[Variance|variance]] directly is a bit cumbersome, so instead, we work with the [[Precision|precision]], so let $\tau=\frac{1}{\sigma^{2}}$, then we can write
$$
X\sim N\left( \mu,\frac{1}{\tau} \right)
$$
And its pdf is
$$
f(x|\mu,\tau)=\sqrt{ \frac{\tau}{2\pi} }e^{ -\frac{\tau}{2}(x-\mu)^{2} }
$$
Let $X_{1},\dots,X_{n}$ be [[Independent and Identically Distributed|IID]] variables, with $X_{i}\sim N\left( \mu,\frac{1}{\tau} \right)$ with precision $\tau>0$ known.
Suppose our prior pdf for uncertain $\mu$ is:
$$
\mu \sim N\left( m,v^{2}=\frac{1}{t} \right),t>0
$$
Then our posterior pdf for $\mu|x$ is also Normal such that:
$$
\mu|\underline{x}\sim N\left( m_{1},v_{1}^{2}=\frac{1}{t_{1}} \right)
$$
Where $m_{1},v_{1},t_{1}$ are the updated ones:
$$
t_{1}=t+n\tau
$$
$$
m_{1}=\frac{tm+n\tau \bar{x}}{t+n\tau}
$$
We can re-write the posterior mean as:
$$
m_{1}=E(\mu|\underline{x})=\frac{t}{t_{1}}m+\frac{n\tau}{t_{1}}\bar{x}=km+(1-k)\bar{x}
$$
Where $k=\frac{t}{t+n\tau}$. Thus, again, the posterior mean is a weighted average of the prior mean $m$ and sample mean $\bar{x}=\frac{1}{n}\sum_{ i=1} ^{ n} x_{i}$ with weights proportional to the respective precisions.
The data precision is $n\tau$, which, if we just reintroduce $\sigma^{2}$, is just $\frac{n}{\sigma^{2}}=\frac{1}{\frac{\sigma^{2}}{n}}$ i.e. the precision of the sample mean $\bar{X}$, as we can recall from the [[Central Limit Theorem|CLT]]:
$$
\bar{X}\sim N\left( \mu,\frac{\sigma^{2}}{n} \right)
$$
Note each data point we observe increases our precision by $\tau$