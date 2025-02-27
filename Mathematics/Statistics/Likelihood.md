We imagine that we will gather data $X_{i}$ with $i=1,2,\dots,n$. Now we may not know the precise distribution that generated this data, but we may suspect that the distribugtion is one of a family of possible distributions laelled on parameterised by a parameter $\theta$ ($\theta$ could even represent a list of parameters). An example of this is saying $X_{i}\sim \text{Bernoulli}(p)$, here $\theta=p$. We also often wee $X_{i}\sim N(\mu,\sigma^{2})$, here $\theta=\left\{ \mu,\sigma \right\}$
The joint pdf of the data is simply represented as:
$$
f(x_{1},x_{2},\dots,x_{n}|\theta)
$$
However, once we measure the data:
$$
X_{1}=x_{1},X_{2}=x_{2},\dots,X_{n}=x_{n}
$$
This joint pdf can now be viewed as just a function of $\theta$ as the data are now fixed
## The Likelihood Function
Suppose we have $X_{1},\dots,X_{n}$ that have joint pdf $f(x_{1},x_{2},\dots,x_{n}|\theta)$, then the likelihood function $\mathcal{L}(\theta)$ is simply the pdf of the observed data considered as a function of $\theta$ only i.e.
$$
\mathcal{L}(\theta)\equiv\mathcal{L}(\theta;x_{1},\dots,x_{n})=f(x_{1},\dots,x_{n}|\theta)
$$
And the log-likelihood function is:
$$
\mathscr{L}(\theta)\equiv \log(\mathcal{L}(\theta))=\log(f(x_{1},x_{2},\dots,x_{n}|\theta))
$$
___
## Likelihood for [[Independent and Identically Distributed|IID]] data
If the $X_{i}$ are independent and identically distrubuted (IID), then the expression for the likelihood takes a more pleasant form. Suppose each $X_{i}$ has pdf given by $f(x_{i}|\theta)$ and that all $X_{i}$ are IID then
$$
\mathcal{L}(\theta)=f(x_{1},x_{2},\dots x_{n}|\theta)=\prod_{i=1}^{n}f(x_{i}|\theta)
$$
$$
\mathscr{L}(\theta)=\log(f(x_{1},\dots x_{n}|\theta))=\log\left( \prod_{i=1}^{n}f(x_{i}|\theta) \right)=\sum_{i=1}^{n}\log(f(x_{i}|\theta))
$$
This is useful as we can differentiate sums much more easily than products
Note that $\mathcal{L}(\theta)$ is not a probability density function with respect to $\theta$, as $\theta$ is just a fixed but unknown parameter (at this point), so $\mathcal{L}(\theta)$ will not integrate to $1$ with respect to $\theta$
However, $\mathcal{L}(\theta)$ is still really useful as it shows us which values of $\theta$ are more likely to have generated the data 
### For Bernoulli
Likeihood for Bernoulli trials. say we have IID
$$
X_{i}\sim \text{Bernoulli}(p)
$$
So each $X_{i}$ is discrete and equal to $1$ or $0$ with probability $p$ or $1-p=q$, hence
$$
f(x_{i}|p)=\begin{cases}
p^{x_{i}}q^{1-x_{i}}&\text{for }x_{i}=0,1\\0&\text{otherwise}
\end{cases}
$$
Hence our parameter of interest is $\theta=p$, so we write our likelihood as $\mathcal{L}(p)$ instead of $\mathcal{L}(\theta)$:
$$
\mathcal{L}(p)=f(x_{1},\dots,x_{n}|p)=\prod_{i=1}^{n}f(x_{i}|p)=\prod_{i=1}^{n}p^{x_{i}}q^{1-x_{i}}=p^{\sum_{i=1}^{n}x_{i}}q^{\sum_{i=1}^{n}1-x_{i}}=p^{x}q^{n-x}
$$
Where $x=\sum_{ i=1} ^{ n} x_{i}$, and
$$
\mathscr{L}(p)=\log(\mathcal{L}(p))=\log(p^{x}q^{n-x})=x\log(p)+(n-x)\log(1-p)
$$
Which we can now maximise by differentiating to find an estimator for $p$ 
### For Binomial
In a binomial scenario, we have that $X$ is the sum or count of the successes from $n$ Bernoulli trials with parameter $p$, so
$$
X\sim \text{Bin}(n,p)
$$
When viewed in this binomial framework, we have one single experiment, that yields the realisation $X=x$
Hence due to a single experiment, the likelyhood is simply ($n$ is known)
$$
\mathcal{L}(p)=f(x|p)={n \choose x }p^{x}q^{n-x}
$$
And the log-likelyhood is:
$$
\mathscr{L}(p)=\log(f(x|p))=\log\left( {n \choose x }p^{x}q^{n-x} \right)=\log\left( \frac{n!}{(n-x)!x!} \right)+x\log(p)+(n-x)\log(1-p)
$$
Note that differentiating this with respect to $p$ gives an identical result as with the bernoulli trials, since their log-likelihoods differ only by a constant