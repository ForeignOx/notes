If $A\in M_{n\times k}(\mathbb{R})$, then
## Columnspaces
The columnspace of $A$ is the span inside $\mathbb{R}^{n}$ of the columns of the matrix $A$, i.e. if
$$
A=\begin{pmatrix}
\vec{u}_{1}&\dots&\vec{u}_{k}
\end{pmatrix}
$$
Then $\text{columnspace}(A)=\text{span}< \vec{u}_{1},\dots \vec{u}_{k} >\subseteq \mathbb{R}^{n}$
Another way of thinking about this is that $\text{columnspace(A)}=\{ A\vec{\lambda}\mid\lambda \in\mathbb{R}^{k} \}\subseteq \mathbb{R}^{n}$
## Columnrank
The columnrank of $A$ is the dimension of the columnspace
## Rowspaces
The rowspace of $A$ is the span inside $\mathbb{R}^{n}$ of the rows of the matrix $A$, so it is a subspace of $\mathbb{R}^k$, more honestluk, it's the columnspace of $A^{t}$
$$
A=\begin{pmatrix}
\vec{u}_{1}\\\vdots\\\vec{u}_{k}
\end{pmatrix}
$$
Then $\text{rowspace}(A)=\text{span}< \vec{u}_{1},\dots \vec{u}_{k} >\subseteq \mathbb{R}^{n}$
Another way of thinking about this is that $\text{rowspace(A)}=\{ A\vec{\lambda}\mid\lambda \in\mathbb{R}^{k} \}\subseteq \mathbb{R}^{n}$
## Rowrank
The rowrank of $A$ is the dimension of the rowspace
