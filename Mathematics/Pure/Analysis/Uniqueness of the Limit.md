A [[Convergence|convergent]] [[Sequences|sequence]] $(x_{n})_{n\in\mathbb{N}}$ has precisely $\hspace{0pt}1$ limit
## Proof
Let $x,x'$ be limits of $x_{n}$, with $x\neq x'$
$$
\epsilon=\frac{|x-x'|}{2}>0
$$
Since $(x_{n})_{n\in\mathbb{N}}$ converges to $x$, there is $n_{0}\in\mathbb{N}$ such that $|x_{n}-x\mid<\epsilon$ for al $n\geq n_{0}$
We also have convergence to $x'$, so there exists some $n_{1}\in\mathbb{N}$ with $|x_{n}-x'|<\epsilon$ for all $n\geq n_{1}$
So for $n\geq \text{max}(n_{0},n_{1})$, we now get:
$$
|x-x'|=|x-x_{n}+x_{n}-x'|\leq |x-x_{n}|+|x_{n}-x'|<2\epsilon=|x-x'|
$$
Which is a contradiction