Let $(a_{k})_{k\in\mathbb{N}}$ be a [[Sequences|sequence]] of [[Real Numbers|real numbers]], then the sequence of partial sums $(s_{n})_{n\in\mathbb{N}}$ is defined as:
$$
s_{n}=\sum_{k=1}^{n}a_{k}
$$
If the sequence of partial sums [[Convergence|converges]], we say the series $\sum_{k=1}^{\infty}a_{k}$ is covergent, and then
$$
\sum_{k=1}^{\infty}a_{k}=\lim_{ n \to \infty }s_{n} 
$$
Otherwise $\sum_{k=1}^{\infty}a_{k}$ is divergent
## Remark
Series can start with a summand different from $a_{1}$, e.g. $\sum_{k=0}^{\infty}a_{k}$ or $\sum_{k=3}^{\infty}a_{k}$, as long as all the terms are defined
$\sum_{k=1}^{\infty}a_{k}$ converges iff $\sum_{k=N}^{\infty}a_{k}$
## Examples
### Geometric Series
For $k\in\mathbb{N}_{0}$, let $a_{k}=q^{k}$ with $q\in\mathbb{R}$, starts with $a_{0}=1$
$$
s_{n}=\sum_{k=0}^{n}q^{k}=\frac{1-q^{n+1}}{1-q}
$$
For $q\neq 1$

#### Proof
Proof by induction, $n=0$, gives 
$$
s_{0}=1=\frac{1-q}{1-q}
$$
Assme true for $n$
$$
s_{n+1}=s_{n}+q^{n+1}=\frac{1-q^{n+1}}{1-q}+\frac{q^{n+1}-q^{n+2}}{1-q}=\frac{1-q^{n+2}}{1-q}
$$
___
For $|q|<1$, $s_{n}$ converges to $\frac{1}{1-q}$, for $|q|>1$, $q^{n+1}$ is unbounded, and so is $s_{n}$, so the series is divergent, for $q=1$, $s_{n}=n+1$, which diverges, for $q=-1$, $s_{n}$ alternates between $\hspace{0pt}1$ and $\hspace{0pt}0$, so is also divergent
### Example 2
For $k\in\mathbb{N}$, let 
$$
q_{k}=\frac{1}{k(k+1)}=\frac{1}{k}-\frac{1}{k+1}
$$
$$
s_{n}=\sum_{k=1}^{n} \frac{1}{k(k+1)} =\sum_{ k=1} ^{ n}\left( \frac{1}{k}-\frac{1}{k+1} \right)=1-\frac{1}{2}+\frac{1}{2}-\frac{1}{3}+\dots+\frac{1}{n}-\frac{1}{n+1}
$$
$$
= 1-\frac{1}{n+1}
$$
So
$$
\sum_{k=1}^{\infty} \frac{1}{k(k+1)}=\lim_{ n \to \infty } \left( 1-\frac{1}{n+1} \right)=1
$$
## If $\sum_{k=0}^{\infty} a_{k}$ is convergent, then $\lim_{ k \to \infty }a_{k}=0$
Proof:
Let $s_{n}=\sum_{k=0}^{\infty} a_{k}$, then $\lim_{ n \to \infty }s_{n}=s$ for some $s \in \mathbb{R}$
Write $a_{n}=s_{n}-s_{n-1}$ for $n\geq 1$, so by [[Calculus of Limits Theorem|CoLT]], $\lim_{ n \to \infty }a_{n}=s-s=0$
This is a criterion for divergence fo a series, it is not a criterion for convergence of a series
## Convergence Criteria
### Comparison Test
Let $N\in\mathbb{N}$, and let $(a_{k})_{k\in\mathbb{N}_{0}}$, $(b_{k})_{k\in\mathbb{N}_{0}}$ be sequences with $0\leq a_{k}\leq b_{k}$ for $k\geq n$:
- If $\sum_{k=0}^{\infty} b_{k}$ is convergent, then $\sum_{k=0}^{\infty} a_{k}$ is convergent
- If $\sum_{k=0}^{\infty} a_{k}$ is divergent, then $\sum_{k=0}^{\infty} b_{k}$ is divergent
#### Proof
Use $\sum_{k=0}^{\infty} a_{k}$ is convergent iff $\sum_{k=N}^{\infty} a_{k}$ is convergent:
For $n\geq N$, let $s_{n}=\sum_{k=N}^{n}a_{k}$ and $t_{n}=\sum_{k=N}^{\infty} b_{k}$, these are monotonically increasing since $0\leq a_{k}\leq b_{k}$
If $\sum_{k=0}^{\infty} b_{k}$ is convergent, then $(t_{n})_{n\geq N}$ also converges, to $t$, $s_{n}\leq t_{n}\leq t$, so the sequence $s_{n}$ is monotonically increasing and [[Boundedness|bounded]], so is convergent by [[Every Increasing Sequence which is Bounded Above, Converges|this theorem]]
Since $s_{n}$ is monotonically increasing, divergence means that $s_{n}$ is unbounded, but then $t_{n}$ is also unbounded, so must also diverge
#### Example
$\sum_{k=1}^{\infty} \frac{1}{k^{2}}$ converges, since:
$$
\frac{1}{n^{2}}=\frac{2}{n^{2}+n^{2}}\leq \frac{2}{n^{2}+n}=\frac{2}{n(n+1)}
$$
We know $\sum_{k=1}^{\infty} \frac{2}{k(k+1)}$ converges to $\hspace{0pt}2$ by [[Calculus of Limits Theorem|CoLT]] and the example above, so by comparison test, we know it also converges
