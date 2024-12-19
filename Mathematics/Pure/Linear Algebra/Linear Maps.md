Suppose $V,W$ are [[Real Vectorspaces|vectorspaces]], a linear map (aka linear transformation) is a [[Functions|funciton]] $T:V\to W$ satisfying linearity:
- For all $\vec{u},\vec{v}\in V$, we have
$$
T(\vec{u}+\vec{v})=T(\vec{u})+T(\vec{v})
$$
- For all $\lambda \in\mathbb{R}$, and $\vec{u}\in V$, we have
$$
T(\lambda \vec{u})=\lambda T(\vec{u})
$$
The idea is that linear maps preserve the structure of the vectorspace
## Lemma
If $T:V\to W$ is linear, then $T(\vec{0})=\vec{0}$
### Proof
$$
T(\vec{0})=T(\vec{0}+\vec{0})=T(\vec{0})+T(\vec{0})=2T(\vec{0})
$$
$$
\implies T(\vec{0})=\vec{0}
$$
## Examples
If [[Matrices|$A\in M_{m\times n}(\mathbb{R})$]], then we can define a map $T_{A}:\mathbb{R}^{n}\to \mathbb{R}^{m}$ by $T_{A}(\vec{v})=A\vec{v}$
Check: is $T_{A}$ linear? consider some $\vec{u},\vec{v}\in\mathbb{R}^{n},\lambda \in\mathbb{R}$
$$
T_{A}(\vec{u}+\vec{v})=A(\vec{u}+\vec{v})=A\vec{u}+A\vec{v}=T(\vec{u})+T(\vec{v})
$$
$$
T_{A}(\lambda \vec{u})=A(\lambda \vec{u})=\lambda A\vec{u}=\lambda T(\vec{u})
$$
___
If $B$ is a [[basis|basis]] for $V$, then [[Coordinates|$\Phi_{B}:V\to \mathbb{R}^{n}$]] is a linear map
___
$$
\frac{d }{dx} :\mathbb{R}[x]_{n}\to \mathbb{R}[x]_{n-1}
$$
$$
 p\mapsto \frac{d p}{dx} 
$$
Is a linear map as:

$$
\frac{d }{dx} (p+q)=\frac{d p}{dx} +\frac{d q}{dx} 
$$
$$
\frac{d }{dx} (\lambda p)=\lambda \frac{d p}{dx} 
$$


Similarly:
$$
\int _{0}^{x}:\mathbb{R}[x]_{n}\to \mathbb{R}[x]_{n+1}
$$
$$
p\mapsto \int _{0}^{x}p(t) \, dt 
$$
As:
$$
\int _{0}^{x}(p+q) \, =\int _{0}^{x} p(t)+q(t)\, dt =\int _{0}^{x}p(t) \, dt +\int _{0}^{x}q(t) \, dt 
$$
$$
\int _{0}^{x}\lambda p=\int _{0}^{x}\lambda p(t) \, dt=\lambda \int _{0}^{x}p(t) \, dt 
$$
And
$$
\text{Eval}_{a}:\mathbb{R}[x]_{n}\to \mathbb{R}
$$
$$
 p\mapsto p(a)
$$
are both also linear maps
___
$$
T:\mathbb{R}^{3}\to \mathbb{R}^{3}
$$
$$
 \begin{pmatrix}
x\\y\\z
\end{pmatrix}\mapsto \begin{pmatrix}
x+1\\y\\z
\end{pmatrix}
$$
Is not a linear map, for example
$$
T\begin{pmatrix}
0\\0\\0
\end{pmatrix}=\begin{pmatrix}
1\\0\\0
\end{pmatrix}
$$
Which contradicts the lemma
However if each coordinate is a linear combination of $x,y,z$, then that will be a linear map, for example:
$$
T:\mathbb{R}^{3}\to \mathbb{R}^{3}
$$
$$
 \begin{pmatrix}
