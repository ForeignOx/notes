Suppose $V,W$ are [[Vectorspaces|vectorspaces]], a linear map (aka linear transformation) is a [[Functions|function]] $T:V\to W$ satisfying linearity:
- For all $\underline{u},\underline{v}\in V$, we have
$$
T(\underline{u}+\underline{v})=T(\underline{u})+T(\underline{v})
$$
- For all $\lambda \in\mathbb{R}$, and $\underline{u}\in V$, we have
$$
T(\lambda \underline{u})=\lambda T(\underline{u})
$$
The idea is that linear maps preserve the structure of the vectorspace
## Lemma
If $T:V\to W$ is linear, then $T(\underline{0})=\underline{0}$
### Proof
$$
T(\underline{0})=T(\underline{0}+\underline{0})=T(\underline{0})+T(\underline{0})=2T(\underline{0})
$$
$$
\implies T(\underline{0})=\underline{0}
$$
## Examples
If [[Matrices|$A\in M_{m\times n}(\mathbb{R})$]], then we can define a map $T_{A}:\mathbb{R}^{n}\to \mathbb{R}^{m}$ by $T_{A}(\underline{v})=A\underline{v}$
Check: is $T_{A}$ linear? consider some $\underline{u},\underline{v}\in\mathbb{R}^{n},\lambda \in\mathbb{R}$
$$
T_{A}(\underline{u}+\underline{v})=A(\underline{u}+\underline{v})=A\underline{u}+A\underline{v}=T(\underline{u})+T(\underline{v})
$$
$$
T_{A}(\lambda \underline{u})=A(\lambda \underline{u})=\lambda A\underline{u}=\lambda T(\underline{u})
$$
___
If $B$ is a [[Basis|Basis]] for $V$, then [[Coordinates|$\Phi_{B}:V\to \mathbb{R}^{n}$]] is a linear map
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
Suppose $\{ \underline{v}_{1},\dots,\underline{v}_{n} \}$ is a basis for $V$, then
- Any linear map $T:V\to W$ is determined by its values $T(\underline{v}_{1}),T(\underline{v}_{2}),\dots,T(\underline{v}_{n})$
- Given arbitrary vectors $\underline{w}_{1},\underline{w}_{2},\dots,\underline{w}_{n}\in W$, then there exists a linear map $T:V\to W$ with $T(\underline{v}_{1})=\underline{w}_{1},T(\underline{v}_{2})=\underline{w}_{2},\dots,T(\underline{v}_{n})=\underline{w}_{n}$ 
### Proof
First part:
Is any linear map determined by its values?
Suppose $\underline{v}\in V$, then we have $\underline{v}=\lambda_{1}\underline{v}_{1}+\dots+\lambda _{n}\underline{v}_{n}$ for some $\lambda_{i}\in\mathbb{R}$, so 
$$
T(\underline{v})=T(\lambda_{1}\underline{v}_{1}+\dots+\lambda _{n}\underline{v}_{n})=\lambda_{1}T(\underline{v}_{1})+\dots+\lambda_{n}T(\underline{v}_{n})
$$
So any vector in the linear map is in fact determined by its values, hence proved
Second part:
We wish to define such a $T:V\to W$, suppose $\underline{v}\in V$ then $\underline{v}=\lambda_{1}\underline{v}_{1}+\dots+\lambda _{n}\underline{v}_{n}$ for a unique choice of $\lambda_{i}\in\mathbb{R}$, then we define $T:V\to W$
$$
T(\underline{v}):=\lambda_{1}\underline{w}_{1}+\dots+\lambda_{n}\underline{w}_{n}
$$
Note this is well-defined since the $\lambda_{i}$'s are unique. Also note $T(\underline{v}_{i})=\underline{w}_{i}$
Now we have defined a map, but is it linear?
Suppose $\underline{u},\underline{v}\in V,\lambda \in\mathbb{R}$, then $\underline{u}=\lambda_{1}\underline{v}_{1}+\dots+\lambda_{n}\underline{v}_{n}$, and $\underline{v}=\mu_{1}\underline{v}_{1}+\dots+\mu_{n}\underline{v}_{n}$ for some $\lambda_{i},\mu_{i}\in\mathbb{R}$, then
$$
T(\underline{u}+\underline{v})=T((\lambda_{1}+\mu_{1})\underline{v}_{1}+\dots+(\lambda_{n}+\mu_{n})\underline{v}_{n})
$$
$$
= (\lambda_{1}+\mu_{1})\underline{w}_{1}+\dots+(\lambda_{n}+\mu_{n})\underline{w}_{n}
$$
$$
= (\lambda_{1}\underline{w}_{1}+\dots+\lambda_{n}\underline{w}_{n})+(\mu_{1}\underline{w}_{1}+\dots+\mu_{n}\underline{w}_{n})=T(\underline{u})+T(\underline{v})
$$
$$
T(\lambda \underline{u})=T(\lambda\lambda_{1}\underline{v}_{1}+\dots+\lambda\lambda_{n}\underline{v}_{n})
$$
$$
= (\lambda\lambda_{1})\underline{w}_{1}+\dots+(\lambda\lambda_{n})\underline{w}_{n}
$$
$$
=\lambda(\lambda_{1}\underline{w}_{1}+\dots+\lambda_{n}\underline{w}_{n})=\lambda T(\underline{v})
$$
## Lemma
$$
T:\mathbb{R}^{n}\to \mathbb{R}^{n}
$$
is linear iff $\exists A\in M_{m\times n}(\mathbb{R})$ such that
$$
T(\underline{v})=A\underline{v}
$$
### Proof
If direction:
We already know this, so $T$ is linear if the map is matrix multiplication, as shown above in examples
Only if direction:
Consider $\{ \underline{e}_{1},\dots, \underline{e}_{n}\}$ is a basis for $\mathbb{R}^{n}$, then
$$
T\begin{pmatrix}
\lambda_{1}\\\vdots\\\lambda_{n}
\end{pmatrix}=T(\lambda_{1}\underline{e}_{1}+\dots+\lambda_{n}\underline{e}_{n})
$$
$$
= \lambda_{1}T(\underline{e}_{1})+\dots+\lambda_{n}T(\underline{e}_{n})
$$
$$
 =\begin{pmatrix}
