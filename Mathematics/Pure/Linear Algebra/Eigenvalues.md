Eigenvalues are associated with [[Eigenvectors]], and represent a special set of scalar values associated with the system of linear equations such that, for a matrix $A$: 
$$
A \underline{x}=\lambda \underline{x}
$$
Where $\lambda$ is an eigenvalue of $A$, and $\underline{x}$ is an eigenvector of $A$ corresponding to $\lambda$
## Square Matrices
To calculate eigenvalues for an $n\times n$ square matrix, we use the following method:
If A has an invariant line through the origin, then for some non-zero eigenvector, we can say 
$$
\begin{pmatrix}
a_{11} && a_{12} && \dots && a_{1n} \\
a_{21} && a_{22} && \dots && a_{2n} \\
\vdots && \vdots && \ddots && \vdots \\
a_{n1} && a_{n 2} && \dots && a_{nn}
\end{pmatrix}
\begin{pmatrix}
x_{1} \\ x_{2} \\ \vdots \\ x_{n}
\end{pmatrix}=\lambda\begin{pmatrix}
x_{1} \\ x_{2} \\ \vdots \\ x_{n}
\end{pmatrix}=\begin{pmatrix}
\lambda && 0&& \dots&&0 \\
0&&\lambda&&\dots &&0 \\
\vdots && \vdots && \lambda && \vdots \\
0&&0&&\dots&&\lambda
\end{pmatrix}\begin{pmatrix}
x_{1} \\ x_{2} \\ \vdots \\ x_{n}
\end{pmatrix}
$$
$$
\implies \begin{pmatrix}
a_{11} && a_{12} && \dots && a_{1n} \\
a_{21} && a_{22} && \dots && a_{2n} \\
\vdots && \vdots && \ddots && \vdots \\
a_{n1} && a_{n 2} && \dots && a_{nn}
\end{pmatrix}
\begin{pmatrix}
x_{1} \\ x_{2} \\ \vdots \\ x_{n}
\end{pmatrix}-\begin{pmatrix}
\lambda && 0&& \dots&&0 \\
0&&\lambda&&\dots &&0 \\
\vdots && \vdots && \lambda && \vdots \\
0&&0&&\dots&&\lambda
\end{pmatrix}\begin{pmatrix}
x_{1} \\ x_{2} \\ \vdots \\ x_{n}
\end{pmatrix}=\begin{pmatrix}
0\\0\\\vdots\\0
\end{pmatrix}
$$
By distributivity:
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
Which means we have $(A-\lambda I)$ multiplying by a non-zero vector and getting the zero vector, meaning that $A-\lambda I$ is singular and hence $\det(A-\lambda I)=0$, which will give a polynomial of degree $n$, known as the characteristic equation, and hence $n$ eigenvalues each with their own eigenvectors
### Geometrical Interpretations
#### Reflection
Consider a $3\times{3}$ matrix $M$ that represents a reflection, we know that $\det M=-1$ as orientation is not preserved and volume doesn\'t change. We know its eigenvalues must be 1, 1 and -1 as there is an eigenplane which is unaffected by the transformation and then the other is for the invariant lines which represent the reflection perpendicular to the plane. To find the plane of reflection of a matrix, solve
$$
M\underline{x}=1\underline{x}\implies(M-I)\underline{x}=\underline{0}
$$
#### Rotation
For a $2\times 2$ rotation matrix, the two eigenvalues will be real for $0^{\circ}$ or $180^{\circ}$, for $0^{\circ}$, they will be 1 and 1, for $180^{\circ}$, they will be -1 and -1, and for both, the entire plane will be the set of eigenvectors
For a $3\times 3$ rotation matrix, one eigenvalue will be 1 and the other two will be complex, the eigenvectors will be a zero vector with a non-zero value for the axis of rotation, so for example for a rotation about the $z-$axis, an eigenvector would be:
$$
\begin{pmatrix}
0\\0\\1
\end{pmatrix}
$$

#Mathematics #LinAlg 