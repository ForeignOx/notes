For a [[Sequences|sequence]] $(a_{k})_{k\in\mathbb{N}}$ set this [[Limsup and Liminf|limsup]]:
$$
a=\limsup_{ k \to \infty }\sqrt[k]{\left| a_{k} \right|   } 
$$
If $a<1$, then [[series|$\sum_{k=1}^{\infty} a_{k}$]] is [[Absolute Convergence|absolutely convergent]]
If $a>1$, then $\sum_{k=1}^{\infty} a_{k}$ is divergent
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
Hence for all $k\geq n_{1}$, 
$$
\left| a_{k} \right| \geq q^{k}
$$
By comparison test with the diverging geometric series $\sum_{k=1}^{\infty} q^{k}$, we get divergence
## Examples
Look at $\sum_{n=1}^{\infty} \frac{1}{n}$, $\sum_{n=1}^{\infty} \frac{1}{n^{2}}$
Look at $\sqrt[n]{ \frac{1}{n} }$
$$
\ln\left( \sqrt[n]{\frac{1}{n}  } \right)=\frac{1}{n}\ln\left( \frac{1}{n} \right)=\frac{\ln n}{n}\to_{0}
$$
So we can't say anything
___
$$
e_{k}=(2+(-1)^{k})c^{k},c\in \mathbb{R}
$$
Using the root test:
$$
\sqrt[k]{ |e_{k}| }=\sqrt[k]{ \left| 2+(-1)^{k} \right| \left| c \right| ^{k} }=|c|\sqrt[k]{2 \pm1  }\to|c|
$$
So we get absolute convergence for $|c|<1$, and divergece for $|c|>1$
 If $c=1$, $e_{k}=2+(-1)^{k}$ does not converge to $\hspace{0pt}0$, we get divergence
 If $c=-1$, $e_{k}=(-1)^{k}(2+(-1)^{k})$ does not converge to $\hspace{0pt}0$, we get divergence
 
#Mathematics #Analysis #Theorem 