T(\underline{e}_{1})&\dots&T(\underline{e}_{n})
\end{pmatrix}\begin{pmatrix}
\lambda_{1}\\\vdots\\\lambda_{n}
\end{pmatrix}
$$
So $T\underline{\lambda}=A\underline{\lambda}$, where 
$$
A=\begin{pmatrix}
T(\underline{e}_{1})&\dots&T(\underline{e}_{n})
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
T(\underline{e}_{1})&T(\underline{e}_{2})&T(\underline{e}_{3})
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
Suppose $S:U\to V$, $T:V\to W$ are linear, then $T\circ S:U\to W$ is linear, similarly if $S:\mathbb{R}^m\to \mathbb{R}^{n}$, $T:\mathbb{R}^{n}\to \mathbb{R}^k$ are given by $S(\underline{x})-A\underline{x}$, $T(\underline{y})=B\underline{y}$, then $T\circ S(\underline{x})=BA\underline{x}$
#### Proof
Suppose $\underline{u},\underline{v}\in U,\lambda \in\mathbb{R}$, then
$$
T\circ S(\underline{u}+\underline{v})=T(S(\underline{u}+\underline{v}))=T(S(\underline{u})+S(\underline{v}))=T(S(\underline{u}))+T(S(\underline{v}))=T\circ S(\underline{u})+T\circ S(\underline{v})
$$
$$
T\circ S(\lambda \underline{u})=T(S(\lambda \underline{u}))=T(\lambda S(\underline{u}))=\lambda T(S(\underline{u}))=\lambda T\circ S(\underline{u})
$$
For the second statement, note:
$$
T\circ S(\underline{x})=T(S(\underline{x}))=T(A\underline{x})=BA\underline{x}
$$
Which in a way is where matrix multiplication comes from (very cool)
## Proposition
If $T:V\to W$ is linear, then the following are equivalent:
- [[Kernel|$\text{ker}(T)=0=\{ \underline{0} \}$]]
- $T$ is [[Injective Functions|injective]] (1-1)
- If $\{ \underline{v}_{1},\dots,\underline{v}_{n} \}\subseteq V$ are [[Linear Independence|linearly independent]], then $\{ T(\underline{v}_{1}),\dots,T(\underline{v}_{n}) \}\subseteq W$ are linearly independent
### Proof
$1\implies2$ Assume 1:
Suppose $T(\underline{u})=T(\underline{v})$, so for injectivity we want to show $\underline{u}=\underline{v}$
$$
T(\underline{u}-\underline{v})=T(\underline{u})-T(\underline{v})=\underline{0}
$$
$$
\implies \underline{u}-\underline{v}\in \text{ker}(T)=0
$$
$$
\implies \underline{u}-\underline{v}=\underline{0}
$$
$$
\implies \underline{u}=\underline{v}
$$
$2\implies 3$: Assume $2$:
Suppose 
$$
\lambda_{1}T(\underline{v}_{1})+\dots+\lambda_{n}T(\underline{v}_{n})=\underline{0}
$$
$$
\implies T(\lambda_{1}\underline{v}_{1}+\dots+\lambda_{n}\underline{v}_{n})=\underline{0}=T(\underline{0})
$$
Hence, since $T$ is 1$\hspace{0pt}-1$, 
$$
\lambda_{1}\underline{v}_{1}+\dots+\lambda_{n}\underline{v}_{n}=\underline{0} 
$$
$$
\implies \lambda_{1}=\dots=\lambda_{n}=0
$$
So the $\underline{v}_{i}$'s are linearly independent
$3\implies1$: Assume $3$
Suppose $\underline{u}\neq 0$ and $\underline{u}\in\text{ker}(T)$ then $\{ \underline{u} \}$ is linearly independent, but $\{ \underline{0} \}=\{ T(\underline{u}) \}$ is not linearly independent, which contradicts our $3$, so $\text{ker}(T)=\{ \underline{0} \}$
### Corollary
Let $T:V\to W$ be linear and suppose $\text{ker}(T)=0$, then if $\{ \underline{v}_{1},\dots,\underline{v}_{n} \}$ is a basis for $\underline{v}$, we have that $\{ T(\underline{v}_{1}),\dots,T(\underline{v}_{n}) \}$ is a basis for $\text{im}(T)$, hence $\text{rk}(T)=\dim(\text{im}(T))=n=\dim(V)$
#### Proof
$\{ T(\underline{v}_{1}),\dots,T(\underline{v}_{n}) \}$ is spanning by [[Image#Lemma|this lemma]] and linearly independent by the proposition, so is a basis for $\text{im}(T)$
___
## Symmetric Linear Operators
A linear map or linear operator is symmetric if it is [[Self-Adjoint|self-adjoint]]
### Theorem
Associated with each [[Inner Product|inner product]], there is a special linear operator which is symmetric with respect to that inner product
### Examples
[[Legendre's Equation|Legendre]], $\mathcal{L}_{L}f=(1-x^{2})f''-2xf'$ is symmetric with respect to inner product

#Mathematics #LinAlg #Definition #Theorem 