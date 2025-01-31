We are polling station, $\hspace{0pt}485$ said Harris, $\hspace{0pt}515$ said Trump, what do I say about the result of the election? Do I trust this? Would I bet on it?
If we pick a person at random from Pennsylvania at random then they will have probability $p$ of saying (truthfully) that they will vote for Trump, where $p$ is the proportion of Trump voters in the state, so $p=\frac{N_\text{Trump}}{N}$, with $N$ being the total voters in the state, but this value of $p$ is unknown (we will assume people are telling the truth here)
If we choose $n$ random people (sample), then it is the same, each has probability $p$, provided the sample is small compared to the total population of voters $N$; $n\ll N$ 
## Probability vs Statistics
A typical probability question would involve telling you the probability $p$ and then having to calculate the probabilities of various configurations of $X_{1},\dots,X_{n}$. However, in statistics we want to go a step further: following a real world experiment, we would be told the results:
$$
X_{1}=x_{1},X_{2}=x_{2},\dots,X_{n}=x_{n}
$$
And then have to infer something meaningful about the unknown probability $p$. This is referred to as inference
## Statistical Inference
Think about what $p$ actually is:
real fixed with "true" value that is 
- just unknown (frequentist)
- an unknown quantity for which we should represent our subjective unceertainty about via a probability distribution (Bayesian/subjective)
## Totals and Samples Propotions as Estimators
First lets redefine $X$ to be the sum of all successes (values of 1) over the $n$ trials:
$$
X=\sum_{i=1}^{n}X_{i}
$$
With
$$
X_{i}=\begin{cases}
1&\text{if success}\\0&\text{if failure}
\end{cases}
$$
We want to estimate $p$, but first we want to examine the pmf for the set of Bernoulli trials $X_{1},\dots,X_{n}$. As the $X_{i}$'s are independent, we can just multiply their pmfs
$$
\implies f(x_{1},x_{2},\dots,x_{n}|p)=\prod_{i=1}^{n}f(x_{i}|p)=\prod_{i=1}^{n}p^{x_{i}}q^{1-x_{i}}
$$
$$
= p^{\prod_{i=1}^{n}x_{i}}q^{\prod_{i=1}^{n}(1-x_{i})}=p^{x}q^{n-x}
$$
Where
$$
x=\sum_{ i=1} ^{ n}  x_{i}
$$
Note this only depends on $p,n$ and $x$. This is a dramatic simplification of information, an example of dimensional reduction, data compression and sufficiency
Perhaps we should construct an estimator for $p$ using only $x$ and $n$? How about we ask what (proposed/estimated) value of $p$ would actually maximise the pmf $f(x_{1},\dots,x_{n}|p)$? Surely this will be good!
The trick is to maximise $\ln(f(x_{1},x_{2},\dots,x_{n}|p))$ as $\ln$ is monotonic, so maxima are the same (and it's easier to differentiate) so
$$
f(x_{1},x_{2},\dots,x_{n}|p)=p^{x}q^{n-x}
$$
$$
\implies \ln(f(x_{1},\dots,x_{n}|p))=x\ln p+(n-x)\ln(1-p)
$$
$$
\implies \frac{ \partial  }{ \partial p } \ln(f(x_{1},\dots,x_{n}|p))=\frac{x}{p}-\frac{n-x}{1-p}
$$
We set this equal to $\hspace{0pt}0$ to find our estimate $\hat{p}$
$$
\frac{x}{\hat{p}}- \frac{n-x}{1-\hat{p}}=0
$$
$$
\implies x(1-\hat{p})=(n-x)\hat{p}
$$
$$
\implies x=n\hat{p}
$$
$$
\implies \hat{p}=\frac{x}{n}
$$
So we have shown that a good estimator for the true $p$ is the sample proportion. This is a very intuitive/obvious result
We often dentote this as $Y$ and interms of random variables;
$$
\hat{p}=Y=\frac{X}{n}=\frac{1}{n}\sum_{i=1}^{n}X_{i}
$$
Note that $\hat{p} =Y$ is also the mean of the $X_{i}$'s but is $\hat{p}$ any good?