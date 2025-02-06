## Real Inner Products
An inner product on a [[Vectorspaces|real vectorspace]] $V$ is a [[Linear Maps|map]] $(\cdot,\cdot):V\times V\mapsto \mathbb{R}$, which assigns each pair of vectors $\underline{u},\underline{v}\in V$ a [[Real Numbers|real number]] $(\underline{u},\underline{v})$, satisfying the following for all $\underline{u},\underline{v},\underline{w}\in V$, $\lambda \in\mathbb{R}$:
- $(\underline{u},\underline{v})=(\underline{v},\underline{u})$ symmetry
- $(\underline{u}+\underline{v},\underline{w})=(\underline{u},\underline{w})+(\underline{v},\underline{w})$
- $(\lambda \underline{u},\underline{v})=\lambda(\underline{u},\underline{v})$ these last two mean that it is [[Linear|linear]] in first order, with symmetry as well, linear in second order; a symmetric [[Bilinear Form|bilinear form]]
- $(\underline{v},\underline{v})\geq 0$ with $(\underline{v},\underline{v})=0\iff \underline{v}=\underline{0}$ (positivity)
Essentially, a bilinear form which is symmetric and positie defines an inner product $(\underline{u},\underline{v})=B(\underline{u},\underline{v})$
## Encoding with Matrices
We can always encode an inner product via a [[Matrices|matrix]], since you can encode a bilinear product, $(\underline{v}_{i},\underline{v}_{j})=A_{ji}$, then 
$$
(\underline{u},\underline{v})=\sum_{ i=1} ^{ n}  \sum_{ j=1} ^{ n}  y_{j}A_{ji}x_{i}=\underline{y}^{\top}A\underline{x}
$$
And since
$$
(\underline{v}_{i},\underline{v}_{j})=(\underline{v}_{j},\underline{v}_{i})
$$
$A_{ij}=A_{ji}$, so[[Transpose| $A^{\top}=A$]], so $A$ is symmetric, using the p
## Examples
Consider $V=\mathbb{R}^{2}$, and $(\underline{x},\underline{y})=x_{1}y_{1}+x_{1}y_{2}+x_{2}y_{1}+2x_{2}y_{2}$ 
Is this an inner product? We can see it is symmetric and bilinear by inspection, is it positive definite? We can work this out by considering $(\underline{x},\underline{x})$:
$$
x_{1}^{2}+2x_{1}x_{2}+2x_{2}^{2}=(x_{1}+x_{2})^{2}+x_{2}^{2}\geq 0\forall x_{1},x_{2}\in \mathbb{R}
$$
The only way that it could be zero is if both $x_{2}=0$ and $x_{1}+x_{2}=0$, so if $x_{1}=0$ also, so yes this is positive definite
Now we can consider the matrix form, $A_{ji}=(\underline{v}_{i},\underline{v}_{j})$, so
$$
A=\begin{pmatrix}
1&1\\1&2
\end{pmatrix}
$$
And 
$$
(\underline{x},\underline{y})=\begin{pmatrix}
y_{1}&y_{2}
\end{pmatrix}\begin{pmatrix}
1&1\\1&2
\end{pmatrix}\begin{pmatrix}
x_{1}\\x_{2}
\end{pmatrix}=\underline{y}^{\top}A\underline{x}
$$
$A$ is symmetric, and $A$ is [[Positive Definite Matrices|positive definite]] by Sylvester Criteria, since $A_{1}=(1),\det (A_{1})>0$, and 
$$
A_{2}=\begin{pmatrix}
1&1\\1&2
\end{pmatrix},\det(A_{2})>0
$$
____
Consider $V=\mathbb{R}[x]_{1}=\left\{ p(x)=p_{0}+p_{1}x |p_{0},p_{1}\in\mathbb{R}\right\}$, $\mathbb{R}[x]_{1}$ and more generally $\mathbb{R}[x]_{n}$ are [[Dimension|finite dimensional]] [[Subspaces|vector subspaces]] of $C[a,b]$, the space of continuous functions on an [[Intervals|interval]], and $(f,g)=\int ^{b}_{a} f(t)g(t) \, dt$ defines an inner product on $C[a,b]$, so it also gives an inner product on $\mathbb{R}[x]_{n}$
Fix $a=0,b=1$, then
$$
(p(x),q(x))=\int_{0}^{1} p(x)q(x) \, dx =\int_{0}^{1} (p_{0}+p_{1}x)(q_{0}+q_{1}x) \, dx 
$$
$$
= \int_{0}^{1} p_{0}q_{0}+(p_{0}q_{1}+p_{1}q_{0})x+p_{1}q_{1}x^{2} \, dx =p_{0}q_{0}+ \frac{p_{0}q_{1}+q_{0}p_{1}}{2}+\frac{p_{1}q_{1}}{3}
$$
$$
= \begin{pmatrix}
q_{0}&q_{1}
\end{pmatrix}\begin{pmatrix}
1&\frac{1}{2}\\\frac{1}{2}&\frac{1}{3}
\end{pmatrix}\begin{pmatrix}
p_{0}\\p_{1}
\end{pmatrix}
$$
So 
$$
A=\begin{pmatrix}
1&\frac{1}{2}\\\frac{1}{2}&\frac{1}{3}
\end{pmatrix}
$$
This is symmetric and positive definite


