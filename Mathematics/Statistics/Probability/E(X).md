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
## LotUS
$$
E(g(X))=\sum_{x} g(x)p(x)
$$
For discrete
$$
E(g(X))=\int_{-\infty}^{\infty} g(x)f(x) \, dx 
$$
For continuous
### Multivariate
$$
E(g(X,Y))=\sum_{x}\sum_{y}g(x,y)p(x,y)
$$
For discrete
$$
E(g(X,Y))=\int_{-\infty}^{\infty} \int_{-\infty}^{\infty} g(x,y)f(x,y) \, dx  \, dy 
$$
### Linearity
$$
E(\alpha X+\beta Y)=\alpha E(X)+\beta E(Y)
$$
For $\alpha,\beta \in\mathbb{R}$
## Monotonicity of Expectation
Let $X:\Omega\to \mathbb{R}$, $a\in\mathbb{R}$ such that $\mathbb{P}(X\geq a)=1$, then $E(X)\geq a$
### Proof
Define $Y:\Omega\to \mathbb{R}$ as $Y=X-a$, since $\mathbb{P}(X\geq a)=1$, $\mathbb{P}(Y\geq 0)=1$ therefore $E(Y)\geq0$
Let us assume $X$ is continuous, then 
$$
E(Y)=\int_{-\infty}^{\infty} xf(x) \, d-\int_{-\infty}^{\infty} af(x)\, dx  =E(X)-a\underbrace{ \int_{-\infty}^{\infty} f(x) \, dx }_{ =1 } =E(X)-a
$$
We know $E(Y)\geq 0$, so $E(X)-a\geq 0$ so $E(X)\geq a$

### Example
If $\mathbb{P}(X\geq Y)=1$, then $E(X)\geq E(Y)$
#### Proof
Define $Z:=X-Y$

Then $\mathbb{P}(Z\geq 0)=1$, since $\mathbb{P}(X\geq Y)=1$ using the monotonicity of expectation
We also know linearity of independence
$$
E(Z)=E(X)-E(Y)\geq 0
$$
$$
\implies E(X)\geq E(Y)
$$
___
$E(X^{2})\geq (E(X))^{2}$
#### Proof
Ovserve that
$$
Y=(X-E(X))^{2}\geq 0
$$
From the monotonicity, we have $E(Y)\geq 0$, substituting these:
$$
E(X^{2})-(E(X))^{2}\geq 0
$$
$$
\implies E(X^{2})\geq(E(X))^{2}
$$
## Markov Inequality
If $X\geq 0$, then for any $a>0$,
### Proof
Observe
$$
\mathbb{P}(X>a)\leq \frac{E(X)}{a}
$$
Then
$$
X\geq a\mathbb{1}_{\{ X\geq a \}}
$$
$$
a\mathbb{1}_{\{ X\geq a \}}=\begin{cases}
a&\text{if }X(\omega)\geq a\\0&\text{otherwise}
\end{cases}
$$
Hence
$$
E(X)\geq E(a\mathbb{1}_{\{ X\geq a \}})=a\mathbf{E}(\mathbb{1}_{\{ X\geq a \}})=a\mathbb{P}(X\geq a)
$$
## Chebyshev's Inequality
Let $X:\Omega\to \mathbb{R}$ be a random vaiable, let $a(\in\mathbb{R})$, then
$$
\mathbb{P}(|X-E(X)|\geq a)\leq \frac{1}{a^{2}}Var(X)
$$
### Proof
$$
\mathbb{P}(|X-E(X)|\geq a)=\mathbb{P}((X-E(X))^{2}\geq a^{2})\leq \frac{1}{a^{2}}E((X-E(X))^{2})=\frac{1}{a^{2}}Var(X)
$$
Using Markov's inequality

#Mathematics #Statistics 