x\\y\\z
\end{pmatrix}\mapsto \begin{pmatrix}
2x+2z\\y\\x-y-z
\end{pmatrix}
$$
Is a map, since:
$$
T\begin{pmatrix}
x\\y\\z
\end{pmatrix}=\begin{pmatrix}
2&0&2\\0&1&0\\1&-1&-1
\end{pmatrix}\begin{pmatrix}
x\\y\\z
\end{pmatrix}
$$
___
Not every map is linear, e.g.
$$
\mathbb{R}\to \mathbb{R}
$$
$$
 x\mapsto x^{2}
$$
Which is not linear, for many reasons, such as $4=f(2)=f(1+1)\neq f(1)+f(1)=2$
## Lemma
Suppose $\{ \vec{v}_{1},\dots,\vec{v}_{n} \}$ is a basis for $V$, then
- Any linear map $T:V\to W$ is determined by its values $T(\vec{v}_{1}),T(\vec{v}_{2}),\dots,T(\vec{v}_{n})$
- Given arbitrary vectors $\vec{w}_{1},\vec{w}_{2},\dots,\vec{w}_{n}\in W$, then there exists a linear map $T:V\to W$ with $T(\vec{v}_{1})=\vec{w}_{1},T(\vec{v}_{2})=\vec{w}_{2},\dots,T(\vec{v}_{n})=\vec{w}_{n}$ 
### Proof
First part:
Is any linear map determined by its values?
Suppose $\vec{v}\in V$, then we have $\vec{v}=\lambda_{1}\vec{v}_{1}+\dots+\lambda _{n}\vec{v}_{n}$ for some $\lambda_{i}\in\mathbb{R}$, so 
$$
T(\vec{v})=T(\lambda_{1}\vec{v}_{1}+\dots+\lambda _{n}\vec{v}_{n})=\lambda_{1}T(\vec{v}_{1})+\dots+\lambda_{n}T(\vec{v}_{n})
$$
So any vector in the linear map is in fact determined by its values, hence proved
Second part:
We wish to define such a $T:V\to W$, suppose $\vec{v}\in V$ then $\vec{v}=\lambda_{1}\vec{v}_{1}+\dots+\lambda _{n}\vec{v}_{n}$ for a unique choice of $\lambda_{i}\in\mathbb{R}$, then we define $T:V\to W$
$$
T(\vec{v}):=\lambda_{1}\vec{w}_{1}+\dots+\lambda_{n}\vec{w}_{n}
$$
Note this is well-defined since the $\lambda_{i}$'s are unique. Also note $T(\vec{v}_{i})=\vec{w}_{i}$
Now we have defined a map, but is it linear?
Suppose $\vec{u},\vec{v}\in V,\lambda \in\mathbb{R}$, then $\vec{u}=\lambda_{1}\vec{v}_{1}+\dots+\lambda_{n}\vec{v}_{n}$, and $\vec{v}=\mu_{1}\vec{v}_{1}+\dots+\mu_{n}\vec{v}_{n}$ for some $\lambda_{i},\mu_{i}\in\mathbb{R}$, then
$$
T(\vec{u}+\vec{v})=T((\lambda_{1}+\mu_{1})\vec{v}_{1}+\dots+(\lambda_{n}+\mu_{n})\vec{v}_{n})
$$
$$
= (\lambda_{1}+\mu_{1})\vec{w}_{1}+\dots+(\lambda_{n}+\mu_{n})\vec{w}_{n}
$$
$$
= (\lambda_{1}\vec{w}_{1}+\dots+\lambda_{n}\vec{w}_{n})+(\mu_{1}\vec{w}_{1}+\dots+\mu_{n}\vec{w}_{n})=T(\vec{u})+T(\vec{v})
$$
$$
T(\lambda \vec{u})=T(\lambda\lambda_{1}\vec{v}_{1}+\dots+\lambda\lambda_{n}\vec{v}_{n})
$$
$$
= (\lambda\lambda_{1})\vec{w}_{1}+\dots+(\lambda\lambda_{n})\vec{w}_{n}
$$
$$
=\lambda(\lambda_{1}\vec{w}_{1}+\dots+\lambda_{n}\vec{w}_{n})=\lambda T(\vec{v})
$$
## Lemma
$$
T:\mathbb{R}^{n}\to \mathbb{R}^{n}
$$
is linear iff $\exists A\in M_{m\times n}(\mathbb{R})$ such that
$$
T(\vec{v})=A\vec{v}
$$
### Proof
If direction:
We already know this, so $T$ is linear if the map is matrix multiplication, as shown above in examples
Only if direction:
Consider $\{ \vec{e}_{1},\dots, \vec{e}_{n}\}$ is a basis for $\mathbb{R}^{n}$, then
$$
T\begin{pmatrix}
\lambda_{1}\\\vdots\\\lambda_{n}
\end{pmatrix}=T(\lambda_{1}\vec{e}_{1}+\dots+\lambda_{n}\vec{e}_{n})
$$
$$
= \lambda_{1}T(\vec{e}_{1})+\dots+\lambda_{n}T(\vec{e}_{n})
$$
$$
 =\begin{pmatrix}
