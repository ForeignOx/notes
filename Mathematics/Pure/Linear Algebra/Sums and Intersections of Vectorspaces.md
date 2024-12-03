Suppose $V$ is a [[Real Vectorspaces|vectorspace]], and $U,W\subseteq V$ are [[Subspaces|subspaces]], then
$$
U+W:=\{ \vec{u}+\vec{w}\mid \vec{u}\in U,\vec{w}\in W \}\subseteq V
$$
One can think of the sum as the [[Span|span]] of the union; it is the smallest subspace of $V$ containing $U$ and $W$
$$
U\cap W:=\{ \vec{u}\in V\mid \vec{u}\in U,\vec{u}\in W \}\subseteq V
$$
## Proof
yeh
## Example
Consider two planes $\Pi_{1},\Pi_{2}\in\mathbb{R}^{3}$ through the origin, $\Pi_{1}\cap \Pi_{2}=L$ which is a $\hspace{0pt}1$ dimensional line, $\Pi_{1}+\Pi_{2}=\mathbb{R}^{3}$, which is three-dimensional space. Note that each plane is two-dimensional and the sum of their two dimensions is the sum of the dimensions of the intersection and the sum; $2+2=1+3$
## Proposition
Suppose $U,W\subseteq V$ are finite dimensional subspaces, then $U\cap W$ and $U+W$ are also finite dimensional, and
$$
\dim(U)+\dim(W)=\dim(U+W)+\dim(U\cap W)
$$
### Proof
First note that $U\cap W\subseteq U$ and $U$ is finite dimensional, therefore $U\cap W$ is finite dimensional
Let $\{ \vec{v}_{1},\dots,\vec{v}_{k} \}$ be a basis for $U\cap W$, extend this to a basis $\{ \vec{v}_{1},\dots,\vec{v}_{k},\vec{u}_{1},\dots,\vec{u}_{l} \}$ of $U$
and to a basis of $W$; $\{ \vec{v}_{1},\dots,\vec{v}_{k},\vec{w}_{1},\dots,\vec{w}_{m} \}$
Claim:
$$
B=\{ \vec{v}_{1},\dots,\vec{v}_{k},\vec{u}_{1},\dots,\vec{u}_{l},\vec{w}_{1},\dots,\vec{w}_{m} \}
$$
is a basis for $U+W$, so 
$$
\dim(U+W)+\dim(U\cap W)=(k+l+m)+k=(k+l)+(k+m)=\dim(U)+\dim(W)
$$
Certainly $B$ spans $U+W$, is $B$ linearly independent??
Suppose
$$
\lambda_{1}\vec{v}_{1}+\dots+\lambda_{k}\vec{v}_{k}+\mu_{1}\vec{u}_{1}+\dots+\mu_{l}\vec{u}_{l}+\eta_{1}\vec{w}_{1}+\dots+\eta_{m}\vec{w}_{m}=\vec{0}
$$
So we have
$$
\underbrace{ \lambda_{1}\vec{v}_{1}+\dots+\lambda_{k}\vec{v}_{k}+\mu_{1}\vec{u}_{1}+\dots+\mu_{l}\vec{u}_{l} }_{ \in U }=\underbrace{ -(\eta_{1}\vec{w}_{1}+\dots+\eta_{m}\vec{w}_{m}) }_{ \in W }\in U\cap W
$$
So 
$$
-(\eta_{1}\vec{w}_{1}+\dots+\eta_{m}\vec{w}_{})=\lambda_{1}'\vec{v}_{1}+\dots+\lambda_{k}'\vec{v}_{k}
$$
$$
\implies \lambda_{1}'\vec{v}_{1}+\dots+\lambda_{k}'\vec{v}_{k}+\eta_{1}\vec{w}_{1}+\dots+\eta_{m}\vec{w}_{m}=\vec{0}
$$
But this is is a basis for $W$, so since they are linearly independent, so $\lambda_{1}'=\dots=\lambda_{k}'=\eta_{1}=\dots=\eta_{m}=0$
So the original linear combination becomes:
$$
\lambda_{1}\vec{v}_{1}+\dots+\lambda_{k}\vec{v}_{k}+\mu_{1}\vec{u}_{1}+\dots \mu_{l}\vec{u}_{l}=\vec{0}
$$
Hence $\lambda_{1}=\dots=\lambda_{k}=\mu_{1}=\dots=\mu_{l}=0$
## Example
Consider $V=M_{2}(\mathbb{R})$, $U,L\subseteq V$:
$$
U=\left\{  \begin{pmatrix}
a&b\\0&d
\end{pmatrix}\mid a,b,d\in \mathbb{R}  \right\}\text{ (upper triangular)}
$$
$$
L=\left\{  \begin{pmatrix}
a&0\\c&d
\end{pmatrix}\mid a,c,d\in \mathbb{R}  \right\}\text{ (lower triangular)}
$$
$$
D=U\cap L = \left\{   \begin{pmatrix}
a&0\\0&d
\end{pmatrix}\mid a,d\in \mathbb{R}  \right\}\text{ (diagonal)}
$$
These are each subspaces of $V$, with bases as follows;
For $U$:
$$
\left\{  \begin{pmatrix}
1&0\\0&0
\end{pmatrix},\begin{pmatrix}
0&1\\0&0
\end{pmatrix},\begin{pmatrix}
0&0\\0&1
\end{pmatrix} \right\}
$$
For $L$:
$$
\left\{  \begin{pmatrix}
1&0\\0&0
\end{pmatrix},\begin{pmatrix}
0&0\\1&0
\end{pmatrix},\begin{pmatrix}
0&0\\0&1
\end{pmatrix}  \right\}
$$
For $D$:
$$
\left\{  \begin{pmatrix}
1&0\\0&0
\end{pmatrix},\begin{pmatrix}
0&0\\0&1
\end{pmatrix}  \right\}
$$
So $\dim(U)=3$, $\dim(L)=3$, $\dim(U\cap L)=\dim(D)=2$, $\dim(U+L)=3+3-2=4$, so $U_{L}=M_{2}(\mathbb{R})$
## Direct Sums
Suppose $U,W\subseteq V$ are subspaces that satisfy $U+W=V$, $U\cap W=0=\{ \vec{0} \}$, then we call $V$ the 'direct sum' of $U$  and $W$, and write
$$
V=U \oplus W
$$
## Proposition
If $V$ is finite dimensional, and $U,W\subseteq V$ are subspaces, then the following are pairwise equivalent:
1. $V=U\oplus W$
2. If $\{ \vec{u}_{1},\dots,\vec{u}_{l} \},\{ \vec{w}_{1},\dots,\vec{w}_{k} \}$ are bases for $U$ and $W$ respectively, then $\{ \vec{u}_{1},\dots,\vec{u}_{l},\vec{w}_{1},\dots,\vec{w}_{k} \}$ is a basis for $V$
3. $V=U+W$ and $\dim(V)=\dim(U)+\dim(W)$
4. Every $\vec{v}\in V$ can be written uniquely as $\vec{v}=\vec{u}+\vec{w}$ for some unique choice of $\vec{u}\in U,\vec{w}\in W$

