There are three main ways of representing planes in [[Vectorspace Rn|$\mathbb{R}^3$]]
## Parametric Form
![[Planes in R3 2024-10-14 11.41.53.excalidraw]]
Pick a point $\underline{a}\in\Pi$ on the plane and two [[Vectors|vectors]] $\underline{d_{1}},\underline{d_{2}}\in\mathbb{R}^3$ parallel to $\Pi$ but not parallel to each other and such that $\underline{d_{1}}\neq \underline{0}$,$\underline{d_{2}}\neq \underline{0}$
To get to a general point on the plane $\underline{p}\in\Pi$, you first travel from the origin to the point $\underline{a}$ on the plane and then some multiples of $\underline{d_{1}}$ and some multiples of $\underline{d_{2}}$, so:
$$
\Pi=\{ \underline{a}+\lambda_{1}d_{1}+\lambda_{2}d_{2}|\lambda_{1},\lambda_{2}\in \mathbb{R} \}
$$
Here $\lambda_{1},\lambda_{2}$ are called "free variables” and the fact that there are two of them links to the fact that planes are two-dimensional
## Using the Normal Vector
![[Planes in R3 2024-10-14 11.52.40.excalidraw]]
Consider a point $\underline{a}\in\Pi$, $\underline{n}$ is a normal to $\Pi$ ($n\neq 0$) and a general point $\underline{x}\in\Pi$ must satisfy:
$$
\underline{x}\in \Pi \iff(\underline{x}-\underline{a})\text{ orthogonal to } \underline{n}\iff(\underline{x}-\underline{a})\cdot \underline{n}=0
$$
$$
\iff \underline{x}\cdot \underline{n}-\underline{a}\cdot \underline{n}=0\iff \underline{x}\cdot \underline{n}=\underline{a}\cdot \underline{n}=l
$$
So we can describe a plane as:
$$
\Pi=\{ \underline{x}\in \mathbb{R}^3|\underline{x}\cdot \underline{n}=\underline{a}.\underline{n} \}=\{ \underline{x}\in \mathbb{R}^3|\underline{x}\cdot \underline{n}=l \}
$$
You can find the normal vector by taking the [[Cross Product|cross product]] of $\underline{d_{1}}$ and $\underline{d_{2}}$ from the method above
## Cartesian Form
This is essentially the same as the method using the normal vector above, but using coordinates
If we write:
$$
\underline{n}=\begin{pmatrix}
a\\b\\c
\end{pmatrix},\underline{x}=\begin{pmatrix}
x\\y\\z
\end{pmatrix}
$$
So $\underline{n}\cdot \underline{x}=l$ can be written:
$$
ax+by+cz=l
$$
So:
$$
\Pi=\left\{  \begin{pmatrix}
x\\y\\ z
\end{pmatrix}\in \mathbb{R}^3|ax+by+cz=l  \right\}
$$
## Parametric Description from Normal/Cartesian
Suppose:
$$
\Pi=\left\{ \underline{x}\in \mathbb{R}^3 \middle| \underline{n}\cdot \underline{x}=l \right\}=\left\{  \begin{pmatrix}
x\\y\\ z
\end{pmatrix}\in \mathbb{R}^3\middle|ax+by+cz=l \right\}
$$
$$
\underline{n}=\begin{pmatrix}
a\\b\\c
\end{pmatrix}
$$
If $c\neq 0$ then:
$$
ax+by+cz=l\iff z=\frac{l}{c}-\left( \frac{a}{c} \right)x-\left( \frac{b}{c} \right)y
$$
Since we can use $z$ to be any point, $x$ and $y$ become our free parameters essentially; so:
$$
\Pi=\left\{  \begin{pmatrix}
0\\0\\ \frac{l}{c}
\end{pmatrix} +x\begin{pmatrix}
1\\0\\-\frac{a}{c}
\end{pmatrix}+y\begin{pmatrix}
0\\1\\ -\frac{b}{c}
\end{pmatrix}\middle|x,y\in \mathbb{R} \right\}
$$
If $c=0$, then you can do the same process using $b$ or $c$
## Examples
### Find Plane using Point and Normal
Find the cartesian description of the plane $\Pi$ that passes through:
$$
\begin{pmatrix}
1\\-1\\3
\end{pmatrix}=\underline{a}\in \Pi
$$
and is normal to the direction:
$$
\begin{pmatrix}
5\\2\\1
\end{pmatrix}=\underline{n}
$$
So:
$$
\Pi=\left\{  \underline{x}=\begin{pmatrix}
x\\y\\ z
\end{pmatrix}\in \mathbb{R}^3|\begin{pmatrix}
x\\y\\z
\end{pmatrix}\cdot \begin{pmatrix}
5\\2\\1
\end{pmatrix}= \begin{pmatrix}
1\\-1\\3
\end{pmatrix}\cdot \begin{pmatrix}
5\\2\\1
\end{pmatrix} \right\}
$$
$$
\implies \Pi=\left\{  \begin{pmatrix}
x\\y\\ z
\end{pmatrix}\in \mathbb{R}^3|5x+2y+z=6  \right\}
$$
### Find Normal Vector and Point on the Plane
Find a normal vector and a point on the plane $6x-5y+3z=30$, using what we know about the cartesian equation for a plane we can clearly see:
$$
\underline{n}=\begin{pmatrix}
6\\-5\\3
\end{pmatrix}
$$
and $\underline{a}$ can be any point on the plane, an easy way of finding one is to let $z,y=0$ and solve $6x=30\implies x=5$, so:
$$
\underline{a}=\begin{pmatrix}
5\\0\\0
\end{pmatrix}
$$
Using the same method we could obtain
$$
\underline{a}=\begin{pmatrix}
0\\-6\\0
\end{pmatrix}\text{ or }\underline{a}=\begin{pmatrix}
0\\0\\10
\end{pmatrix}
$$
### FInding Parametric and Cartesian Descriptions of the Plane $\Pi$ based on Points
Where $\Pi \subseteq\mathbb{R}^3$ that passes through:
$$
\underline{a}=\begin{pmatrix}
1\\0\\1
\end{pmatrix},\underline{b}=\begin{pmatrix}
2\\-1\\3
\end{pmatrix},\underline{c}=\begin{pmatrix}
5\\1\\1
\end{pmatrix}
$$
![[Planes in R3 2024-10-15 11.45.09.excalidraw]]

