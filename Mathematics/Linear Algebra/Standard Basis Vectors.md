These are [[Vectors|Vectors]] in [[Vectorspace Rn|$\mathbb{R}^n$]], and for $1\leq i\leq n$, we define $\vec{e}_{i}\in\mathbb{R}^n$ by:
$$
\vec{e}_{1}=\begin{pmatrix}
1\\0\\\vdots\\0
\end{pmatrix}
$$
$$
\vec{e}_{2}=\begin{pmatrix}
0\\1\\\vdots\\0
\end{pmatrix}
$$
$$
\vdots
$$
$$
\vec{e}_{n}=\begin{pmatrix}
0\\0\\\vdots\\1
\end{pmatrix}
$$
![[Standard Basis Vectors 2024-10-08 11.17.26.excalidraw]]
Where the $i$th term from the top is a $\hspace{0pt}1$
We can express any vector $\vec{x}\in\mathbb{R}^n$ uniquely as a linear combination of the standard basis vectors, i.e:
$$
\vec{x}=\begin{pmatrix}
x_{1}\\x_{2}\\\vdots\\x_{n}
\end{pmatrix}=x_{1}\begin{pmatrix}
1\\0\\\vdots\\0
\end{pmatrix}+x_{2}\begin{pmatrix}
0\\1\\\vdots\\0
\end{pmatrix}+\dots+x_{n}\begin{pmatrix}
0\\0\\\vdots\\1
\end{pmatrix}=x_{1}\vec{e}_{1}+x_{2}\vec{e}_{2}+\dots+x_{n}\vec{e}_{n}
$$
The $x_{i}$ terms, the coefficiets are sometimes called the cartesian coordinates of the vector $\vec{x}$

#Mathematics #LinAlg #Definition