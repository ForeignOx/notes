Also known as SET, states that:
Suppose that $V$ is a [[Real Vectorspaces|vectorspace]] and $S=\{ \vec{v}_{1},\dots,\vec{v}_{k} \}\subseteq V$ is a [[Span|spanninng]] [[Sets|set]] for $V$, $L=\{ \vec{u}_{1},\dots,\vec{u}_{l} \}$ is a [[Linear Independence|linearly independent]] set. Then there exists distinct [[Vectors|vectors]]:
$$
\vec{v}_{i_{1}},\vec{v}_{i_{2}},\dots,\vec{v}_{i_{l}}\in S
$$
Such that for each $0\leq j\leq l$ we have:
$$
(S\setminus \{ \vec{v}_{i_{1}},\dots,\vec{v}_{i_{j}} \})\cup \{ \vec{u}_{1},\dots,\vec{u}_{j} \}
$$
Is a spanning set
## Proof
[[Proof by Mathematical Induction!!!!!|Induction]] on $j$. Base case, $j=0$ is clear. So suppose we have distinct $\vec{v}_{i_{1}},\dots,\vec{v}_{i_{J}}$ such that:
$$
(S\setminus \{ \vec{v}_{i_{1}},\dots,\vec{v}_{i_{J}} \})\cup \{ \vec{u}_{1},\dots,\vec{u}_{J} \}
$$
Is spanning, since this is spanning, we have:
$$
\vec{u}_{J+1}=\sum_{\vec{w}\in S\setminus \{ \vec{v}_{i_{1}},\dots,\vec{v}_{i_{j}} \}}\lambda_{\vec{w}}\vec{w}+\sum_{k=1}^{j}\mu_{k}\vec{u}_{k}
$$
Not every $\lambda_{\vec{w}}$ can be zero, since suppose it were, then the first sum would be zero, and then since the second sum is linearly independent, then we would have a linear dependence between the $\vec{u}_{1},\dots,\vec{u}_{J+1}$. So pick a non-zero $\lambda_{\vec{v}_{i_{J+1}}}\neq 0$ to pick $i_{J+1}$, so
$$
V=\text{span}<(S\setminus \{ \vec{v}_{i_{1}},\dots,\vec{v}_{i_{J}} \})\cup \{ \vec{u}_{1},\dots,\vec{u}_{J} \}  > 
$$
$$
= \text{span}< (S\setminus \{ \vec{v}_{i_{1}},\dots,\vec{v}_{i_{J}} \})\cup \{ \vec{u}_{1},\dots,\vec{u}_{J+1} \} >  
$$
Because adding an element doesn't reduce the span, so won't affect it,
$$
=\text{span}< (S\setminus \{ \vec{v}_{i_{1}},\dots,\vec{v}_{i_{J+1}} \})\cup \{ \vec{u}_{1},\dots,\vec{u}_{J+1} \} > 
$$
We can remove $\vec{v}_{i_{J+1}}$, as
$$
\vec{v}_{i_{J+1}}\in \text{span}< (S\setminus \{ \vec{v}_{i_{1}},\dots,\vec{v}_{i_{J+1}} \})\cup \{ \vec{u}_{1},\dots,\vec{u}_{J+1} \}  > 
$$
Which we know because of the non-zero $\lambda_{\vec{v}_{i_{J+1}}}$, so we can remove it
So verified for $J+1$
## Corollary
$k\geq l$, so any linearly independent set has as many or fewer vectors than a spanning set
## Corollary
In a finite dimensional vectorspace, every [[Basis|basis]] has the same [[Cardinality of Sets|cardinality]]
### Proof
If $A=\{ \vec{a}_{1},\dots,\vec{a}_{r} \}$ and $B=\{ \vec{b}_{1},\dots,\vec{b}_{s} \}$ are two bases for $V$, then $r\geq s$ since $A$ is spanning and $B$ is linearly independent, also $s\geq r$, since $B$ is spanning and $A$ is linearly independent, so $r=s$

#Mathematics #LinAlg #Theorem 