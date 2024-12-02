Let $(a_{k})_{k\in\mathbb{N}}$ be a [[Sequences|sequence]] with the following properties, $a_{k}\neq 0$ for all $k\in\mathbb{N}$, except finitely many
- If $\lim_{ k \to \infty }\left| \frac{a_{k+1}}{a_{k}} \right|<1$, then the [[series|series]] $\sum_{k=1}^{\infty} a_{k}$ is [[Absolute Convergence|absolutely convergent]]
- If $\lim_{ k \to \infty } \left| \frac{a_{k+1}}{a_{k}} \right|>1$, then the series $\sum_{k=1}^{\infty} a_{k}$ is divergent
## Remark
The limit $\lim_{ k \to \infty }\left| \frac{a_{k+1}}{a_{k}} \right|$ need not exist, but we can still make a conclusion, provided:
- If $\lim\sup_{ k \to \infty } \left| \frac{a_{k+1}}{a_{k}} \right|<1$, that is $\left|  \frac{a_{k+1}}{a_{k}}\right|\leq q<1$ for all but finiteely many $k$, then series is absolutely convergent
- If $\left| \frac{a_{k+1}}{a_{k}} \right|\geq 1$ for all but finitely many $k$, then $\sum_{k=1}^{\infty} a_{k}$ diverges
## Proof
Assume $\limsup_{ k \to \infty } \left| \frac{a_{k+1}}{a_{k}} \right|<1$, then there exists $n_{0}$ with  $\left| \frac{a_{k+1}}{a_{k}} \right|\leq q$ for all $k\geq n_{0}$, 
$$
\implies \left| a_{k+1} \right|\leq \left| a_{k} \right|q
$$
$$
\implies \left| a_{n_{0}+j} \right| \leq \left| a_{n_{0}+j-1} \right| q\leq \left| a_{n_{0}+j-2} \right| q^{2}\leq\dots \leq \left| a_{n_{0}} \right| q^{j}
$$
Which can be thought of as a sort of a comparison series, since $0\leq q<1$, so
$$
\sum_{j=0}^{\infty} |a_{n_{0}}|q^{j}=\frac{\left| a_{n_{0}} \right|  }{1-q}
$$
So $\sum_{j=0}^{\infty} \left| a_{n_{0}+j} \right|$ is convergent by comparison test and is equal to $\sum_{k=n_{0}}^{\infty} \left| a_{k} \right|$ so is absolutely convergent. Hence $\sum_{k=1}^{\infty} \left| a_{k} \right|$ is also absolutely convergent