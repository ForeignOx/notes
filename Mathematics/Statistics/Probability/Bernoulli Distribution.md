A Bernoulli trial is a random experiment with only two possible outcomes:
- Success, with probability $p$
- Failure, with probability $1-p(=q)$


___
The Bernoulli distribution assigns a [[Random Variables|random variable]] to a Bernoulli trial with:
- a value of 1 corresponding to a 'success'
- a value of 0 corresponding to a 'failure'
So:
$$
X\sim \text{Bernoulli}(p) \iff P(X=x)=\begin{cases}
p && x=1 \\
1-p && x=0\\
0 && \text{otherwise}
\end{cases}
$$
___
## [[E(X)]]
$$
E(X)=\sum xP(X=x)=1\times p+0\times(1-p)=p
$$
___
## [[Var(X)]]
$$
Var(X)=\sum x^{2}P(X=x)-(E(X))^{2}=1^{2}\times p+0^{2}\times (1-p)-p^{2}=p-p^{2}=p(1-p)=pq
$$

#Mathematics #Statistics #Distribution