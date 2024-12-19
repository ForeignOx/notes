The following are equivalent as proven here(!)
- $B$ is a [[basis|basis]] for $V$
- $B$ is a maximal [[Linear Independence|linearly independent]] [[Subsets|subset]]
- $B$ is a minimal [[span|spanning]] set
- $B=\{ \vec{v}_{1},\dots,\vec{v}_{n} \}$ is a basis iff we can write each $\vec{v}\in V$ uniquely as $\vec{v}=\lambda_{1}\vec{v}_{1}+\dots+\lambda_{n}\vec{v}_{n}$
We call $\lambda_{1},\dots,\lambda_{n}$ the coordinates of $\vec{v}$ with respect to $B$
## Coordinate Map
We define the coordinate map with respect to $B$ (an ordered basis) as:
$$
\Phi_{B}:V\to \mathbb{R}^{n}
$$
$$
 \Phi_{B}:\vec{v}\mapsto \begin{pmatrix}
\lambda_{1}\\\vdots\\\lambda_{n}
\end{pmatrix}
$$
## Examples
The standard basis for $M_{2}(\mathbb{R})$ is
$$
B=\left\{  \begin{pmatrix}
1&0\\0&0
\end{pmatrix},\begin{pmatrix}
0&1\\0&0
\end{pmatrix},\begin{pmatrix}
0&0\\1&0
\end{pmatrix},\begin{pmatrix}
0&0\\0&1
\end{pmatrix}  \right\}
$$
So:
$$
\Phi_{B}:M_{2}(\mathbb{R})\to \mathbb{R}^4
$$
$$
 \Phi_{B}:\begin{pmatrix}
a&b\\c&d
\end{pmatrix}\mapsto \begin{pmatrix}
a\\b\\c\\d
\end{pmatrix}
$$
If we take the basis
$$
E=\left\{  \begin{pmatrix}
1&0\\0&0
\end{pmatrix},\begin{pmatrix}
0&0\\1&0
\end{pmatrix},\begin{pmatrix}
0&-2\\0&0
\end{pmatrix},\begin{pmatrix}
0&0\\0&1
\end{pmatrix}  \right\}
$$
Then
$$
\begin{pmatrix}
a&b\\c&d
\end{pmatrix}=a\begin{pmatrix}
1&0\\0&0
\end{pmatrix}+c\begin{pmatrix}
0&0\\1&0
\end{pmatrix}-\frac{1}{2}b\begin{pmatrix}
0&-2\\0&0
\end{pmatrix}+d\begin{pmatrix}
0&0\\0&1
\end{pmatrix}
$$
So
$$
\Phi_{E}\begin{pmatrix}
a&b\\c&d
\end{pmatrix}=\begin{pmatrix}
a\\c\\-\frac{1}{2}b\\d
\end{pmatrix}
$$
We could take 
$$
F=\left\{  \begin{pmatrix}
1&0\\0&0
\end{pmatrix},\begin{pmatrix}
1&1\\0&0
\end{pmatrix},\begin{pmatrix}
0&0\\1&0
\end{pmatrix},\begin{pmatrix}
0&0\\0&1
\end{pmatrix}  \right\}
$$
$$
\begin{pmatrix}
a&b\\c&d
\end{pmatrix}=(a-b)\begin{pmatrix}
1&0\\0&0
\end{pmatrix}+b\begin{pmatrix}
1&1\\0&0
\end{pmatrix}+c\begin{pmatrix}
0&0\\1&0
\end{pmatrix}+d\begin{pmatrix}
0&0\\0&1
\end{pmatrix}
$$
$$
\Phi_{F}\begin{pmatrix}
a&b\\c&d
\end{pmatrix}=\begin{pmatrix}
a-b\\b\\c\\d
\end{pmatrix}
$$
## Coordinates on $\mathbb{R}^{n}$
If $B=\{ \vec{e}_{1},\dots,\vec{e}_{n} \}$ is the standard basis for $\mathbb{R}^{n}$, then
$$
\Phi_{B}:\begin{pmatrix}
\lambda_{1}\\\vdots\\\lambda_{n}
\end{pmatrix}\mapsto \begin{pmatrix}
\lambda_{1}\\\vdots\\\lambda_{n}
\end{pmatrix}
$$
So $\Phi_{B}:\mathbb{R}^{n}\to \mathbb{R}^{n}$
Suppose $C=\{ \vec{v}_{1},\dots,\vec{v}_{n} \}$ is a basis for $\mathbb{R}^{n}$, let's think about $\Phi_{C}:\mathbb{R}^{n}\to \mathbb{R}^{n}$
Set 
$$
P=\begin{pmatrix}
\vec{v}_{1}&\vec{v}_{2}&\dots&\vec{v}_{n}
\end{pmatrix}\in M_{n}(\mathbb{R})
$$
Is [[Matrix Inverses|invertible]] since $C$ is a basis, then if
$$
\vec{v}=\lambda_{1}\vec{v}_{1}+\lambda_{2}\vec{v}_{2}+\dots+\lambda_{n}\vec{v}_{n}
$$
$$
= P\begin{pmatrix}
\lambda_{1}\\\lambda_{2}\\\vdots\\\lambda_{n}
\end{pmatrix}
$$
So 
$$
\Phi_{C}(\vec{v})=\begin{pmatrix}
\lambda_{1}\\\vdots\\\lambda_{n}
\end{pmatrix}=P^{-1}\vec{v}
$$
### Example
Show that
$$
\vec{v}_{1}=\begin{pmatrix}
1\\2\\3
\end{pmatrix},\vec{v}_{2}=\begin{pmatrix}
2\\3\\2
\end{pmatrix},\vec{v}_{3}=\begin{pmatrix}
3\\2\\1
\end{pmatrix}
$$
Is a basis for $\mathbb{R}^{3}$ and give the coordinates of $\vec{v}$ with respect to the basis
First we form:
$$
P=\begin{pmatrix}
1&2&3\\2&3&2\\3&2&1
\end{pmatrix}
$$
Then we show $\det P\neq 0$, hence we have a basis
Then find $P ^{-1}$, and finally, compute
$$
\begin{pmatrix}
\lambda_{1}\\\lambda_{2}\\\lambda_{3}
\end{pmatrix}=P ^{-1}\begin{pmatrix}
3\\4\\5
\end{pmatrix}=\frac{1}{2}\begin{pmatrix}
1\\0\\3
\end{pmatrix}
$$
Which is incorrect! Pls fix 


#Mathematics #LinAlg #Definition 