This method works assuming $\underline{a},\underline{b}$ and $\underline{c}$ are not colinnear
Set:
$$
\underline{d_{1}}=\underline{b}-\underline{a}=\begin{pmatrix}
1\\-1\\2
\end{pmatrix}
$$
$$
\underline{d_{2}}=\underline{c}=\underline{a}=\begin{pmatrix}
4\\1\\0
\end{pmatrix}
$$
So 
$$
\Pi=\{ \underline{a}+\lambda_{1}  \underline{d_{1}}+ \lambda_{2} \underline{d_{2}}|\lambda_{1},\lambda_{2}\in \mathbb{R}\}
$$
Now to find a cartesian description, we can use the fact that $\underline{n}$ will be orthogonal to $\underline{d_{1}}$ and $\underline{d_{2}}$ so:
$$
\underline{n}:=\underline{d_{1}}\times \underline{d_{2}}
$$
$$
\therefore \underline{n}=\begin{pmatrix}
1\\-1\\2
\end{pmatrix}\times \begin{pmatrix}
4\\1\\0
\end{pmatrix}=\begin{pmatrix}
-2\\8\\5
\end{pmatrix}
$$
Then we know $l=\underline{n}\cdot \underline{a}$, so $l=-2+5=3$, so we have:
$$
\Pi=\left\{  \begin{pmatrix}
x\\y\\ z
\end{pmatrix}\in \mathbb{R}^3\middle|-2x+8y+5z=3  \right\}
$$

#Mathematics #LinAlg 