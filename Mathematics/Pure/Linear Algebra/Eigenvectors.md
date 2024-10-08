To find eigenvectors for a given [[Eigenvalues|eigenvalue]] $\lambda$ for a square matrix, substitute $\lambda$ into:
$$
\begin{pmatrix}
a_{11}-\lambda && a_{12} && \dots && a_{1n} \\
a_{21} && a_{22}-\lambda && \dots && a_{2n} \\
\vdots && \vdots && \ddots && \vdots \\
a_{n1} && a_{n 2} && \dots && a_{nn}-\lambda
\end{pmatrix}
\begin{pmatrix}
x_{1} \\ x_{2} \\ \vdots \\ x_{n}
\end{pmatrix}=\begin{pmatrix}
0\\0\\\vdots\\0
\end{pmatrix}
$$
which will generate a set of linear equations, and any values of $x_{1}, x_{2}, \dots, x_{n}$ that satisfies every linear equation will be an eigenvector for $\lambda$ if there are any free parameters, then that value of $x_{k}$ will be 0 

#Mathematics 