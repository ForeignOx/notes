If $U$ is a finite [[Dimension|dimensional]] [[Subspaces|subspace]] of $V$, then we can always decompose any [[Vectors|$\underline{v}\in V$]] into [[Orthogonality|orthogonal]] components from the [[Orthogonal Complement|orthogonal complement]] of $U$, $U^{\bot}$:
$$
\underline{v}=\underline{u}+\tilde{\underline{u}}
$$
With $\underline{u}\in U,\tilde{\underline{u}}\in U^{\bot}$
We call $\underline{u}$ the orthogonal projection of $\underline{v}$ onto the subspace $U$, and we write this as $P_{U}(\underline{v})$
## Proof
Apply [[Gran-Schmidt Procedure|Gran-Schmidt]], to $U$, so
$$
U=\text{span}\left\{ \underline{u}_{1},\dots,\underline{u}_{k} \right\}
$$
With some [[Inner Product|inner product]], such that
$$
(\underline{u}_{i},\underline{u}_{j})=\delta_{ij}
$$
(Using the [[Kronecker Delta Function|Kronecker delta function]])
Then set:
$$
\underline{u}=(\underline{v},\underline{u}_1)\underline{u}_{1}+(\underline{v},\underline{u}_{2})\underline{u}_{2}+\dots+(v,\underline{u}_{k})\underline{u}_{k}
$$
And
$$
\underline{\tilde{u}}=\underline{v}-\underline{u}
$$
Then clearly
$$
\underline{v}=\underline{u}+ \tilde{\underline{u}}
$$
WIth $\underline{u}\in U$, and,
$$
(\underline{\tilde{u}},\underline{u}_{i})=(\underline{v}-\underline{u},\underline{u}_{i})=(\underline{v},\underline{u}_{i})-(\underline{u},\underline{u}_{i})=(\underline{v},\underline{u}_{i})-(\underline{v},\underline{u}_{i})=0
$$
So $\tilde{\underline{u}}\bot \underline{u}_{i}\forall i=1\dots k$ so $\underline{\tilde{u}}$ is orthogonal to all elements of $U$, so $\underline{\tilde{u}}\in U^{\bot}$
## Properties
$P_{U}$ is a [[Linear Maps|linear]] operator $P:V\to V$
The [[image|image]] of $P$ is $\text{Im}(P)=U$, while its [[Kernel|kernel]] is $\text{ker}(P)=U^{\bot}$
$P_{U}^{2}=P_{U}$, since if you have a vector in the subspace, if you apply the transformation again, nothing happens , i.e. $\forall \underline{v}\in V$,
$$
P_{U}^{2}(\underline{v})=P_{U}(\underline{v})
$$
So $P$ is idempotent
$P$ restricted to $U$ is the identity operator, which we usually write as $P|_{U}=I$ to $P_{U}(\underline{u})=\underline{u}\forall \underline{u}\in U$
$$
P_{U}(I-P_{U})=0
$$
[[Eigenvalues|Eigenvalues]] of $P_{U}$ are just $0$ and $1$
The idea is that $P_{U}(\underline{v})$ is the closest bector to $\underline{v}$ belonging to $U$
## Proposition
Let $U$ be a finite dimensional subspace of $\left\{ V,(,) \right\}$ let $\underline{v}_{0}\in V$ and $\underline{u}_{0}=P_{U}(\underline{v}_{0})$, i.e. $\underline{u}_{0}$ is the orthogonal projection of $\underline{v}_{0}$ onto $U$
Then
$$
\forall \underline{u}\in U,\lvert \lvert \underline{u}-\underline{v}_{0} \rvert \rvert \geq \lvert \lvert \underline{u}_{0}-\underline{v}_{0} \rvert \rvert 
$$
With equality iff $\underline{u}=\underline{u}_{0}$
$\underline{u}_{0}$ is sometimes called the least-squares approximation to $\underline{v}_{0}$
## Example
Let $V=\mathbb{R}^{4}$ with [[Dot Product|dot product]], then let 
$$
U=\text{span}\left\{ \underline{u}_{1}=\begin{pmatrix}
1\\1\\0\\1
\end{pmatrix},\underline{u}_{2}=\begin{pmatrix}
0\\1\\1\\0
\end{pmatrix} \right\}
$$
 
