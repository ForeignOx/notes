We define the scalar or dot product:
$$
\mathbb{R}^n\times \mathbb{R}^n\to \mathbb{R}
$$
$$
(\vec{u},\vec{v})\mapsto \vec{u}\cdot \vec{v}
$$
$$
\vec{u}\cdot \vec{v}=\begin{pmatrix}
u_{1}\\u_{2}\\\vdots\\v_{n}
\end{pmatrix}\cdot \begin{pmatrix}
v_{1}\\v_{2}\\\vdots\\v_{n}
\end{pmatrix}=u_{1}v_{1}+u_{2}v_{2}+\dots+u_{n}v_{n}=\sum_{ i=1} ^{ n}  u_{i}v_{i} \in \mathbb{R}
$$
## Properties of the dot product
- Symmetry: 
$$
\vec{u}\cdot \vec{v}=\vec{v}\cdot \vec{u},\forall \vec{u},\vec{v}\in\mathbb{R}^n
$$
- Linearity 1:
$$
(\vec{u}+\vec{v})\cdot \vec{w}=\vec{u}\cdot \vec{w}+\vec{v}\cdot \vec{w}
$$
$$
(\lambda \vec{u})\cdot \vec{w}=\lambda(\vec{u}\cdot \vec{w}),\,\forall\lambda \in \mathbb{R},\vec{u},\vec{v},\vec{w}\in \mathbb{R}^n
$$
- Linearity 2
$$
\vec{u}\cdot(\vec{v}+\vec{w})=\vec{u}\cdot \vec{v}+\vec{u}\cdot \vec{w}
$$
$$
\vec{u}\cdot(\lambda \vec{w})=\lambda(\vec{u}\cdot \vec{w}),\,\forall\lambda \in \mathbb{R},\vec{u},\vec{v},\vec{w}\in \mathbb{R}^n
$$
- Positivity
$$
\vec{v}\cdot \vec{v}\geq 0\,\forall \vec{v}\in \mathbb{R}^n
$$
$$
\vec{v}\cdot \vec{v}=\vec{0}\iff \vec{v}=\vec{0}
$$
## Consider $\mathbb{R}^2$
Suppose $\vec{v},\vec{w}\in\mathbb{R}^2$, where $|\vec{v}|=r$, $|\vec{w}|=s$, suppose that $\vec{v},\vec{w}$ make an angle of $\alpha$ with each other where $0\leq\alpha \leq \pi$
![[Polar Coordinates 2024-10-10 10.12.27.excalidraw]]
Then using the [[Dot Product|dot product]], we want to show $\vec{v}\cdot \vec{w}=rs\cos\alpha$
### Proof
Suppose polar coordinates of $\vec{v}$ are $(r,\theta)$ and of $\vec{w}$ are $(s,\phi)$, then
$$
\vec{v}=\begin{pmatrix}
r\cos\theta\\r\sin\theta
\end{pmatrix}
$$
$$
\vec{w}=\begin{pmatrix}
s\cos \phi\\s\sin \phi
\end{pmatrix}
$$
$$
\implies \vec{v}\cdot \vec{w}=\begin{pmatrix}
r\cos\theta\\r\sin\theta
\end{pmatrix}\cdot
\begin{pmatrix}
s\cos \phi\\s\sin \phi
\end{pmatrix}=rs\cos\theta \cos \phi+rs\sin\theta \sin \phi=rs(\cos\theta \cos \phi+\sin\theta \sin \phi)
$$
$$
= rs\cos(\theta-\phi)=rs\cos(\pm\alpha)=rs\cos\alpha
$$
as $\cos$ is an [[Even Functions|even function]]
### Corollary
If $\vec{v}\neq 0$ and $\vec{w}\neq 0$, $\vec{v}$ and $\vec{w}$ are orthogonal iff $\vec{v}\cdot \vec{w}=0$
#### Proof
$$
\vec{v}\cdot \vec{w}=0\iff \cos\alpha=0\iff\alpha=\frac{\pi}{2}
$$


#Mathematics #LinAlg #Definition