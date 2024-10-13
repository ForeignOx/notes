If we consider a $2\times 2$ matrix, $M$ which represents a transformation, if we consider its two [[Eigenvectors]], any point on the invariant line represented by the eigenvector, will be moved to that point multiplied by the corresponding [[Eigenvalues|eigenvalue]] for that eigenvector. Another way of thinking about this is that the matrix transforms the coordinate axis to the invariant lines, then multiplies the values linearly, then converts the axes back. We write this like so:
$$
M=PDP^{-1}
$$
Where $P$ is a matrix of the eigenvectors in columns and $D$ is a diagonal matrix of the respective eigenvalues for the eigenvector's column, for example for a matrix with eigenvalues $\lambda_{1}$ and $\lambda_{2}$ with respective eigenvectors $(a_{1},a_{2})$ and $(b_{1},b_{2})$:
$$
P=\begin{pmatrix}
a_{1} && b_{1} \\
a_{2} &&b_{2}
\end{pmatrix}
$$
$$
D=\begin{pmatrix}
\lambda_{1} && 0\\ 0&& \lambda_{2}
\end{pmatrix}
$$
This extends into further dimensions
Now consider $M^{2}$
$$
M^{2}=(PDP ^{-1})(PDP ^{-1})=PD(PP ^{-1})DP ^{-1}=PDIDP ^{-1}=PD^{2}P ^{-1}
$$
This extends to the general case:
$$
M^{n}=PD^{n}P ^{-1}
$$
If the eigenvectors are mutually perpendicular and have unit length, then $P ^{-1}=P^{T}$ and hence
$$
M=PDP^{T}
$$

#Mathematics #LinAlg 