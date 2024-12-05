Suppose $V,W$ are [[Real Vectorspaces|vectorspaces]], a linear map is a [[Functions|funciton]] $T:V\to W$ satisfying:
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
If $B$ is a [[basis|basis]] for $V$, then $\Phi_{B}:V\to \mathbb{R}^{n}$ is a linear map
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