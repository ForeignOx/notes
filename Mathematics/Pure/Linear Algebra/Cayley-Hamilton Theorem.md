Any square matrix satisfies its own [[Eigenvalues|characteristic equation]]
## Proof
Consider a general square matrix $M$ with characteristic equation $f(\lambda)=0$
$$
f(M)=a_{0}I+a_{1}M+a_{2}M^{2}+\dots+a_{n}M^{n}
$$
$$
= a_{0}PIP ^{-1}+a_{1}PDP ^{-1}+a_{2}PD^{2}P ^{-1}+\dots+a_{n}PD^{n}P ^{-1}
$$
$$
= P(a_{0}I+a_{1}D+a_{2}D^{2}+\dots+a_{n}D^{n})P ^{-1}
$$
$$
= P \begin{pmatrix}
f(\lambda_{1}) && 0 && \dots&&0 \\
0 && f(\lambda_{2}) && \dots &&0 \\
\vdots &&\vdots&&\ddots&&\vdots\\
0&&0&&\dots &&f(\lambda_{n})
\end{pmatrix}P ^{-1}
$$
$$
=P \underline{0}P ^{-1}=\underline{0}
$$

#Mathematics #LinAlg #Theorem