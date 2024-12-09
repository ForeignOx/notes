If $T:V\to W$ is a [[Bijective Functions|bijective]] [[Linear Maps|linear map]] (onto and 1-1), then we call $T$ an isomorphism and we call $V$ and $W$ isomorphic. We write $V\cong W$
## Lemma
If $T:V\to W$ is an isomorphism, then so is $T^{-1}:W\to V$ 
For the linear map $T:\mathbb{R}^{n}\to \mathbb{R}^m$ given by [[Matrices|$A\in M_{m\times n}(\mathbb{R})$]], we have $T$ is an isomorphism iff $A$ is invertible and then $T^{-1}(\vec{y})=A^{-1}\vec{y}$
### Proof
We essentially need to check that $T^{-1}$ is also a linear map
Let $\vec{w}_{1},\vec{w}_{2}\in W,\lambda \in\mathbb{R}$, then there exist unique $\vec{v}_{1},\vec{v}_{2}\in V$ such that $T(\vec{v}_{1})=\vec{w}_{1},T(\vec{v}_{2})=\vec{w}_{2}$, since $T$ is a bijection
Then
$$
\vec{w}_{1}+\vec{w}_{2}=T(\vec{v}_{1})+T(\vec{v}_{2})=T(\vec{v}_{1}+\vec{v}_{2})
$$
To which we apply $T^{-1}$:
$$
T^{-1}(\vec{w}_{1}+\vec{w}_{2})=\vec{v}_{1}+\vec{v}_{2}=T^{-1}(\vec{w}_{1})+T^{-1}(\vec{w}_{2})
$$
$$
\lambda \vec{w}_{1}=\lambda T(\vec{v}_{1})=T(\lambda \vec{v}_{1})
$$
Applying $T^{-1}$:
$$
T^{-1}(\lambda \vec{w}_{1})=\lambda \vec{v}_{1}=\lambda T^{-1}(\vec{w}_{1})
$$
Prove the second part here :)
## Fundamental Example
If $B$ is a [[Basis|basis]] for [[Real Vectorspaces|$V$]], then we have a [[Coordinates|coordinate]] map
$$
\Phi_{B}:V\to \mathbb{R}^{n}
$$
Where $\dim(V)=n$, $\Phi_{B}$ is an isomorphism