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


#Mathematics #LinAlg #Definition