### Proof
$1\iff2\iff 3$ follows from the proposition above, and $1 \iff 4$ is on a problem sheet :(
### Exapmle
$V=M_{n}(\mathbb{R})$, $S=\{ A\in V \mid A^{t}=A \}$, $T=\{ A\in V\mid A^{t} = -A \}$
$S$ is the $n\times n$ symmetric matrices, $T$ is the $n\times n$ antisymmetric matrices
$S,T\subseteq V$ are subspaces, also $V=S\oplus T$
#### Proof
Check definition:
If $A\in V$, then 
$$
A=\underbrace{ \frac{1}{2}(A+A^{t}) }_{ \in S }+\underbrace{ \frac{1}{2}(A-A^{t}) }_{ \in T }
$$
As:
$$
\left( \frac{1}{2}(A+A^{t}) \right)^{t}=\frac{1}{2}(A^{t}+(A^{t})^{t})=\frac{1}{2}(A^{t}+A)
$$
and
$$
\left( \frac{1}{2}(A-A^{t}) \right)^{t}=\frac{1}{2}(A^{t}-(A^{t})^{t})=\frac{1}{2}(A^{t}-A)=-\frac{1}{2}(A-A^{t})
$$
Suppse $A\in S\cap T$, then $A=A^{t}=-A$, so $ZA=0$
