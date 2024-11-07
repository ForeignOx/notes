## Functions?

## [[Sequences|Sequences]]
Let $(x_{n})_{n\in\mathbb{N}}$ and $(y_{n})_{n\in\mathbb{N}}$ be sequences which are [[Convergence|convergent]] with $x=\lim_{ n \to \infty }x_{n}$ and $y=\lim_{ n \to \infty }y_{n}$. Also let $a,b\in\mathbb{R}$. Then:
$$
\lim_{ n \to \infty } (ax_{n}+by_{n})=ax+by
$$
$$
\lim_{ n \to \infty } (x_{n}y_{n})=xy
$$
$$
\lim_{ n \to \infty } \left( \frac{x_{n}}{y_{n}} \right)=\frac{x}{y}
$$
(Provided $y\neq 0$ and $y_{n}\neq 0\forall n\in\mathbb{N}$)
### Proof
Proof of the second part:
We need to know about $|x_{n}y_{n}-yx|<\epsilon$ for all $n\geq N_\epsilon$
$$
|x_{n}y_{n}-xy|=|x_{n}y_{n}-x_{n}y+x_{n}y-xy|
$$
And by the triangle inequality:
$$
\leq|x_{n}(y_{n}-y)|+|(x_{n}-x)y|=|x_{n}||y_{n}-y|+|x_{n}-x| |y|
$$
We can now make $|x_{n}-x|$ and $|y_{n}-y|$arbitrarily small, and then we only have $|x_{n}|$ to worry about
Note there is a $c>0$ with $|x_{n}|\leq c$ since [[Every Convergent Sequence is Bounded|convergent sequences are bounded]]
We can also assume that $c\geq|y|$, then
$$
|x_{n}y_{n}-xy|\leq c(|y_{n}-y|+|x_{n}-x|)
$$
Now let $\epsilon>0$, there exists an $N_{\epsilon1}$ and $N_{\epsilon 2}$ with
$$
|y_{n}-y|<\frac{\epsilon}{2c} \forall n\geq N_{\epsilon 1}
$$
$$
|x_{n}-x|<\frac{\epsilon}{2c} \forall n\geq N_{\epsilon 2}
$$
Then for all $n\geq \text{max}(N_{\epsilon 1},N_{\epsilon2})$ we have:
$$
|x_{n}y_{n}-xy|\leq c(|y_{n}-y|+|x_{n}-x|)<c\left( \frac{\epsilon}{2c}+\frac{\epsilon}{2c} \right)=\epsilon
$$
$W^5$
### Example
Consider a sequence:
$$
x_{n}=\frac{n^{3}-2n^{2}+3n-4}{3n^{4}+10n^{2}-8}=\frac{n^{3}\left( 1-\frac{2}{n}+\frac{3}{n^{2}}-\frac{4}{n^{3}} \right)}{n^{4}\left( 3+\frac{10}{n^{2}}-\frac{8}{n^{4}} \right)}
$$
$$
= \frac{1}{n}\left( \frac{1-\frac{2}{n}+\frac{3}{n^{2}}-\frac{4}{n^{3}}}{3+\frac{10}{n^{2}}-\frac{8}{n^{4}}} \right)
$$
Each part divided by $n^{r}$ goes to $\hspace{0pt}0$, and so by COLT,
$$
\lim_{ n \to \infty } x_{n}=0\times \frac{1}{3}=0
$$
___
$x_{1}=1$, $x_{n}=\frac{x_{n-1}}{2}+\frac{1}{x_{n-1}}$ for $n\geq 2$
$x_{n}\in[1,2]$ by induction, since $x_{1}\in[1,2]$
If $x_{n-1}\in[1,2]$, then
$$
\frac{x_{n-1}}{2}\in \left[ \frac{1}{2},1 \right]
$$
$$
\frac{1}{x_{n-1}}\in \left[ \frac{1}{2},1 \right]
$$
So by adding them, 
$$
x_{n}\in [1,2]
$$
Let us assume that $x_{n}$ converges to $x$, then $x_{n-1}$ also converges to $x$, so by COLT:
$$
x=\lim_{ n \to \infty } x_{n}=\lim_{ n \to \infty }\left( \frac{x_{n-1}}{2}+\frac{1}{x_{n-1}} \right)=\frac{x}{2}+\frac{1}{x}
$$
$$
\implies x^{2}=2
$$
So we have two candidates, $x=\sqrt{ 2 }$ or $x=-\sqrt{ 2 }$, but $-\sqrt{ 2 }$ is not in our interval, so we can ignore it
Now we can use the [[Squeeze Theorem|squeeze thorem]] to show convergence:
$$
|x_{n}-\sqrt{ 2 }|=\left|\frac{x_{n-1}}{2}+\frac{1}{x_{n-1}}-\sqrt{ 2 } \right|=\left| \frac{x_{n-1}^{2}+2-2\sqrt{ 2 }x_{n-1}}{2x_{n-1}} \right|=\frac{(x_{n-1}-\sqrt{ 2 })^{2}}{2x_{n-1}}
$$
As the numerator is squared, and $x_{n-1}\in[1,2]$
$$
\therefore |x_{n}-\sqrt{ 2 }|\leq \frac{|x_{n-1}-\sqrt{ 2 }|}{2}\leq \frac{|x_{n-2}-\sqrt{ 2 }|}{4}\leq\dots
$$
So
$$
|x_{n}-\sqrt{ 2 }|\leq \frac{1}{2^{n}}
$$
And we know $\frac{1}{2^{n}}$ is a case of [[Convergence#In the form of $x_{n}=c {n}$|$c^{n}$]], so we know it converges to $\hspace{0pt}0$, so $x_{n}-\sqrt{ 2 }$ tends to $\hspace{0pt}0$, so $x_{n}$ tends to $\sqrt{ 2 }$

