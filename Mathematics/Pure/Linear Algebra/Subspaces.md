A non-[[Empty Set|empty]] [[Subsets|subset]] of $U$ of a [[Vectorspaces|vectorspace]] is called a vectorsubspace or linear subspace or subspace if it satisfies the following conditions:
- If $\vec{u},\vec{v}\in U$, then $\vec{u}+\vec{v}\in U$ (closure under addition)
- If $\vec{u}\in U,\lambda \in\mathbb{R}$, then $\lambda \vec{u}\in U$ (closure under scalar multiplication)
- $\{ \vec{0} \}\in U$ (existence of 0)
## Examples
Trivial cases:
$\{ \vec{0} \}\subseteq U$ is a subspace of $U$ and is called the trivial subspace and is sometimes written $0=\{ \vec{0} \}$
$U\subseteq U$ is a subspace of $U$ fairly obviously
Non-trivial cases for [[Vectorspace Rn|$\mathbb{R}^{n}$]]:
Suppose $\vec{d}\in\mathbb{R}^{n}$, $\vec{d}\neq  \vec{0}$, then $L=\{ \lambda \vec{d}\mid\lambda \in\mathbb{R} \}$ (a line through the origin in direction $\vec{d}$) is a subspace of $\mathbb{R}^{n}$, $L\subseteq \mathbb{R}^{n}$ and:
- $\lambda_{1}\vec{d}+\lambda_{2}\vec{d}=(\lambda_{1}+\lambda_{2})\vec{d}\in L$
- $\lambda(\mu \vec{d})=(\lambda\mu)\vec{d} \in L$
- $\vec{0}=0\vec{d} \in L$
Suppose $\vec{a},\vec{b}\in\mathbb{R}$, and they are not multiples of each oter, then $\Pi=\{ \lambda \vec{a}+\mu \vec{b}\mid\lambda,\mu \in\mathbb{R} \}\subseteq \mathbb{R}^{n}$ is a subspace of $\mathbb{R}^{n}$
Note if we had $\Pi=\{ \vec{c}+\lambda \vec{a}+\mu \vec{b}\mid\lambda,\mu \in\mathbb{R} \}\subseteq \mathbb{R}^{n}$, this may not necessarily be a subspace as it may not contain $\vec{0}$, and similarly for other lines not going through the origin. These are called affine subspaces
### Proposition
Suppose [[Matrices|$A\in M_{m\times n}(\mathbb{R})$]], then the solution set $S\subseteq \mathbb{R}^{n}$ to the homogeneous [[Systems of Linear Equations|system of linear equations]] $A\vec{x}=\vec{0}$ is a linear subspace of $\mathbb{R}^{n}$
#### Proof
$$
S=\{ \vec{x}\in \mathbb{R}^{n}\mid A\vec{x}=\vec{0} \}
$$
Then if $\vec{u},\vec{v}\in S$, we have 
$$
A(\vec{u}+\vec{v})=A\vec{u}+A\vec{v}=0+0=0
$$
So $\vec{u}+\vec{v}\in S$
If $\vec{u}\in S,\lambda \in\mathbb{R}$, 
$$
A(\lambda \vec{u})=\lambda A\vec{u}=\lambda0=0
$$
So $\lambda \vec{u}\in S$
And finally $\vec{0}\in S$ as $A\vec{0}=\vec{0}$