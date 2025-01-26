If [[Matrices|$A\in M_{n\times k}(\mathbb{R})$]], then
## Columnspaces
The columnspace of $A$ is the [[Span|span]] inside $\mathbb{R}^{n}$ of the columns of the matrix $A$, i.e. if
$$
A=\begin{pmatrix}
\vec{u}_{1}&\dots&\vec{u}_{k}
\end{pmatrix}
$$
Then $\text{columnspace}(A)=\text{span}< \vec{u}_{1},\dots \vec{u}_{k} >\subseteq \mathbb{R}^{n}$
Another way of thinking about this is that $\text{columnspace(A)}=\{ A\vec{\lambda}\mid\lambda \in\mathbb{R}^{k} \}\subseteq \mathbb{R}^{n}$
## Columnrank
The columnrank of $A$ is the [[Dimension|dimension]] of the columnspace
## Rowspaces
The rowspace of $A$ is the span inside $\mathbb{R}^{n}$ of the rows of the matrix $A$, so it is a subspace of $\mathbb{R}^k$, more honestly, it's the columnspace of $A^{t}$
$$
A=\begin{pmatrix}
\vec{u}_{1}\\\vdots\\\vec{u}_{k}
\end{pmatrix}
$$
Then $\text{rowspace}(A)=\text{span}< \vec{u}_{1},\dots \vec{u}_{k} >\subseteq \mathbb{R}^{k}$
## Rowrank
The rowrank of $A$ is the dimension of the rowspace
## Lemma
Suppose $\{ \vec{v}_{1},\dots,\vec{v}_{r} \}\in\mathbb{R}^{n}$ is a [[Linear Independence|linearly independnet]] [[Subsets|subset]], and let $P\in M_{n}(\mathbb{R})$ be an [[Matrix Inverses|invertible]] matrix
Then $\{ P\vec{v}_{1},\dots,P\vec{v}_{r} \}\subseteq \mathbb{R}^{n}$ is also linearly independent
### Proof
Suppose $\lambda_{1}P\vec{v}_{1}+\dots+\lambda_{r}P\vec{v}_{r}= \vec{0}$, we want to show all $\lambda=0$, so we start by left multiplying by $P ^{-1}$
$$
P(\lambda_{1}\vec{v}_{1}+\dots+\lambda_{r}\vec{v}_{r})=\vec{0}
$$
$$
\implies P ^{-1}P(\lambda_{1}\vec{v}_{1}+\dots+\lambda_{r}\vec{v}_{r})=P ^{-1}(\vec{0})
$$
$$
\implies \lambda_{1}\vec{v}_{1}+\dots+\lambda_{r}\vec{v}_{r}= \vec{0}
$$
So since $\{ \vec{v}_{1},\dots,\vec{v}_{r} \}$ is linearly independent, each $\lambda_{i}=0$
## Proposition
Let $A\in M_{m\times n}(\mathbb{R})$ and let $P \in M_{n}(\mathbb{R})$ be invertible, then $A$ and $PA$ have the same colrank, rowrank and nullity
- $A$ and $PA$ have the same rowspace
- $A$ and $PA$ have the same colrank
- $A$ and $PA$ have the same nullspace
### Proof
Since invertible matrices are the product of elementary matrices, it suffices to prove this for $P=E$, an elementary matrix
Each row of $EA$ is a [[Linear Combinations|linear combination]] of the rows of $A$, since $EA$ differs from $A$ by an $ERO$, so we certainly have $\text{rowspace}(EA)\subseteq \text{rowspace}(A)$, but also $A=E ^{-1}(EA)$, where $E^{-1}$ is elementary, so $\text{rowspace}(A)\subseteq \text{rowspace}(EA)$ as well

Write $U=\text{colspace}(A)=\{ A \vec{x}\mid \vec{x} \in\mathbb{R}^{k} \}\subseteq \mathbb{R}^{n}$, so $\text{colspace}(PA)=\{ PA\vec{x}\mid \vec{x} \in \mathbb{R}^{k} \}\subseteq \mathbb{R}^{n}$, so if we have for some $\vec{x}$
$$
\vec{u}\in U\iff \vec{u}=A\vec{x}
$$
$$
\iff P\vec{u}=PA\vec{x}
$$
Since $P$ is invertible
$$
\iff P\vec{u}\in \text{colspace}(PA)
$$
Hence $\text{colspace}(PA)=PU:=\{ P\vec{u}\mid \vec{u}\in U \}$, and we want to show whether $\text{dim}(U)=\dim(PU)$
Let $\{ \vec{v}_{1},\dots,\vec{v}_{r} \}\in\mathbb{R}^{n}$ be a [[Basis|basis]] for $U$, (so $\dim(U)=r$), we are claiming that $\{ P\vec{v}_{1},\dots,P\vec{v}_{r} \}\subseteq \mathbb{R}^{n}$ is a basis for $PU$ (so $\dim(PU)=r$)
$\{ P\vec{v}_{1},\dots,P\vec{v}_{r} \}$ is independent by the Lemma above. If $\vec{v}\in PU$, then $\vec{v}=P\vec{u}$ for some $\vec{u}=\lambda_{1}\vec{v}_{1}+\dots+\lambda_{r}\vec{v}_{r}\in U$, so
$$
\vec{v}=P(\lambda_{1}\vec{v}_{1}+\dots+\lambda _{r}\vec{v}_{r})=\lambda_{1}P\vec{v}_{1}+\dots+\lambda_{r}P\vec{v}_{r}
$$
So it is spanning, so overall a basis :)

Suppose that $\vec{u}\in\mathbb{R}^{k}$, then $A\vec{u}= \vec{0}\iff PA \vec{u}=\vec{0}$, so $\text{nullspace}(A)=\text{nullspace}(PA)$
## $\text{rowrank}(A)=\text{colrank}(A)$
### Corollary/Definition
We define the rank of a matrix $A\in M_{n\times k}(\mathbb{R})$, by $\text{rk}(A):=\text{rowrank}(A)=\text{colrank}(A)$
By the proposition, we can consider the [[Row Reduced Echelon Form|RREF]] of $A$, $A'\in M_{n\times k`}(\mathbb{R})$
If there are $m$ rows witha leading $\hspace{0pt}1$, and $n-m$ zero rows, so:
$$
\text{colspace}(A')=\text{span}< \vec{e}_{1},\dots,\vec{e}_{m} > \in \mathbb{R}^{n}
$$
$$
\implies \text{colrank}(A')=m
$$
$$
\text{rowspace}(A')=\text{span}< \vec{r}_{1},\dots \vec{r}_{m} > \subseteq \mathbb{R}^{k}
$$
Where $\vec{r}_{i}$ is the $i$th row of $A'$, where we have discarded columns rows of zeros, so we only have $m$ of them, but note $\{ \vec{r}_{1},\dots,\vec{r}_{m} \}$ is linearly independent by looking at the coordinates of the leading 1's, so $\text{rowrank}(A')=m$

#Mathematics #LinAlg #Definition #Theorem 