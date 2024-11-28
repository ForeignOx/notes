$E(X)$ is the expected value, or mean of a [[Git?/Mathematics/Statistics/Probability/Discrete Random Variables|discrete random variable]] X, and can be calculated like so:
$$
E(X)=\sum_{x\in \mathbb{R}} xP(X=x)
$$
Or for a [[Continuous Random Variables|continuous random variable]],
$$
E(X)=\int_{-\infty}^{\infty} xf(x) \, dx 
$$
Note expectation does not always exist, since expectation exists finitely, which means that, for discrete $\sum|x|p(x)<\infty$, and for continuous, $\int_{-\infty}^{\infty} |x|f(x) \, dx<\infty$
___
THis process is equivalent to haveing the function:
$$
X:\Omega\to \mathbb{R}\to \mathbb{R}
$$
$$
g_{0}(x)\to \text{random variable}\to \mathbb{R}
$$
$$
g_{0}(x)=g(X(\omega))
$$
To find $E(f(X))$, where $f(X)$ is a function of $X$, you can use the formula:
$$
E(f(X))=\sum f(x)P(X=x)
$$
This is useful for calculating [[Var(X)|variance]]
This is also useful to show:
$$
E(aX+b)=\sum (ax+b)P(X=x)
$$
$$
=a\sum xP(X=x)+b\sum P(X=x)
$$
Probabilities sum to one
$$
=a\sum xP(X=x)+b=aE(X)+b
$$
$$
\therefore E(aX+b)=aE(X)+b
$$
Since integrals are also linear, we can do the same with continuous
## Proof
Let $Y=g(x)$, then by definition,
$$
E(g(x))=E(Y)=\sum_{y}y\mathbb{P}(g(X)=y\mid x\in X)
$$
Note that $\mathbb{P}(Y=y)=\mathbb{P}(g(X)=y)$, note that $\mathbb{P}(g(X)-y\mid X=x)=1$, otherwise
$$
\mathbb{P}(Y=y)=\sum_{x:g(x)=y}\mathbb{P}(g(x)=y\mid X=x)\mathbb{P}(X-x)=\sum_{x:g(x)=y}1\times \mathbb{P}(X=x)=\sum_{x:g(x)=y}p(x)
$$
Putting this in $1$:
$$
E(g(x)\sum_{y}y\left( \sum_{x:g(y)=x} p(x) \right)
$$
Interchanging the order of summation:
$$
=\sum_{x}\sum_{y\in g(\mathbb{R})}yp(x)=\sum_{x\in \mathbb{R}}q(x)|p(x)
$$
___
Consider two [[Git?/Mathematics/Statistics/Probability/Discrete Random Variables|discrete random variables]] $X$ and $Y$, where 
$$
p(x,y)=P(X=x, Y=y)
$$
We can write
$$
E(X+Y)=\sum^{x}\sum^{y}(x+y)p(x,y)
$$
$$
=\sum^{x}\sum^{y}(xp(x,y)+yp(x,y))
$$
$$
=\sum^{x}x\sum^{y}p(x,y)+\sum^{y}y\sum^{x}p(x,y)
$$
$$
=E(X)+E(Y)
$$
Similarly, $E(X-Y)=E(X)-E(Y)$, hence:
$$
E(X\pm Y)=E(X)\pm E(Y)
$$
___

#Mathematics #Statistics 
