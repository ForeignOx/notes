The $k$th convergent to a [[Finite Continued Fraction]] $x=[a_{0};a_{1},\dots a_{n}]$ is $c_{k}=[a_{0};a_{1},\dots,a_{k}]$ for $k\leq n$. Note we usually write $c_{k}=\frac{p_{k}}{q_{k}}$
## Calculating Convergents
Let $x=[a_{0};a_{1},\dots,a_{n}]$, then its convergents $c_{k}=\frac{p_{k}}{q_{k}}$ can be calculated using the following recurrence relations:
$$
p_{0}=a_{0},\,p_{1}=a_{0}a_{1}+1,\,\text{for }k\geq 2,\, p_{k}=a_{k}p_{k-1}+p_{k-2}
$$
$$
q_{0}=1,\,q_{1}=a_{1},\text{ for }k\geq 2,\,q_{k}=a_{k}q_{k-1}+q_{k-2}
$$
### Proof
First verify for $k=0$:
$$
c_{0}=[a_{0}]=a_{0}
$$
$$
\frac{p_{0}}{q_{0}}=\frac{a_{0}}{1}=a_{0}
$$
So it is true for $k=0$, next verify for $k=1$:
$$
c_{1}=[a_{0};a_{1}]=a_{0}+\frac{1}{a_{1}}=\frac{a_{0}a_{1}+1}{a_{1}}
$$
$$
\frac{p_{1}}{p_{2}}=\frac{a_{0}a_{1}+1}{a_{1}}
$$
So it is true for $k=1$
For $k\geq 2$, $[a_{0};a_{1},\dots,a_{k}]=\frac{a_{k}p_{k-1}+p_{k-2}}{a_{k}q_{k-1}+q_{k-2}}$
Base case:
$$
LHS=[a_{0},a_{1},a_{2}]=a_{0}+\frac{1}{a_{1}+\frac{1}{a_{2}}}=a_{0}+\frac{1}{\frac{a_{1}a_{2}+1}{a_{2}}}=a_{0}+\frac{a_{2}}{a_{1}a_{2}+1}
$$
$$
=\frac{a_{0}a_{1}a_{2}+a_{0}+a_{2}}{a_{1}a_{2}+1}
$$
$RHS:$
$$
p_{2}=a_{2}p_{1}+p_{0}=a_{2}(a_{0}a_{1}+1)+a_{0}=a_{0}a_{1}a_{2}+a_{0}+a_{2}
$$
$$
q_{2}=a_{2}q_{1}+q_{0}=a_{2}a_{1}+1
$$
$$
\implies RHS=\frac{p_{2}}{q_{2}}=\frac{a_{0}a_{1}a_{2}+a_{0}+a_{2}}{a_{1}a_{2}+1}=LHS
$$
So claim is true for $k=2$
Assume claim is true for $k=r$:
$$
[a_{0};a_{1},\dots,a_{r}]=\frac{p_{r}}{q_{r}}
$$
Where
$$
p_{r}=a_{r}p_{r-1}+p_{r-2}
$$
$$
q_{r}=a_{r}q_{r-1}+q_{r-2}
$$
Consider $k=r+1$:
$$
[a_{0};a_{1},\dots,a_{r},a_{r+1}]=\left[ a_{0};a_{1},\dots,a_{r}+\frac{1}{a_{r+1}} \right]=\frac{\left( a_{r}+\frac{1}{a_{r+1}} \right)p_{r-1}+p_{r-2}}{\left( a_{r}+\frac{1}{a_{r+1}} \right)q_{r-1}+q_{r-2}}
$$
By assumption,
$$
=\frac{a_{r+1}a_{r}p_{r-1}+q_{r-1}+a_{r+1}p_{r-2}}{a_{r+1}a_{r}q_{r-1}+q_{r-1}+a_{r+1}q_{r-2}}=\frac{a_{r+1}(a_{r}p_{r-1}+p_{r-2})+p_{r-1}}{a_{r+1}(a_{r}q_{r-1}+q_{r-2})+q_{r-1}}
$$
$$
=\frac{a_{r+1}p_{r}+p_{r-1}}{a_{r+1}q_{r}+q_{r-1}}
$$
Which is the claim for $k=r+1$
Hence, if the claim is true for $k=r$ then the claim is true for $k=r+1$, and since we have shown that the claim is true for $k=2$, by induction, the claim is true for all $k\geq 2,k\in\mathbb{Z}$
## 