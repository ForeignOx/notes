A real vectorspace is a non-empty set $V$ with two operations, addition:
$$
V\times V\to V
$$
$$
(\vec{u},\vec{v})\mapsto \vec{u}+\vec{v}
$$
And scalar multiplication by a [[Real Numbers|real number]] (hence real vectorspace):
$$
\mathbb{R}\times V\to V
$$
$$
 (\lambda,\vec{v})\mapsto\lambda \vec{v}
$$
And must satisfy these axioms:
We often refer to elements of $V$ as [[Vectors|vectors]]
## Axioms for Vector Addition
$\hspace{0pt}1$. Existance of Additive identity - there exists an additive identity
$$
\vec{0}\in V: \vec{0}+\vec{v}=\vec{v}+\vec{0}=\vec{v} \,\,\,\, \forall \vec{v} \in V
$$
$\hspace{0pt}2$. Commutativity 
$$
\forall  \vec{w},\vec{v} \in V,\vec{v}+\vec{w}=\vec{w}+\vec{v}
$$
$\hspace{0pt}3$. Existance of Additive Inverse
$$
\forall \vec{v} \in V \exists (-\vec{v})\in V:\vec{v}+(-\vec{v})=(-\vec{v})+\vec{v}=\vec{0}
$$
$\hspace{0pt}4$. Associativity
$$
\forall \vec{u},\vec{v},\vec{w} \in V,(\vec{u}+\vec{v})+\vec{w}=\vec{u}+(\vec{v}+\vec{w})
$$
Using axioms $\hspace{0pt}1$,$\hspace{0pt}3$,$\hspace{0pt}4$, we know that $(V,+)$ is a [[groups|group]]
Using all four axioms we know that $(V,+)$ is an [[Abelian Groups|abelian group]] 
## Axioms for Scalar Multiplication
$\hspace{0pt}1$. Multiplication by 0
$$
0 \vec{v}=\vec{0}\forall \vec{v}\in V
$$
$\hspace{0pt}2$. Multiplication by 1
$$
1\vec{v}=\vec{v}\forall \vec{v}\in V
$$
$\hspace{0pt}3$. Associativity
$$
\lambda(\mu \vec{v})=(\lambda\mu)\vec{v}\,\forall\lambda,\mu \in \mathbb{R},\forall \vec{v}\in V
$$
$\hspace{0pt}4$. Distributivity
$$
(\lambda+\mu)\vec{v}=\lambda \vec{v}+\mu \vec{v}\,\forall\lambda,\mu \in \mathbb{R},\forall \vec{v}\in V
$$
$$
\lambda(\vec{v}+\vec{w})=\lambda \vec{v}+\lambda \vec{w}\,\forall\lambda \in \mathbb{R},\forall \vec{v},\vec{w}\in V
$$
## Examples
- [[Vectorspace Rn|$\mathbb{R}^{n}$]] is an important vectorspace
- [[Subspaces|Subspaces]] of $\mathbb{R}^{n}$ are vectorspaces
- [[Matrices|$M_{m\times n}(\mathbb{R})$]] form a vectorspace under matrix addition and scalar multiplication
And a useful one is
$$
V=\{ f:[0,1]\to \mathbb{R}\mid f\text{ is continuous} \}
$$
Is a vectorspace under the operations:
$$
V\times V\to V
$$
$$
 (f,g)\mapsto f+g
$$
$$
 \mathbb{R}\times V\to V
$$
$$
 (\lambda,f)\mapsto\lambda f
$$
It is straightforward to check that this $V$ under these operations satisfies the axioms, the $\hspace{0pt}0$ vector in $B$ is the $\hspace{0pt}0$ function: $0:[0,1]\to \mathbb{R},0(t)=0\forall0\leq t\leq 1$
Another similar one:
$$
V=\{ f:[0,1]\to \mathbb{R}\mid f\text{ is differentiable} \}
$$
And another:
$$
V=\{ f:[0,1]\to \mathbb{R} \}
$$
Or even:
$$
V=\{ f:\mathbb{R}\to \mathbb{R} \}
$$
The only thing that is important in these examples is that the functions map to the reals, which is necessary to have $f\in V\implies\lambda f\in V$
Or we can be more restrictive:
$$
\mathbb{R}[x]_{n}=\{ \text{polynomials with real valued coefficients of degree }n \}
$$
$$
= \{ a_{0}+a_{1}x+a_{2}x^{2}+\dots+a_{n}x^{n}\mid a_{i}\in \mathbb{R},0\leq i\leq n \}
$$
$$
\mathbb{R}[x]=\{ \text{polynomials with real-valud coefficients} \}=\bigcup_{n=0}^{\infty}\mathbb{R}[x]_{n}
$$
$\mathbb{R}[x]_{n}$ and $\mathbb{R}[x]$ are both vectorspaces under usual addition and scalar multiplication, i.e. if:
$$
p=a_{0}+a_{1}x+\dots+a_{n}x^{n}
$$
$$
 q=b_{0}+b_{1}x+\dots+b_{n}x^{n}
$$
$$
\lambda \in \mathbb{R}
$$
Then:
$$
p+q=(a_{0}+b_{0})+(a_{1}+b_{1})x+\dots+(a_{n}+b_{n})x^{n}
$$
$$
 \lambda p=(\lambda a_{0})+(\lambda a_{1})x+\dots+(\lambda a_{n})x^{n}
$$
## Finite Dimensional Vectorspaces
We call a vectorspace finite dimensional iff it has a finite [[basis|basis]]
What is the dimension of a finite dimensional vectorspace? Our test can be that we want $\text{dim}(\mathbb{R}^{n})=n$

#Mathematics #LinAlg #Definition