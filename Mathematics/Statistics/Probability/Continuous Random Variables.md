Let $X:\Omega\to \mathbb{R}$ be a [[Random Variables|random variable]], we call $X$ a continuous random variable, or $X$ has a continuous probability distribution, if there exists a non-negative [[Functions|function]] $f$:
$$
f:\mathbb{R}\to \mathbb{R}
$$
Such that
$$
\mathbb{P}(X \in [a,b])=\int ^{b}_{a} f(t) \, dt 
$$
$f$ is called the probability density function of $X$ or pdf
Let $x \in\mathbb{R}$, choose $a=b=x$:
$$
\mathbb{P}(X=x)=\int _{a}^{a}f(t) \, dt =0
$$
We say that a continuous random variable has no mass a given value, so we can't say:
$$
\mathbb{P}(X=x)=f(x)
$$ But we can think that:
$$
\mathbb{P}(X \in [x,x+dx])\approx f(x)
$$
For small $dx$, you can think of $f(x)$ as the rate of change in that sense:
$$
\frac{d \mathbb{P}(X\in [x,x+dx])}{dx} \approx f(x)
$$
A pdf is always [[Piecewise Functions|piecewise]] [[Continuity|continuous]], but it is not necessarily unique
Piecewise continuous means that there are some discontinuities, but the probability is defined in continuous pieces
Note that:
$$
\mathbb{P}(X \in (a,b))=\mathbb{P}(X \in [a,b))=\mathbb{P}(X\in (a,b])=\mathbb{P}(X \in [a,b])
$$
For now we will assume that pdf is unique except for finitely many points, that is, if $X$ is a random variable, let $f$ and $g$ be potential candidates for the pdf of $X$, then there exists a finite $k\geq 1$ and a sequence $a_{1},a_{2},\dots ,a_{k}$ such that $a_{i}\in\mathbb{R},1\leq i\leq k$ such that $f(x)=g(x)\forall x\not\in\{ a_{1},a_{2},\dots ,a_{k} \}$. The pdf is unique up to a set of measure zeros
## Finite Union of Intervals
Let $B\subseteq \mathbb{R}$, such that $B=\bigcup_{i=1}^{m}[a_{i},b_{i}]$ ($B$ is a finite union of intervals, the intervals may be open or closed or a mixture), then 
$$
\mathbb{P}(X \in B)=\int _{B}f(x) \, dx 
$$
### Corollary
If the intervals are disjoint, we can write it as a sum:
$$
        \mathbb{P}(X \in B)=\sum_{i=1}^{m}\int_{a_{i}}^{b_{i}}f(x)  \, dx 
$$
### Infinities
Note that then we can say:
$$
\mathbb{P}( X \in (-\infty,b])=\int _{-\infty}^{b}f(x) \, dx ,\mathbb{P}(X \in [a,\infty) )=\int _{a}^{\infty}f(x) \, dx 
$$
As we can write:
$$
(-\infty,b]=\bigcup_{n=1}^{\infty}\left( -\infty,b-\frac{1}{n} \right]
$$
Which is a countable union
From this we can say:
$$
\mathbb{P}(X\in\mathbb{R})=\mathbb{P}(-\infty<x<\infty)=\int_{-\infty}^{\infty} f(t) \, dt =1
$$