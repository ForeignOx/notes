A [[Continuous Random Variables|continuous]] [[Random Variables|random variable]] $X$ is normally distributed with parameters $\mu,\sigma^{2}$, ($\mu,\sigma \in\mathbb{R},\sigma>0$) if the pdf is given by
$$
f(x)=\frac{1}{\sqrt{ 2\pi }\sigma}e^{ -\frac{(x-\mu^{2})}{2\sigma^{2}} }
$$
The curve follows a symmetric bell shape, with mean at the peak:
![[Pasted image 20241114183806.png]]
## Standard Normal
A random variable $Z$ is said to be a standard normal if it has the following pdf:
$$
\varphi(z)=\frac{1}{\sqrt{ 2\pi }}e^{ -z^{2}/2 }
$$
With $z\in\mathbb{R}$, and also have the following [[Cumulative Distribution Functions|cdf]]:
$$
\Phi(z)=\frac{1}{\sqrt{ 2\pi }}\int _{-\infty}^{x}e^{ -t^{2}/2 } \, dt 
$$
$Z$ is used to denote $N(0,1)$
### Converting
Let $X\sim N(\mu,\sigma^{2})$ and $Z\sim N(0,1)$, then 
$$
\frac{X-\mu}{\sigma}\sim N(0,1)
$$
$$
\mu+\sigma Z\sim N(\mu,\sigma^{2})
$$

#Mathematics #Probability #Definition 