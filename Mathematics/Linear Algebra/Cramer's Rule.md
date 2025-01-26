Suppose we have [[Systems of Linear Equations|$A\vec{x}=\vec{b}$]] for [[Matrices|$A\in M_{n}(\mathbb{R})$]] and [[Determinants|$\det(A)\neq 0$]]; $A$ is [[Matrix Inverses|invertible]]
The unique solution to $A\vec{x}=\vec{b}$ is given by:
$$
x_{i}=\frac{\det(\vec{a_{1}},\dots,\vec{a}_{i-1},\vec{b},\vec{a}_{i+1},\dots,\vec{a_{n}})}{\det(A)}
$$
Where:
$$
A=\begin{pmatrix}
\vec{a_{1}}&\vec{a_{2}}&\dots&\vec{a_{n}}
\end{pmatrix}
$$
Where each $\vec{a_{i}}$ are column [[Vectors|vectors]]
## Proof
$A\vec{x}=\vec{b}$, so, using what we know about the [[Adjoint Matrix|adjoint matrix]],
$$
\vec{x}=A^{-1}\vec{b}=\frac{1}{\det(A)}\text{Adj}(A)\vec{b}
$$
$$
\implies x_{i}=\frac{1}{\det(A)}\sum_{ k=1} ^{ n}  \text{Adj}(A)_{ik}b_{k}=\frac{1}{\det(A)}\sum_{ k=1} ^{ n}  (-1)^{i+k}b_{k}\det(A_{k,i})
$$
$$
=\frac{\det(\vec{a_{1}},\dots,\vec{a}_{i-1},\vec{b},\vec{a}_{i+1},\dots,\vec{a_{n}})}{\det(A)}
$$
We get the numerator by performing the expansion of $\det$ along the $i$th column

#Mathematics #LinAlg #Theorem 