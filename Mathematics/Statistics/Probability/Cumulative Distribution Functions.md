For any [[Random Variables|random variable]] $X$, 
$$
\mathbb{P}_{X}(B)=\mathbb{P}(X \in B), B\subseteq \mathbb{R}
$$
We define the cumulative distribution [[Functions|function]] (cdf) as this probability on the [[Intervals|interval]] $(-\infty,x]$:
$$
\mathbb{P}_{X}((-\infty,x])=\mathbb{P}(X\in (-\infty,x])=\mathbb{P}(X\leq x)=F(x)
$$
So a cdf:
$$
F:\mathbb{R}\to[0,1]
$$
$$
 F(X)=\mathbb{P}(X\leq x)
$$
So we can find $X(\omega)$ in the way
Let $-\infty<a\leq b<\infty$,
$$
\mathbb{P}(X \in (a,b])=F_{X}(b)-F_{X}(a)
$$
## Proof
The interval $(a,b]=(-\infty,b]\setminus(-\infty,a]$, so we can write:
$$
\mathbb{P}(X \in (a,b])=\mathbb{P}(X \in (-\infty,b]\setminus(-\infty,a])=\mathbb{P}(X\in (-\infty,b])-\mathbb{P}(X \in \underbrace{ (-\infty,b]\cap(-\infty,a] }_{ (-\infty,a] })
$$
Using the first consequence of [[Probabilities|probability]]
$$
\therefore \mathbb{P}(X \in (a,b])=\mathbb{P}(X \in (-\infty,a])=F_{X}(b)-F_{X}(a)
$$
## Theorem
### [[Continuous Random Variables|Continuous]]:
Let $X$ be a continuous random variable with pdf $f$, then 
$$
F(x)=\mathbb{P}(X\leq x)=\int _{-\infty}^{x}f(t) \, dt
$$
Moreover,
$$
\frac{d F}{dx} (x)=f(x)
$$
$F$ is [[Continuity|continuous]] everywhere except at countably many points, that is $\lim_{ y \to x }F(y)=F(x)$ for countably many $x$
### [[Discrete Random Variables|Discrete]]:
Let $X$ be a discrete random variable with pmf $p$, then 
$$
F(x)=\sum_{t:t\leq x}p(t)
$$
$F(x)$ is piecewise continuous and discontinuities, and the discontinuities are jump discontinuities. $F$ is always right discontinuous (for both discrete and continuous), i.e. at the point of discontinuity,
$$
\lim_{ y \uparrow x } F(y)\neq F(x)
$$
But
$$
\lim_{ y \downarrow x } F(y)=F(x)
$$
For all $x$, so for a discrete random variable,
$$
\mathbb{P}(X=x)=\lim_{ y \uparrow x }F(y)=p(x) 
$$
We find this by supposing $p(x-1)\neq 0$ and $p(x)\neq 0$ and $p(y)=0$, for any $[x-1,x]$, 
## Theorem 2
Let $F$ be a cdf, then it has the following properties:
- $\lim_{ x \to -\infty }F(x)=0$, $\lim_{ x \to \infty }F(x)=1$
- $F$ is always right continuous
- $F$ is monotonically increasing
### Proof
For the first,
$$
F(x)=\mathbb{P}(X \in (-\infty,x])
$$
We know that
$$
\lim_{ x \to \infty } (-\infty,x]=\mathbb{R}
$$
So
$$
\lim_{ x \to \infty } F(x)=\mathbb{P}(X \in \mathbb{R})=1
$$
Similarly,
$$
\lim_{ x \to -\infty } (-\infty,a]=\emptyset
$$
So
$$
\lim_{ x \to \infty } F(x)=\mathbb{P}(X \in \emptyset)=0
$$
For the second, prove in own time bro
For the third, consider
$$
F(s)=\mathbb{P}(X\leq s)=\mathbb{P}(X \in (-\infty,s])
$$
$$
 F(t)=\mathbb{P}(X\leq t)=\mathbb{P}(X \in (-\infty,t])
$$
If $s\leq t$, $(-\infty,s]\subseteq(-\infty,t]$, then $\mathbb{P}(A)\leq \mathbb{P}(B)$, using this, we get $F(s)\leq F(t)$


