If [[Linear Maps|$T:V\to W$]], we define the image of $T$ by:
$$
\text{im}(T):=\{ T(\underline{v})\mid\underline{v}\in  V \}\subseteq W
$$
$\text{im}(T)$ is a subspace
## Proof
Suppose $\underline{u},\underline{w}\in \text{im}(T),\lambda \in\mathbb{R}$, then $\exists \underline{x},\underline{y}\in V$ such that
$$
T(\underline{x})=\underline{u},T(\underline{y})=\underline{w}
$$
So
$$
\underline{u}+\underline{w}=T(\underline{x})+T(\underline{y})=T(\underline{x}+\underline{y})\in  \text{im}(T)
$$
## [[Columnspace and Rowspace|Rank]]
The rank of $T$ is the [[Dimension|dimension]] of the image of $T$
$$
\text{rk}(T):=\dim(\text{im}(T))
$$
## Example
If [[Matrices|$A\in M_{m\times n}(\mathbb{R})$]], $A:\mathbb{R}^{n}\to \mathbb{R}^{n}$, 
$$
\text{im}(A)=\{ A\underline{v}\mid \underline{v}\in \mathbb{R}^{n} \}=\text{colspace(A)}\subseteq \mathbb{R}^{n}
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
Let $T:V\to W$ be linear and $\{ \underline{v}_{1},\dots,\underline{v}_{n} \}$ be a [[Span|spanning set]] for $V$ (eg. a [[Basis|basis]]), then $\{ T(\underline{v}_{1},\dots,T(\underline{v}_{n})) \}$ is a spanning set for $\text{im}(T)$
### Proof
Suppose $\underline{w}\in\text{im}(T)$, then $\exists \underline{v}\in V:T(\underline{v})=\underline{w}$, we have $\underline{v}=\lambda_{1}\underline{v}_{1}+\dots+\lambda_{n}\underline{v}_{n}$ for some $\lambda_{i}$'s. So 
$$
\underline{w}=T(\underline{v})=T(\lambda_{1}\underline{v}_{1}+\dots+\lambda_{n}\underline{v}_{n})=\lambda_{1}T(\underline{v}_{1})+\dots+\lambda_{n}T(\underline{v}_{n})
$$
Hence proved

#Mathematics #LinAlg #Definition 