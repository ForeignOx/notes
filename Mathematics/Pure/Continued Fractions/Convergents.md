The $k$th convergent to a [[continued fraction]] $x=[a_{0};a_{1},\dots ]$ is $c_{k}=[a_{0};a_{1},\dots,a_{k}]$ for $k\leq n$. Note we usually write $c_{k}=\frac{p_{k}}{q_{k}}$
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
## Two successive convergents satisfy $p_{k-1}q_{k}-p_{k}q_{k-1}=(-1)^{k}$
### Proof
Base case, let $k=1$:
$$
p_{0}q_{1}-p_{1}q_{0}=a_{0}a_{1}-1(a_{0}a_{1}+1)=-1=(-1)^{1}
$$
So the claim is true for $k=1$
Assume the claim is true for $k=r$:
$$
p_{r-1}q_{r}-p_{r}q_{r-1}=(-1)^{r}
$$
Consider the case when $k=r+1$:
$$
p_{r}q_{r+1}-p_{r+1}q_{r}=p_{r}(a_{r+1}q_{r}+q_{r-1})-(a_{r+1}p_{r}+p_{r-1})q_{r}=a_{r+1}p_{r}q_{r}+p_{r}q_{r-1}-a_{r+1}p_{r}q_{r}-p_{r-1}q_{r}
$$
$$
=p_{r}q_{r-1}-p_{r-1}q_{r}=-(-1)^{r}=(-1)^{r+1}
$$
Hence the claim is true by induction
## [[Greatest Common Divisor|$gcd(p_{k},q_{k})=1$]]
### Proof:
Assume $gcd(p_{k},q_{k})=d$, where $d>1$. Then $d|p_{k}$ and $d|q_{k}$ which imply $d|(p_{k-1}q_{k}-p_{k}q_{k-1})$ as this is a linear combination of $p_{k}$ and $q_{k}$ (see the Lemma for the [[Euclidean Algorithm]])
But we know $p_{k-1}q_{k}-p_{k}q_{k-1}=(-1)^{k}$, so this implied $d|(-1)^{k}$. This cannot hold for $d>1$
## A real number $x$ with convergents $c_{n}=\frac{p_{n}}{q_{n}}$ satisfies $| x-c_{n} |<\frac{1}{q_{n}q_{n+1}}$ 
### Proof
For each $n$, we can write $x=[a_{0};a_{1},\dots,a_{n},y_{n+1}]$ such that $y_{n+1}>a_{n+1}$ (assuming $a_{n+1}$ is not the final term), then
$$
\left| x-c_{n} \right|=\left| \frac{y_{n+1}p_{n}+p_{n-1}}{y_{n+1}q_{n}+q_{n-1}}-\frac{p_{n}}{q_{n}} \right|=\left| \frac{y_{n+1}p_{n}q_{n}+q_{n}p_{n-1}-y_{n+1}p_{n}q_{n}-p_{n}q_{n-1}}{q_{n}(y_{n+1q_{n}+q_{n-1}})} \right|
$$
$$
=\left| \frac{p_{n-1}q_{n}=p_{n}q_{n-1}}{q_{n}(y_{n+1}q_{n}+q_{n-1})} \right|=\left| \frac{(-1)^{n}}{q_{n}(y_{n+1}q_{n}+q_{n-1})} \right|= \frac{1}{q_{n}(y_{n+1}q_{n}+q_{n-1})}
$$
since $q_{n},y_{n+1},q_{n-1}>0$
$$
<\frac{1}{q_{n}(a_{n+1}q_{n}+q_{n-1})}=\frac{1}{q_{n}q_{n+1}}
$$
$$
\therefore \left| x-c_{n} \right|<\frac{1}{q_{n}q_{n+1}}
$$



#Mathematics #Fractions #Definition #Theorem