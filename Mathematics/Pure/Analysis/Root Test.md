For a [[Sequences|sequence]] $(a_{k})_{k\in\mathbb{N}}$ set this [[Limsup and Liminf|limsup]]:
$$
a=\limsup_{ k \to \infty }\sqrt[k]{\left| a_{k} \right|   } 
$$
If $a<1$, then [[series|$\sum_{k=1}^{\infty} a_{k}$]] is [[Absolute Convergence|absolutely convergent]]
If $a>1$, then $\sum_{k=1}^{\infty} a_{k}$ is devergent
## Proof
Assume $a<1$, then for all but finitely many $k$, we have:
$$
\sqrt[k]{ \left| a_{k} \right|  }\leq q<1
$$
(using $q=\frac{a+1}{2}$), so for all $k\geq n_{0}$, we have
$$
\left| a_{k} \right| \leq q^{k}
$$
By comparison test with the convergent geometric series $\sum_{k=1}^{\infty} q^{k}$, gives absolute convergence
Assume $a>1$, then for all but finitely many $k$, we have
$$
\sqrt[k]{ \left| a_{k} \right|  }\geq q>1
$$
ence for all $k\geq n_{1}$, 