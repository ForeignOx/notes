If $V$ is a finite dimensional [[Real Vectorspaces|vectorspace]], we define its dimension, $\text{dim}(V)$ to be the [[Cardinality of Sets|cardinality]] of any [[Basis|basis]] of $V$
## Examples
$\text{dim}(\mathbb{R}^{n})=n$, as $n=|\{ \vec{e}_{1},\dots,\vec{e}_{n} \}|$
___
$\text{dim}(\mathbb{R}[x]_{n})$ as a basis: $\{ 1,x,x^{2},\dots,x^{n} \}$ which has cardinality $n+1$ as we go through powers of $x$ from $\hspace{0pt}0$ to $n$
___
$\text{dim}(M_{m\times n}(\mathbb{R}))=mn$, as it has a basis: $\{ E^{ij}\mid 1\leq i\leq m,1\leq j\leq n \}$
___
Consider $U\subseteq \mathbb{R}[x]_{n}$, $U:=\{ p\in\mathbb{R}[x]_{n}\mid p(1)=0 \}$, this is a [[Subspaces|subspace]] (which we can check). Calculus tells us $p \in U\iff(x-1)|p$, so $U=\{ (x-1)q\mid q\in\mathbb{R}[x]_{n-1} \}$, so $U$ has a basis: 
$$
\{ (x-1),(x-1)x,\dots,(x-1)x^{n-1} \}
$$
Which we can check to be spanning and linearly independent, so $\text{dim}(U)=n$
___
$\text{sym}_{2}(\mathbb{R})\subseteq M_{2}(\mathbb{R})$ has basis:
$$
\left\{  \begin{pmatrix}
1&0\\0&0
\end{pmatrix},\begin{pmatrix}
0&0\\0&1
\end{pmatrix},\begin{pmatrix}
0&1\\1&0
\end{pmatrix}  \right\}
$$
Which we can check to be spanning and linearly indipendent, so $\text{dim}(\text{sim}_{2}(\mathbb{R}))=3$