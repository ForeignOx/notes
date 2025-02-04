## Real Inner Products
An inner product on a [[Real Vectorspaces|real vectorspace]] $V$ is a [[Linear Maps|map]] $(\cdot,\cdot):V\times V\mapsto \mathbb{R}$, which assigns each pair of vectors $\underline{u},\underline{v}\in V$ a [[Real Numbers|real number]] $(\underline{u},\underline{v})$, satisfying the following for all $\underline{u},\underline{v},\underline{w}\in V$, $\lambda \in\mathbb{R}$:
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
## Hermitian Inner Product
This is a way to extend the concept of an inner product to complex numbers, which still satisfies positivity. The solution to this is called a Hermitian Inner Product, and is defined on a complex vectorspace is a mapping
$$
\left< , \right>:V\times V\to \mathbb{C}
$$
$$
 \underline{u},\underline{v}\mapsto \left< \underline{u},\underline{v} \right> \in \mathbb{C}
$$
For $\underline{u},\underline{v}\in V$ such that:
- $\left< \underline{v},\underline{u} \right>= \overline{\left< \underline{u},\underline{v} \right>}$ (Hermiticity)
- $\left< \underline{u}+\underline{v},\underline{w} \right>=\left< \underline{u},\underline{w} \right> +\left< \underline{v},\underline{w} \right>$
- $\left< \lambda \underline{u},\underline{v} \right>=\lambda \left< \underline{u},\underline{v} \right>$ (this and previous, make linear in first argument)
- $\left< \underline{v},\underline{v} \right>\geq 0$ with $\left< \underline{v},\underline{v} \right> =0\iff \underline{v}=\underline{0}$
Why is $\left< \underline{v},\underline{v} \right>\in\mathbb{R}$, it follows from the first point that swapping the vectors gives the conjugate, so they must map to $\mathbb{R}$
- $\left< \underline{v},\underline{v} \right>\in\mathbb{R}$
Note that $\left< , \right>$ is not quite linear in its second argument, we can use property $\hspace{0pt}1$ to show that $\left< \underline{u},\lambda \underline{v} \right> =\overline{\left< \lambda \underline{v},\underline{u} \right> }$ then by the third property is equal to $\overline{\lambda \left< \underline{v},\underline{u} \right>}=\overline{\lambda}\overline{\left< \underline{v},\underline{u} \right>}$, which by the first property is then equal to $\overline{\lambda}\left< \underline{u},\underline{v} \right>$
- $\left< \underline{u},\lambda \underline{v} \right>=\overline{\lambda}\left< \underline{u},\underline{v} \right>$
The property of linearity in first argument, and complex-conjugate-linearity in second is called sesquilinearity
As for a real inner product, fix a basis $\left\{ \underline{v}_{1},\dots,\underline{v}_{n} \right\}$ of $V$,
$$
\underline{u}=\sum_{ i=1} ^{ n}  x_{i}\underline{v}_{i},\underline{v}=\sum_{ j=1} ^{ n}  y_{j}\underline{v}_{j}
$$
With $x_{i},y_{j}\in\mathbb{C}$, so
$$
\left< \underline{u},\underline{v} \right> =\sum_{ i=1} ^{ n}  \sum_{ j=1} ^{ n}  \overline{y}_{j}\left< \underline{v}_{i},\underline{v}_{j} \right> x_{i}
$$
$$
= \sum_{ i=1} ^{ n}  \sum_{ j=1} ^{ n}  \overline{y}_{j}B_{ji}x_{i}=(\overline{\underline{y}})^{\top}B\underline{x}
$$
$$
= \underline{y}^{*}B\underline{x}
$$
$$
\left< \underline{u},\underline{v} \right> =\begin{pmatrix}
\overline{y}_{1}&\overline{y}_{2}&\dots&\overline{y}_{n}
\end{pmatrix}\begin{pmatrix}
B_{11}
\end{pmatrix}
$$
Where $B_{ji}=\left< \underline{v}_{i},\underline{v}_{j} \right>\in\mathbb{C}$, and $\underline{y}^{*}=(\overline{\underline{y}})^{\top}$, so $B$ is the matrix representation of $\left< , \right>$ in the basis $\left\{ v_{i} \right\}$
$B$ must satisfy $B=(\overline{B})^{\top}=B^{*}$, called the hermitian transpose, or the conjugate transpose, or the hermitian conjugate, sometimes written $B^{\dagger}$ 

