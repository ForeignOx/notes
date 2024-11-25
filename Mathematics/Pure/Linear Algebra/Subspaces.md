A non-[[Empty Set|empty]] [[Subsets|subset]] of $U$ of a [[Real Vectorspaces|vectorspace]] is called a vectorsubspace or linear subspace or subspace if it satisfies the following conditions, and is itself a vectorspace:
- If $\vec{u},\vec{v}\in U$, then $\vec{u}+\vec{v}\in U$ (closure under addition)
- If $\vec{u}\in U,\lambda \in\mathbb{R}$, then $\lambda \vec{u}\in U$ (closure under scalar multiplication)
- $\{ \vec{0} \}\in U$ (existence of 0)
## Examples
Trivial cases:
$\{ \vec{0} \}\subseteq U$ is a subspace of $U$ and is called the trivial subspace and is sometimes written $0=\{ \vec{0} \}$
$U\subseteq U$ is a subspace of $U$ fairly obviously
Non-trivial cases for [[Vectorspace Rn|$\mathbb{R}^{n}$]]:
Suppose $\vec{d}\in\mathbb{R}^{n}$, $\vec{d}\neq  \vec{0}$, then $L=\{ \lambda \vec{d}\mid\lambda \in\mathbb{R} \}$ (a line through the origin in direction $\vec{d}$) is a subspace of $\mathbb{R}^{n}$, $L\subseteq \mathbb{R}^{n}$ and:
- $\lambda_{1}\vec{d}+\lambda_{2}\vec{d}=(\lambda_{1}+\lambda_{2})\vec{d}\in L$
- $\lambda(\mu \vec{d})=(\lambda\mu)\vec{d} \in L$
- $\vec{0}=0\vec{d} \in L$
Suppose $\vec{a},\vec{b}\in\mathbb{R}$, and they are not multiples of each oter, then $\Pi=\{ \lambda \vec{a}+\mu \vec{b}\mid\lambda,\mu \in\mathbb{R} \}\subseteq \mathbb{R}^{n}$ is a subspace of $\mathbb{R}^{n}$
Note if we had $\Pi=\{ \vec{c}+\lambda \vec{a}+\mu \vec{b}\mid\lambda,\mu \in\mathbb{R} \}\subseteq \mathbb{R}^{n}$, this may not necessarily be a subspace as it may not contain $\vec{0}$, and similarly for other lines not going through the origin. These are called affine subspaces
### Proposition
Suppose [[Matrices|$A\in M_{m\times n}(\mathbb{R})$]], then the solution set $S\subseteq \mathbb{R}^{n}$ to the homogeneous [[Systems of Linear Equations|system of linear equations]] $A\vec{x}=\vec{0}$ is a linear subspace of $\mathbb{R}^{n}$
#### Proof
$$
S=\{ \vec{x}\in \mathbb{R}^{n}\mid A\vec{x}=\vec{0} \}
$$
Then if $\vec{u},\vec{v}\in S$, we have 
$$
A(\vec{u}+\vec{v})=A\vec{u}+A\vec{v}=0+0=0
$$
So $\vec{u}+\vec{v}\in S$
If $\vec{u}\in S,\lambda \in\mathbb{R}$, 
$$
A(\lambda \vec{u})=\lambda A\vec{u}=\lambda0=0
$$
So $\lambda \vec{u}\in S$
And finally $\vec{0}\in S$ as $A\vec{0}=\vec{0}$
## [[span|Spans]]
If $\vec{u}_{1},\vec{u}_{2},\dots,\vec{u}_{k}\in\mathbb{R}^{n}$ then $U=\text{span}<\vec{u}_{1},\vec{u}_{2},\dots,\vec{u}_{k}> \subseteq V$ is a subspace of $V$
### Proof
Check conditions to be a subspace:
$\hspace{0pt}1$. Suppose $\lambda \vec{u}_{1}+\dots+\lambda_{k}\vec{u}_{k},\mu_{1}\vec{u}_{1}+\dots+\mu_{k}\vec{u}_{k}\in U$, then
$$
(\lambda_{1} \vec{u}_{1}+\dots+\lambda_{k}\vec{u}_{k})+(\mu_{1}\vec{u}_{1}+\dots+\mu_{k}\vec{u}_{k})=(\lambda_{1}+\mu_{1})\vec{u}_{1}+\dots+(\lambda_{k}+\mu_{k})\vec{u}_{k}\in U
$$
$\hspace{0pt}2$. Suppose $\lambda \vec{u}_{1}+\dots+\lambda_{k}\vec{u}_{k}\in U,\lambda \in\mathbb{R}$, then:
$$
\lambda(\lambda \vec{u}_{1}+\dots+\lambda_{k}\vec{u}_{k})=(\lambda\lambda_{1})\vec{u}_{1}+\dots+(\lambda\lambda_{k})\vec{u}_{k}\in U
$$
$\hspace{0pt}3$. $\vec{0}=0\vec{u}_{1}+\dots+0\vec{u}_{k}\in U$
## Any Vectorspace
If $\vec{u}_{1},\dots,\vec{u}_{r}\in V$, then $\text{span}< \vec{u}_{1},\dots,\vec{u}_{r} >\subseteq V$ is a subspace of $V$ 
### Examples
- $0=\{ \vec{0} \}\subseteq \mathbb{R}^{n}$, $0=\text{span}<\vec{0}>$
- $\mathbb{R}^{n}\subseteq \mathbb{R}^{n}$, $\mathbb{R}^{n}=\text{span}< \vec{e}_{1},\dots,\vec{e}_{n}>$
- $\Pi=\{ \lambda \vec{a}+\mu \vec{b} \mid\lambda,\mu \in\mathbb{R}\}\subseteq \mathbb{R}^{n},\vec{a},\vec{b}\in\mathbb{R}^{n}$, $\Pi=\text{span}<\vec{a},\vec{b}>$
#### Discussion
What is the span inside $\mathbb{R}^{3}$ of 
$$
\vec{u}_{1}=\begin{pmatrix}
1\\1\\1
\end{pmatrix},\vec{u}_{2}=\begin{pmatrix}
-1\\0\\2
\end{pmatrix},\vec{u}_{3}=\begin{pmatrix}
0\\1\\3
\end{pmatrix},\vec{u}_{4}=\begin{pmatrix}
-1\\1\\5
\end{pmatrix}
$$
Let:
$$
A=\begin{pmatrix}
\vec{u}_{1}&\vec{u}_{2}&\vec{u}_{3}&\vec{u}_{4}
\end{pmatrix}\in M_{3\times 4}(\mathbb{R})
$$
Then, given $\vec{b}\in\mathbb{R}^{3}$, we could like to know if $\exists\vec{\lambda}\in\mathbb{R}^{4}$ such that $A\vec{\lambda}=\vec{b}$, so $\vec{b}\in \text{span}<\vec{u}_{1},\vec{u}_{2},\vec{u}_{3},\vec{u}_{4}>:=U$
I.e. when does $A\vec{\lambda}=\vec{b}$ have solutions?
$$
\left(
\begin{array}{cccc|c}
1&-1&0&-1&b_{1}\\
1&0&1&1&b_{2}\\1&2&3&5&b_{3}
\end{array}
\right)\to 
\left(
\begin{array}{cccc|c}
1&0&1&1&b_{2}\\
0&1&1&2&b_{2}-b_{1}\\
0&0&0&0&2b_{1}-3b_{2}+b_{3}
\end{array}
\right)
$$
By using [[Gauss-Jordan Elimination|Gauss-Jordan elimination]], so we have solutions exactly when $2b_{1}-3b_{2}+b_{3}=0$, so:
$$
U=\left\{  \begin{pmatrix}
b_{1}\\b_{2}\\b_{3}
\end{pmatrix}\mid2b_{1}-3b_{2}+b_{3}=0  \right\}
$$
$U$ is a plane inside $\mathbb{R}^{3}$passing through the origin of normal vector
$$
\begin{pmatrix}
2\\-3\\1
\end{pmatrix}
$$
Also 
$$
U=\text{span}<\vec{u}_{1},\vec{u}_{2},\vec{u}_{3},\vec{u}_{4}> =\text{span}<\vec{u}_{1},\vec{u}_{2}>=\text{span}<\vec{u}_{i},\vec{u}_{j}>
$$
where $i\neq j$, $1\leq i,j\leq 4$ (since $U$ is a plane)
## Examples
$\mathbb{R}^{1}=\mathbb{R}$ is a vectorspace, $\mathbb{Z},\mathbb{Q}\subseteq \mathbb{R}$, $\mathbb{Z}$ and $\mathbb{Q}$ are not subspaces, as they are not closed under scalar multiplication, as for example, $1\in\mathbb{Z},\mathbb{Q}$, but $\sqrt{ 2 }=\sqrt{ 2 }\times 1\not\in\mathbb{Z}$ or $\mathbb{Q}$ 
$\mathbb{R}[x]_{n}\subseteq \mathbb{R}[x]_{n+1}\subseteq \mathbb{R}[x]$, are subspaces
Function spaces:
$$
\{ f:[0,1]\to \mathbb{R}\mid \text{conditions} \}
$$
Are subspaces of each other if the conditions are strict enough
A subspace of $M_{n}(\mathbb{R})$ is the symmtric matrices:
$$
\text{sym}_{n}(\mathbb{R}):=\{ A\in M_{n}(\mathbb{R}) \mid A^{t}=A\}
$$
### Proof
$0\in M_{n}(\mathbb{R})$ as the $\hspace{0pt}0$ matrix, as $0^{t}=0$
Suppose $A,B\in \text{sym}_{n}(\mathbb{R})$, then $(A+B)^{t}=A^{t}B^{t}$, so we have closeure under addition
$$
A \in  \text{sym}_{n}(\mathbb{R}),\lambda \in \mathbb{R}
$$
$$
(\lambda A)^{t}=\lambda(A)^{t}=\lambda A
$$
So we have closure under scalar multiplication
___
The set of even polynomials (only even powers of $x$), $\mathbb{R}[x]_\text{even}\subseteq \mathbb{R}[x]$ is a subspace of $\mathbb{R}[x]$

#Mathematics #LinAlg #Definition 