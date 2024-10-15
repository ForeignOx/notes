## Numbers
If $x,y\in \mathbb{R}$ then $\left| x+y \right|\leq \left| x \right|+\left| y \right|$
### Proof
Given $x,y\in\mathbb{R}$, then $xy=0$ or $xy>0$ or $xy<0$
If $xy=0$ then either $x=0$ or $y=0$
    If $x=0$, $\left| x+y \right|=\left| y \right|=\left| x \right|+\left| y \right|$
    Similarly, if $y=0$, by symmetry, $\left| x+y \right|=\left| x \right|+\left| y \right|$
If $xy>0$ either $x>0$, $y>0$ or $x<0$, $y<0$
    If $x>0$, $y>0$ then $x+y>0$, so $\left| x+y \right|=x+y=\left| x \right|+\left| y \right|$
    If $x<0$, $y<0$ then $x+y<0$ so $\left| x+y \right|=-(x+y)=-x+-y=\left| x \right|+\left| y \right|$
If $xy<0$, either $x>0$,$y<0$ or $x<0$, $y>0$
    Without loss of generalisation, $x>0$, $y<0$
        If $\left| x \right|>\left| y \right|$ then $x+y>0$ so $\left| x+y \right|=\left| x \right|-\left| y \right|<\left| x \right|<\left| x \right|+\left| y \right|$
        If $\left| x \right|<\left| y \right|$, then $\left| x+y \right|=\left| y \right|-\left| x \right|<\left| y \right|<\left| x \right|+\left| y \right|$
        If $\left| x \right|=\left| y \right|$, then $\left| x+y \right|=0=\left| x \right|+\left| y \right|$
## [[Vectors|Vectors]] in $\mathbb{R}^n$
The triangle inequality is as follows:
$$
|\vec{u}+\vec{v}|\leq|\vec{u}|+|\vec{v}|
$$
Intuitively it can be thought of by considering the triangle formed with side lengths $|\vec{u}|,|\vec{v}|,|\vec{u}+\vec{v}|$:
![[Triangle Inequality 2024-10-15 22.09.42.excalidraw]]
We can see that clearly one side can't be greater than the sum of the lengths of the other two sides, and that equality holds when $\vec{v}$ and $\vec{u}$ are parallel
### Proof
Let $\vec{u},\vec{v}\in\mathbb{R}^n$, let:
$$
\vec{u}=\begin{pmatrix}
u_{1}\\u_{2}\\\vdots\\u_{n}
\end{pmatrix},\vec{v}=\begin{pmatrix}
v_{1}\\v_{2}\\\vdots\\v_{n}
\end{pmatrix}
$$
We can now express the [[Dot Product|dot product]] in terms of $|\vec{u}|,|\vec{v}|,|\vec{u}+\vec{v}|$ by first noting:
$$
\vec{u}\cdot \vec{v}=u_{1}v_{1}+u_{2}v_{2}+\dots+u_{n}v_{n}
$$
$$
|\vec{u}|^{2}=u_{1}^{2}+u_{2}^{2}+\dots+u_{n}s^{2}
$$
$$
|\vec{v}|^{2}=v_{1}^{2}+v_{2}^{2}+\dots+v_{n}^{2}
$$
So:
$$
|\vec{u}+\vec{v}|^{2}=(u_{1}+v_{1})^{2}+(u_{2}+v_{2})^{2}+\dots+(u_{n}+v_{n})^{2}
$$
$$
= u_{1}^{2}+2u_{1}v_{1}+v_{1}^{2}+u_{2}^{2}+2u_{2}v_{2}+v_{2}^{2}+\dots+u_{n}^{2}+2u_{n}v_{n}+v_{n}^{2}=|\vec{u}|^{2}+|\vec{v}|^{2}+2(\vec{u}\cdot \vec{v})
$$
$$
\implies \vec{u}\cdot \vec{v}=\frac{|\vec{u}+\vec{v}|^{2}-|\vec{u}|^{2}-|\vec{v}|^{2}}{2}
$$
Using the [[Cauchy-Schwarz Inequality|Cauchy-Schwarz inequality]] we have:
$$
\vec{u}\cdot \vec{v}\leq|\vec{u}| | \vec{v}|
$$
Combining these, we get:
$$
|\vec{u}| |\vec{v}|\geq \frac{|\vec{u}+\vec{v}|^{2}-|\vec{u}|^{2}-|\vec{v}|^{2}}{2}
$$
$$
\implies |\vec{u}+\vec{v}|^{2}\leq|\vec{u}|^{2}+2|\vec{u}| |\vec{v}|+|\vec{v}|^{2}
$$
$$
\implies |\vec{u}+\vec{v}|^{2}\leq (|\vec{u}|+|\vec{v}|)^{2}
$$
$$
\implies |\vec{u}+\vec{v}|\leq|\vec{u}|+|\vec{v}|
$$
Since $|\vec{u}+\vec{v}|^{2}$ is the square of a magnitude (and so is positive) and $|\vec{u}|+|\vec{v}|$ is the sum of two magnitudes (and so is also positive)

#Mathematics #LinAlg #Theorem