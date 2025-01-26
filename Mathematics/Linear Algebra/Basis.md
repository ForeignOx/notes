A basis for a [[Real Vectorspaces|vectorspace]] $V$ is a finite [[Sets|set]] of [[Vectors|vectors]]:
$$
\{ \vec{v}_{1},\vec{v}_{2},\dots,\vec{v}_{n} \}\subseteq V
$$
Such that:
- $\{ \vec{v}_{1},\vec{v}_{2},\dots,\vec{v}_{n} \}$ is [[Linear Independence|linearly independent]]
- $\{ \vec{v}_{1},\vec{v}_{2},\dots,\vec{v}_{n} \}$ [[Span|spans]] $V$
## Examples
For [[Vectorspace Rn|$\mathbb{R}^{n}$]] $\{\vec{e}_{1},\vec{e}_{2},\dots,\vec{e}_{n} \}$ (the standard basis), is the standard basis for $\mathbb{R}^{n}$
___
For $\mathbb{R}[x]_{n}$,:
$$
\{ 1,x,x^{2},\dots,x^{n} \}\subseteq \mathbb{R}[x]_{n}
$$
Is a basis for $\mathbb{R}[x]_{n}$; if $t\in\mathbb{R}[x]_{n}$, then 
$$
a_{0}+a_{1}x+\dots+a_{n}x^{n}\in \text{span}< 1,x,\dots x^{n} > 
$$
So 
$$
\text{span}< \{ 1,x,x^{2},\dots,x^{n} \} > =\mathbb{R}[x]_{n}
$$
Also if $a_{0}+a_{1}x+\dots+a_{n}x^{n}=0$, then $a_{0}=a_{1}=\dots=a_{n}=0$
Note, for example, $\mathbb{R}[x]$ doesn't have a vbasis, since it doesn't have a finite spanning the set
Are the polynomials $1-x,x-x^{2},1-x^{2}$ a basis for $\mathbb{R}[x]_{2}$? The answer is no, since:
$$
1-x+(x-x^{2})-(1-x^{2})=0
$$
So these elements are not linearly independent
If we write $E^{ij}\in M_{m\times n}(\mathbb{R})$ for the matrix that has $(i,j)$rh entry $\hspace{0pt}1$, and all other entries $\hspace{0pt}0$, then
$$
\{ E^{ij}\mid1\leq i\leq m,1\leq j\leq n \}\subseteq M_{m\times n}(\mathbb{R})
$$
Why? If it is spanning,
$$
A=\left( a_{ij}=\sum_{1\leq i \leq m,1\leq j\leq n} \right)a_{ij}E^ij 
$$
___
$M_{2}(\mathbb{R})$ has a basis $\{ E_{11},E_{12},E_{21},E_{22} \}$
$$
=\left\{  \begin{pmatrix}
1&0\\0& 0
\end{pmatrix}, \begin{pmatrix}
0&1\\0&0
\end{pmatrix},\begin{pmatrix}
0&0\\1&0
\end{pmatrix},\begin{pmatrix}
0&0\\0&1
\end{pmatrix} \right\}
$$
But there are other bases available, such as:
$$
\left\{  \begin{pmatrix}
1&0\\0&0
\end{pmatrix},\begin{pmatrix}
0&0\\0&1
\end{pmatrix},\begin{pmatrix}
0&1\\1&0
\end{pmatrix},\begin{pmatrix}
0&1\\-1&0
\end{pmatrix}  \right\}
$$
To check this, we want to check if it is spanning, so we want to find $\lambda_{1},\lambda_{2},\lambda_{3},\lambda_{4}$ such that:
$$
\begin{pmatrix}
a&b\\c&c
\end{pmatrix}=\lambda_{1}\begin{pmatrix}
1&0\\0&0
\end{pmatrix}+\lambda_{2}\begin{pmatrix}
0&0\\0&1
\end{pmatrix}+\lambda_{3}\begin{pmatrix}
0&1\\1&0
\end{pmatrix}+\lambda_{4}\begin{pmatrix}
0&1\\-1&0
\end{pmatrix}=\begin{pmatrix}
\lambda_{1}&\lambda_{3}+\lambda_{4}\\\lambda_{3}-\lambda_{4}&\lambda_{2}
\end{pmatrix}
$$
So can take:
$$
\lambda_{1}=a,\lambda_{2}=d,\lambda_{3}=\frac{b+c}{2},\lambda_{4}=\frac{b-c}{2}
$$
So they are spanning, now we need to check if they are linearly independent:
$$
\begin{pmatrix}
\lambda_{1}&\lambda_{3}+\lambda_{4}\\\lambda_{3}-\lambda_{4}&\lambda_{2}
\end{pmatrix}=\begin{pmatrix}
0&0\\0&0
\end{pmatrix}
$$
$$
\implies \lambda_{1}=\lambda_{2}=0
$$
and 
$$
\lambda_{3}+\lambda_{4}=0,\lambda_{3}-\lambda_{4}=0
$$
$$
\implies \lambda_{3}=\lambda_{4}=0
$$
## Theorem: What is a Basis???
Suppose $\vec{u}_{1},\dots,\vec{u}_{r}\in V$, then the following are equivalent:
- $\{ \vec{u}_{1},\dots,\vec{u}_{r} \}$ is a basis for $V$
- $\{ \vec{u}_{1},\dots,\vec{u}_{r} \}$ are a maximal linearly independent subset of $V$ (maximal meaning we cannot add another vector to $\{ \vec{u}_{1},\dots,\vec{u}_{r} \}$ and stay linearly independent)
- Any vector $\vec{u}\in V$ can be written uniquely as $\vec{u}=\lambda_{1}\vec{u}_{1}+\dots+\lambda_{r}\vec{u}_{r}$ (unique choice of $\lambda_{i}$'s)
- $\{ \vec{u}_{1},\dots,\vec{u}_{r} \}$ are a minimal spanning set for $V$
### Proof
$1\implies2$:
Assume $1$, first note that $\{ \vec{u}_{1},\dots,\vec{u}_{r} \}$ is linearly independent, so is it maximal? Suppose $\vec{u}\in V$, then $\vec{u}=\lambda_{1}\vec{u}_{1}+\dots+\lambda_{r}\vec{u}_{r}$ for some $\lambda_{i}\in\mathbb{R}$, as $\{ \vec{u}_{1},\dots,\vec{u}_{r} \}$ span $V$
So $\lambda_{1}\vec{u}_{1}+\dots+\lambda_{r}\vec{u}_{r}-\vec{u}= \vec{0}$, hence $\{ \vec{u}_{1},\dots,\vec{u}_{r},\vec{u} \}$ is not linearly independent, so $\{ \vec{u}_{1},\dots,\vec{u}_{r} \}$ are maximal
$2\implies 3$:
Assume $\hspace{0pt}2$, suppose $\exists \vec{u}\in V$ not expressible in this way, this means $\vec{u}\not\in\text{span}< \vec{u}_{1},\dots,\vec{u}_{r} >$. Hence $\{ \vec{u}_{1},\dots,\vec{u}_{r},\vec{u} \}$ is linearly indepnedent, this means $\{ \vec{u}_{1},\dots,\vec{u}_{r} \}$ is not maximal, so we have a contradiction
If we have $\vec{u}=\lambda_{1}\vec{u}_{1}+\dots+\lambda_{r}\vec{u}_{r}$, and $\vec{u}=\mu_{1}\vec{u}_{1}+\dots+\mu_{r}\vec{u}_{r}$ then $(\lambda_{1}-\mu_{1})\vec{u}_{1}+\dots+(\lambda_{r}-\mu_{r})\vec{u}_{r}= \vec{0}$, hence $\lambda_{i}=\mu_{i}$ for $1\leq i\leq r$
$3\implies 4$:
Assume $\hspace{0pt}3$, then $\{ \vec{u}_{1},\dots,\vec{u}_{r} \}$ is spanning since all $\vec{u}\in V$  satisfy $\vec{u}\in \text{span}< \vec{u}_{1},\dots,\vec{u}_{r} >$ is not minimal. Without loss of generality, suppose $V=\text{span}< \vec{u}_{2},\dots,\vec{u}_{r} >$ ten $\vec{u}_{1}=\lambda_{2}\vec{u}_{2}+\dots+\lambda_{r}\vec{u}_{r}$ or some $\lambda_{2},\dots,\lambda_{r} \in\mathbb{R}$, these are two different expressions for $\vec{u}_{1}$ which gives a contradiction :O
$4\implies1$:
Assume $\hspace{0pt}4$, then $\{ \vec{u}_{1},\dots,\vec{u}_{r} \}$ is certainly spanning, but is it linearly independent? Suppose it isn't for a contradiction, then $\exists\lambda_{1},\dots,\lambda _{r}\in\mathbb{R}$, not all $\hspace{0pt}0$ such that $\lambda_{1}\vec{u}_{1}+\dots+\lambda_{r}\vec{u}_{r}= \vec{0}$, if $\lambda _{i}\neq 0$, then 
$$
\vec{u}_{i}=-\frac{-\lambda_{1}}{\lambda_{i}}\vec{u}_{1}+\dots+\frac{-\lambda_{i-1}}{\lambda_{i}}\vec{u}_{i-1}+\frac{-\lambda_{i+1}}{\lambda_{i}}\vec{u}_{i+1}+\dots+\frac{-\lambda_{r}}{\lambda_{i}}\vec{u}_{r}
$$
$$
\in \text{span}< \vec{u}_{1},\dots,\vec{u}_{i-1},\vec{u}_{i+1},\dots,\vec{u}_{r} > 
$$
So $\text{span}< \vec{u},\dots,\vec{u}_{i-1},\vec{u}_{i+1},\dots,\vec{u}_{r} >=\text{span}< \vec{u}_{1},\dots,\vec{u}_{r} >$, so $\text{span}< \vec{u}_{1},\dots,\vec{u}_{r} >$ was not a minimal spanning set

#Mathematics #LinAlg #Definition #Theorem 