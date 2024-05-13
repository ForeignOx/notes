The geometric distribution counts the number of trials for the first success to occur, it is defined like so:
$$
X\sim Geo(p)\iff P(X=r)=(1-p)^{r-1}p
$$
This is related to the [[Binomial Distribution|binomial distribution]] as it has:
- a probability of success that is the same on each trial ($p$)
- the outcome of each trial is independent of any other trial
- each trial has exactly two outcomes (success or failure)
___
## Check it is a probability distribution
For it to be a probability distribution, the sum of all probabilities must be 1
$$
\sum_{r=1}^\infty P(X=r)=\sum_{r=1}^\infty(1-p)^{r-1}p
$$
This is a [[Geometric Progressions|geometric progression]] with $a=p$, $r=1-p$, since $p$ is a probability, $|1-p|<1$ so
$$
\sum_{r=1}^\infty P(X=r)=\frac{p}{1-(1-p)}=\frac{p}{p}=1
$$
So it is a probability distribution.
___
## $P(X\leq r)$
$$
P(X\leq r)=P(X=1)+P(X=2)+\dots+P(X=r)
$$
Let $q=1-p$
$$
=p+pq+pq^{2}+\dots+pq^{r-1}
$$
This is a [[Geometric Distribution|geometric sum]]
$$
=\frac{p(1-q^r)}{1-q}=1-q^r
$$
___
## $P(X>r)$
$P(X>r)$ is saying that we need more than $r$ trials to get a success, so
$$
P(X>r)=(1-p)^r
$$
___
## Memoryless Distribution
$$
P(X=k+r|X>r)=\frac{P(X=k+r)}{P(X>r)}=\frac{(1-p)^{k+r-1}p}{(1-p)^r}
$$
$$
=(1-p)^{k-1}p=P(X=k)
$$
This is because you essentially are ignoring the first $r$ trials
___
## Expectation
Find $E(X)$
$$
E(X)=\sum_{r=1}^\infty r(1-p)^{r-1}p=p\sum_{r=1}^\infty r(1-p)^{r-1}
$$
$$
=p\left( \sum_{r=1}^\infty(1-p)^{r-1} +\sum_{r=2}^\infty(1-p)^{r-1}+\sum_{r=3}^\infty(1-p)^{r-1}+\dots\right)
$$
These infinite sums are all [[Geometric Progressions|geometric progressions]]
$$
=p\left( \frac{1}{p}+\frac{1-p}{p}+\frac{(1-p)^{2}}{p}+\dots \right)
$$
$$
=1+(1-p)+(1-p)^{2}+\dots
$$
Another geometric progression
$$
\therefore E(X)=\frac{1}{p}
$$
___
## Variance
Consider $E(X(X-1))$
$$
E(X(X-1))= 1\cdot 0p+2\cdot 1 p(1-p)+3 \cdot 2p(1-p)^{2}+4\cdot 3p(1-p)^{3}+\dots
$$
$$
=p(1-p)(2\cdot 1+3\cdot 2(1-p)+4\cdot 3(1-p)^{2}+\dots)
$$
Let $q=1-p$
$$
=pq(2\cdot 1+3\cdot 2q+4\cdot 3q^{2}+\dots)
$$
Now consider
$$
\frac{1}{1-x}=1+x+x^{2}+x^{3}+\dots
$$
$$
\implies\frac{d}{dx}\left( \frac{1}{1-x} \right)=1+2x+3x^{2}+\dots
$$
$$
\implies \frac{d^{2}}{dx^{2}}\left( \frac{1}{1-x} \right)=(2\cdot 1+3\cdot 2x+4\cdot 3x^{2}+\dots)
$$
We can use this:
$$
\implies E(X(X-1))=pq\left( \frac{d^{2}}{dq^{2}}\left( \frac{1}{1-q} \right) \right)
$$
$$
=pq\left( \frac{d}{dq}\left( \frac{1}{(1-q)^{2}} \right) \right)
$$
$$
=pq\left( \frac{2}{(1-q)^{3}} \right)=p(1-p)\left( \frac{2}{p^{3}} \right)=\frac{2(1-p)}{p^{2}}
$$
We know $Var(X)=E(X(X-1))+E(X)-(E(X)^{2})$
$$
\implies Var(X)=\frac{2(1-p)}{p^{2}}+\frac{1}{p}-\frac{1}{p^{2}}
$$
$$
=\frac{2-2p+p-1}{p^{2}}=\frac{ 1-p }{p^{2}}
$$
$$
\therefore Var(X)=\frac{1-p}{p^{2}}
$$




