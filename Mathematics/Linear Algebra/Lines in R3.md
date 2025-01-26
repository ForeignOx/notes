Lines can be described in a few ways in [[Vectorspace Rn|$\mathbb{R}^3$]]
## Parametric Description
![[Lines in R3 2024-10-15 11.52.34.excalidraw]]
We take a point $\vec{a}\in L$, and a vector $\vec{d}\neq 0$ parallel to $L$, then
$$
L=\{ \vec{a}+\lambda \vec{d}|\lambda \in \mathbb{R} \}
$$
## Cartesian Description
We can abstract this from the cartesian description, set:
$$
\vec{a}=\begin{pmatrix}
a_{1}\\a_{2}\\a_{3}
\end{pmatrix},\vec{d}=\begin{pmatrix}
d_{1}\\d_{2}\\d_{3}
\end{pmatrix}
$$
Then
$$
\begin{pmatrix}
x\\y\\z
\end{pmatrix}\in L\iff \begin{matrix}
a_{1}+\lambda d_{1}=x\\a_{2}+\lambda d_{2}=y\\a_{3}+\lambda d_{3}=z
\end{matrix}
$$
### Suppose $d_{1}\neq 0,d_{2}\neq 0,d_{3}\neq 0$, then
$$
\lambda=\frac{x-a_{1}}{d_{1}}=\frac{y-a_{2}}{d_{2}}=\frac{z-a_{3}}{d_{3}}
$$
So
$$
\begin{pmatrix}
x\\y\\z
\end{pmatrix}\in L\iff \frac{x-a_{1}}{d_{1}}=\frac{y-a_{2}}{d_{2}}=\frac{z-a_{3}}{d_{3}}
$$
$$
L=\left\{  \begin{pmatrix}
x\\y\\ z
\end{pmatrix}\in \mathbb{R}^3| \frac{x-a_{1}}{d_{1}}=\frac{y-a_{2}}{d_{2}}=\frac{z-a_{3}}{d_{3}} \right\}
$$
### If $d_{1},d_{2}\neq 0$, but $d_{3}=0$, then:
$$
\lambda=\frac{x-a_{1}}{d_{1}}=\frac{y-a_{2}}{d_{2}},z=a_{3}
$$
So
$$
L=\left\{  \begin{pmatrix}
x\\y\\ z
\end{pmatrix}\in \mathbb{R}^3| \frac{x-a_{1}}{d_{1}}=\frac{y-a_{2}}{d_{2}},z=a_{3} \right\}
$$
Similar expressions can be formed is one of $d_{1}$ or $d_{2}$ are instead zero
### If $d_{1}\neq 0$, but $d_{2}=d_{3}=0$, then
$$
L=\left\{  \begin{pmatrix}
x\\y\\ z
\end{pmatrix}\in \mathbb{R}^3 | y=a_{2},z=a_{3}\right\}
$$
Which will be a line parallel to the $x$-axis
This makes sense as in a cartesian description, you have $\hspace{0pt}3$ free variables that then you give two conditions for, reducing what we imagine the dimension to be from $\hspace{0pt}3$ to $\hspace{0pt}1$ 
You can also think of the cartesian form as a description that is the intersection of two planes from the two equations
## Intersection of Two [[Planes in R3|Planes]]
Suppose we have two planes for $i=1,2$:
$$
\Pi_{i}=\{ \vec{x}\in \mathbb{R}^3|\vec{n}_{i}\cdot \vec{x} =l_{i}\}\subseteq \mathbb{R}^3
$$
Then what is $\Pi_{1}\cap \Pi_{2}$?
### If $n_{1},n_{2}$ are parallel (collinear)
Then either $\Pi_{1}=\Pi_{2}$, or they are parallel planes, so $\Pi_{1}\cap \Pi_{2}=\emptyset$
### If $n_{1},n_{2}$ are not parallel
Then their intersection is a line $L$
So
$$
L=\{ \vec{x}\in \mathbb{R}^3|\vec{n}_{1}\cdot \vec{x}=l_{1},\vec{n}_{2}\cdot \vec{x}=l_{2} \}
$$
Letting
$$
\vec{n}_{1}=\begin{pmatrix}
a\\b\\c
\end{pmatrix},\vec{n}_{2}=\begin{pmatrix}
d\\e\\f
\end{pmatrix}
$$
$$
L= \left\{  \begin{pmatrix}
x\\y\\ z
\end{pmatrix}\in \mathbb{R}^3\mid \begin{matrix}
ax+by+cz=l_{1}\\dx+ey+fz=l_{2}
\end{matrix}  \right\}
$$
### Converting between this description and parametric description
We need $\vec{a}\in L,\vec{d}\neq 0$ where $\vec{d}$ is parallel to $L$
![[Lines in R3 2024-10-17 10.40.14.excalidraw]]
$\vec{d}$ is parallel to $\Pi_{1}$ and $\Pi_{2}$ so
$$
\vec{d}\cdot \vec{n}_{1}=0,\vec{d}\cdot \vec{n}_{2}=0
$$
So set
$$
\vec{d}=\vec{n}_{1}\times \vec{n}_{2}=\begin{pmatrix}
a\\b\\c
\end{pmatrix}\times \begin{pmatrix}
d\\e\\f
\end{pmatrix}=\begin{pmatrix}
bf-ce\\cd-af\\ae-bd
\end{pmatrix}
$$
To find $\vec{a}\in L$, if $ae-bd\neq 0$, i.e. the third coordinate is non-zero, then $\vec{d}$ has some $z$-component, so must intersect the $x$-$y$ plane at a unique point when $z=0$, which we can take to be $\vec{a}$:
$$
\vec{a}=\begin{pmatrix}
g\\h\\0
\end{pmatrix}
$$
Where $g,h$ satisfy
$$
ag+bh=l_{1},dg+eh=l_{2}
$$
Which can be solved for $g,h$, if the third component is $\hspace{0pt}0$, the same technique can be used for one of the other components
#### Example
Find a parametric description of the intersection $L=\Pi_{1}\cap \Pi_{2}$ of the planes:
$$
\Pi_{1}:x+y+z=2
$$
$$
\Pi_{2}:2x-y+z=0
$$
We can find $\vec{d}$ by reading off the normal vectors
$$
\vec{d}=\vec{n}_{1}\times \vec{n}_{2}=\begin{pmatrix}
1\\1\\1
\end{pmatrix}\times \begin{pmatrix}
2\\-1\\1
\end{pmatrix}=\begin{pmatrix}
2\\1\\-3
\end{pmatrix}
$$
and then find 
$$
\vec{a}=\begin{pmatrix}
g\\h\\0
\end{pmatrix}\in L
$$
So
$$
g+h=2
$$
$$
 2g-h=0
$$
$$
 \iff h=\frac{4}{3},g=\frac{2}{3}
$$
So
$$
L=\left\{  \begin{pmatrix}
\frac{2}{3}\\ \frac{4}{3}\\0
\end{pmatrix}+\lambda \begin{pmatrix}
2\\1\\-3
\end{pmatrix}|\lambda \in \mathbb{R}  \right\}
$$


#Mathematics #LinAlg 