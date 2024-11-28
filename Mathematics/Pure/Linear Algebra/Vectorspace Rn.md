$\mathbb{R}^n$ is the [[Real Vectorspaces|vectorspace]] of the [[Real Numbers|real numbers]]
## Definition
$n$-dimensional real space
$$
\mathbb{R}^n:=\left\{  \vec{x}=\begin{pmatrix}
x_{1}\\x_{2}\\\vdots\\ x_{n}
\end{pmatrix}:x_{i}\in \mathbb{R},0\leq i\leq n  \right\}
$$
There are two operations on $\mathbb{R}^n$
$\hspace{0pt}1$. Vector addition
$$
\mathbb{R}^n\times \mathbb{R}^n\to \mathbb{R}^n
$$
$$
(\vec{v},\vec{w})\mapsto  \vec{v}+\vec{w}
$$
$$
\vec{v}+\vec{w}=\begin{pmatrix}
v_{1}\\v_{2}\\\vdots\\v_{n}
\end{pmatrix}
+
\begin{pmatrix}
w_{1}\\w_{2}\\\vdots\\w_{n}
\end{pmatrix}=
\begin{pmatrix}
v_{1}+w_{1}\\v_{2}+w_{2}\\\vdots\\v_{n}+w_{n}
\end{pmatrix}
$$
$\hspace{0pt}2$. Scalar multiplication
$$
\mathbb{R}\times\mathbb{R}^n\to \mathbb{R}^n
$$
$$
(\lambda,\vec{v})\mapsto\lambda \vec{v}
$$
$$
\lambda \vec{v}=\lambda \begin{pmatrix}
v_{1}\\v_{2}\\\vdots\\v_{n}
\end{pmatrix}=\begin{pmatrix}
\lambda v_{1}\\\lambda v_{2}\\\vdots\\\lambda v_{n}
\end{pmatrix}
$$
These operations satisfy the axioms of a real vectorspace
The vectorspace $\mathbb{R}^n$ quite obviously satisfies the vectorspace axioms, especially when you consider:
$$
-\vec{v}=(-1)\begin{pmatrix}
v_{1}\\v_{2}\\\vdots\\v_{n}
\end{pmatrix}=
\begin{pmatrix}
-v_{1}\\-v_{2}\\\vdots\\-v_{n}
\end{pmatrix}
$$
## Is $\mathbb{R}=\mathbb{R}^1$?
There is a very obvious bijection between the two [[sets|sets]], but the set $\mathbb{R}^1$ technically has fewer operations soooooooooooooooooooooo nuh uh. except that other guy said yuh uh sooooooo idk \shrugh
## Basis?
$\{ e_{1},\dots,e_{n}q\subseteq \mathbb{R}^{n}  \}\subseteq \mathbb{R}^{n}$ is the standard base, other bases exist, for example, we shaw that:
$$
\left\{  
\begin{pmatrix}
1\\0
\end{pmatrix},\begin{pmatrix}
1\\1
\end{pmatrix}
 \right\}\in \mathbb{R}^{2}
$$

Is a spanning set for $\mathbb{R}^{2}$, since $\text{dim}(\mathbb{R}^{2})=2$, tiis $B$ is in vact a basis for $\mathbb{R}^{2}$

## Thrm
Suppose $\{ \vec{u}_{1},\dots,\vec{u}_{r} \}\subseteq \mathbb{R}^{n}$, then
If $r>n$, then $\{ \vec{u}_{1},\dots,\vec{u}_{r} \}$ is not linearly independent
If $r<n$, then $\{ \vec{u}_{1},\dots,\vec{u}_{r} \}$ is not spanning
Suppose $r=n$, we have that $\{ \vec{u}_{1},\dots,\vec{u}_{r} \}$ is a basis iff:
$$
A=\begin{pmatrix}
\vec{u}_{1}&\vec{u}_{2}&\dots&\vec{u}_{n}
\end{pmatrix}\in M_{n}(\mathbb{R})
$$
Is non-singular iff $\det(A)\neq 0$
### Proof
The first two are just the previous theorem
The third one: $\{ \vec{u}_{1},\dots,\vec{u}_{r} \}$ is a basis iff $\{ \vec{u}_{1},\dots,\vec{u}_{r} \}$ is linearly independent (again by previous theorem) iff
$$
\lambda_{1}\vec{u}_{1}+\dots+\lambda_{n}\vec{u}_{n}\implies\lambda_{1}+\dots+\lambda_{n}\vec{u}_{n}=\vec{0}\iff \vec{\lambda}=\vec{0}
$$
iff $A$ is invertible; $\det(A)\neq 0$



#Mathematics #LinAlg #Definition