The vector product also known as the cross product is particular to $\mathbb{R}^3$ is an operation:
$$
\mathbb{R}^3\times \mathbb{R}^3\to \mathbb{R}^3
$$
$$
(\vec{u},\vec{v})\mapsto \vec{u}\times \vec{v}
$$
## Definition
$$
\vec{x}\times \vec{y}=\begin{pmatrix}
x_{1}\\x_{2}\\x_{3}
\end{pmatrix}\times \begin{pmatrix}
y_{1}\\y_{2}\\y_{3}
\end{pmatrix}:=\begin{pmatrix}
x_{2}y_{3}-x_{3}y_{2}\\x_{3}y_{1}-x_{1}y_{3}\\x_{1}y_{2}-x_{2}y_{1}
\end{pmatrix}
$$
## Properties
- Anti-symmetry
$$
\vec{u}\times \vec{v}=-(\vec{v}\times \vec{u}),\forall \vec{u},\vec{v}\in\mathbb{R}^3
$$
- Linearity 1
$$
(\vec{u}+\vec{v})\times \vec{w}=\vec{u}\times \vec{w}+\vec{v}\times \vec{w}
$$
$$
(\lambda \vec{u})\times \vec{v}=\lambda(\vec{u}\times \vec{v})\,\,\forall\lambda \in \mathbb{R},\vec{u},\vec{v},\vec{w}\in \mathbb{R}^3
$$
- Linearity 2
$$
\vec{u}\times(\vec{v}+\vec{w})=\vec{u}\times \vec{v}+\vec{u}\times \vec{w}
$$
$$
\vec{u}\times(\lambda \vec{v})=\lambda(\vec{u}\times \vec{v})\,\,\forall\lambda \in \mathbb{R},\vec{u},\vec{v},\vec{w}\in \mathbb{R}^3
$$
- Orthogonality to the input, in other words $\vec{u}\times \vec{v}$ is orthogonal to $\vec{u}$ and $\vec{v}$
$$
\vec{u}\cdot(\vec{u}\times \vec{v})=0=\vec{v}\cdot(\vec{u}\times \vec{v}),\,\forall \vec{u},\vec{v}\in \mathbb{R}^3
$$
## Lemma
Suppose that $\vec{x},\vec{y}\in\mathbb{R}^3$ are [[Vectors|vectors]] of [[Magnitude of a Vector|length]] $|\vec{x}|=r>0,|y|=s>0$, then
$$
|\vec{x}\times \vec{y}|=rs\sin\theta
$$
Where $0\leq\theta \leq \pi$ is the [[Angle Between Vectors|angle]] between $\vec{x}$ and $\vec{y}$
### Proof
$$
|\vec{x}\times \vec{y}|^{2}=(\vec{x}\times \vec{y})\cdot(\vec{x}\cdot \vec{y})
$$
$$
= (x_{2}y_{3}-x_{3}y_{2})^{2}+(x_{3}y_{1}-xy_{3})^{2}+(x_{1}y_{2}-x_{2}y_{1})^{2}
$$
$$
= (x_{1}^{2}+x_{2}^{2}+x_{3}^{2})(y_{1}^{2}+y_{2}^{2}+y_{3}^{2})-(x_{1}y_{1}+x_{2}y_{2}+x_{3}y_{3})^{2}
$$
This equals sign is important as the first term shows every combination of $x_{i}^{2}$ with $y_{i}^{2}$ and then subtracts all the terms where $x_{1}$ matches with $y_{1}$ ect. This can be shown rigorously by expanding it out properly
$$
= r^{2}s^{2}-(\vec{x}\cdot \vec{y})^{2}=r^{2}s^{2}-r^{2}s^{2}\cos ^{2}\theta=r^{2}s^{2}(1-\cos ^{2}\theta)
$$
$$
= r^{2}s^{2}\sin ^{2}\theta
$$
$$
\therefore |\vec{x}\times \vec{y}|=rs\sin\theta
$$
As we must take the positive square root