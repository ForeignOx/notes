If [[Linear Maps|$T:V\to W$]], we define the image of $T$ by:
$$
\text{im}(T):=\{ T(\vec{v})\mid\vec{v}\in  V \}\subseteq W
$$
$\text{im}(T)$ is a subspace
## Proof
Suppose $\vec{u},\vec{w}\in \text{im}(T),\lambda \in\mathbb{R}$, then $\exists \vec{x},\vec{y}\in V$ such that
$$
T(\vec{x})=\vec{u},T(\vec{y})=\vec{w}
$$
So
$$
\vec{u}+\vec{w}=T(\vec{x})+T(\vec{y})=T(\vec{x}+\vec{y})\in  \text{im}(T)
$$
## [[Columnspace and Rowspace|Rank]]
The rank of $T$ is the [[Dimension|dimension]] of the image of $T$
$$
\text{rk}(T):=\dim(\text{im}(T))
$$
## Example
If [[Matrices|$A\in M_{m\times n}(\mathbb{R})$]], $A:\mathbb{R}^{n}\to \mathbb{R}^{n}$, 
$$
\text{im}(A)=\{ A\vec{v}\mid \vec{v}\in \mathbb{R}^{n} \}=\text{colspace(A)}\subseteq \mathbb{R}^{n}
$$
### Subexample
$$
A=\begin{pmatrix}
3&1\\12&4
\end{pmatrix}:\mathbb{R}^{2}\to \mathbb{R}^{2}
$$
So
$$
\text{im}(A)=\left< \begin{pmatrix}
3\\12
\end{pmatrix},\begin{pmatrix}
1\\4
\end{pmatrix} \right> =\left< \begin{pmatrix}
1\\4
\end{pmatrix} \right> \subseteq \mathbb{R}^{2}
$$
Hence $\text{rk}(A)=1$
___
$$
\frac{d }{dx} :\mathbb{R}[x]_{n}\to \mathbb{R}[x]_{n}
$$
Consider what the map is doing:
$$
\frac{d }{dx} (a_{0}+a_{1}x+\dots+a_{n}x^{n})=a_{1}+2a_{2}x+\dots+na_{n}x^{n-1}
$$
So
$$
\text{im}\left( \frac{d }{dx}  \right)=\mathbb{R}[x]_{n-1}\subseteq \mathbb{R}[x]_{n}
$$
$$
 \text{rk}\left( \frac{d }{dx}  \right)=n=\dim(\mathbb{R}[x]_{n-1})
$$
## Lemma
Let $T:V\to W$ be linear and $\{ \vec{v}_{1},\dots,\vec{v}_{n} \}$ be a [[Span|spanning set]] for $V$ (eg. a [[Basis|basis]]), then $\{ T(\vec{v}_{1},\dots,T(\vec{v}_{n})) \}$ is a spanning set for $\text{im}(T)$
### Proof
Suppose $\vec{w}\in\text{im}(T)$, then $\exists \vec{v}\in V:T(\vec{v})=\vec{w}$, we have $\vec{v}=\lambda_{1}\vec{v}_{1}+\dots+\lambda_{n}\vec{v}_{n}$ for some $\lambda_{i}$'s. So 
$$
\vec{w}=T(\vec{v})=T(\lambda_{1}\vec{v}_{1}+\dots+\lambda_{n}\vec{v}_{n})=\lambda_{1}T(\vec{v}_{1})+\dots+\lambda_{n}T(\vec{v}_{n})
$$
Hence proved

#Mathematics #LinAlg #Definition 