T(\vec{e}_{1})&\dots&T(\vec{e}_{n})
\end{pmatrix}\begin{pmatrix}
\lambda_{1}\\\vdots\\\lambda_{n}
\end{pmatrix}
$$
So $T\vec{\lambda}=A\vec{\lambda}$, where 
$$
A=\begin{pmatrix}
T(\vec{e}_{1})&\dots&T(\vec{e}_{n})
\end{pmatrix}
$$
### Example
Find the matrix of the linear map $T:\mathbb{R}^{3}\to \mathbb{R}^{2}$ given by
$$
T\begin{pmatrix}
x\\y\\z
\end{pmatrix}=\begin{pmatrix}
5x+3y-z\\x+2y-3z
\end{pmatrix}
$$
$$
A=\begin{pmatrix}
T(\vec{e}_{1})&T(\vec{e}_{2})&T(\vec{e}_{3})
\end{pmatrix}
$$
$$
= \begin{pmatrix}
T\begin{pmatrix}
1\\0\\0
\end{pmatrix}&T\begin{pmatrix}
0\\1\\0
\end{pmatrix}&T\begin{pmatrix}
0\\0\\1
\end{pmatrix}
\end{pmatrix}=\begin{pmatrix}
5&3&-1\\1&2&3
\end{pmatrix}\in M_{2\times 3}(\mathbb{R})
$$
## Properties of Linear Maps
### Lemma
Suppose $S:U\to V$,$T:V\to W$ are linear, then $T\circ S:U\to W$ is linear, similarly if $S:\mathbb{R}^m\to \mathbb{R}^{n}$, $T:\mathbb{R}^{n}\to \mathbb{R}^k$ are given by $S(\vec{x})-A\vec{x}$, $T(\vec{y})=B\vec{y}$, then $T\circ S(\vec{x})=BA\vec{x}$
#### Proof
Suppose $\vec{u},\vec{v}\in U,\lambda \in\mathbb{R}$, then
$$
T\circ S(\vec{u}+\vec{v})=T(S(\vec{u}+\vec{v}))=T(S(\vec{u})+S(\vec{v}))=T(S(\vec{u}))+T(S(\vec{v}))=T\circ S(\vec{u})+T\circ S(\vec{v})
$$
$$
T\circ S(\lambda \vec{u})=T(S(\lambda \vec{u}))=T(\lambda S(\vec{u}))=\lambda T(S(\vec{u}))=\lambda T\circ S(\vec{u})
$$
For the second statement, note:
$$
T\circ S(\vec{x})=T(S(\vec{x}))=T(A\vec{x})=BA\vec{x}
$$
Which in a way is where matrix multiplication comes from (very cool)

#Mathematics #LinAlg #Definition #Theorem 