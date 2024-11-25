Suppose [[vectors|vectors]] $\vec{u}_{1},\vec{u}_{2},\dots,\vec{u}_{k}\in\mathbb{R}^{n}$, then we say $\vec{u}_{1},\vec{u}_{2},\dots,\vec{u}_{k}$ are linearly independent iff the only solution to:
$$
\lambda_{1}\vec{u}_{1}+\dots+\lambda_{k}\vec{u}_{k}=\vec{0}
$$
Is $\lambda_{1}=\lambda_{2}=\dots=\lambda_{k}=0$ 
Another way of thinking of this is if we have a [[Matrices|matrix]] $A$:
$$
A=\begin{pmatrix}
\vec{u}_{1}&\dots&\vec{u}_{k}
\end{pmatrix}\in M_{n\times k}(\mathbb{R})
$$
Then $\vec{u}_{1},\vec{u}_{2},\dots,\vec{u}_{k}$ are linearly indepedent iff $A\vec{\lambda}=\vec{0}$, only if $\vec{\lambda}=\vec{0}$
## Linear Dependence
$\vec{u}_{1},\vec{u}_{2},\dots,\vec{u}_{k}\in\mathbb{R}^{n}$ are called linearly dependent iff they are not linearly independent
### Example
Suppse $\vec{u},\vec{v}\in\mathbb{R}^{n}$, $\vec{u}\neq  \vec{0}\neq \vec{v}$, then $\{ \vec{u},\vec{v} \}$ is linearly dependent iff $\vec{u},\vec{v}$ are multiples of each other (they are collinear)
#### Proof
$\vec{u},\vec{v}$ are linearly dependent iff $\exists\lambda,\mu \in\mathbb{R}$, where neither are $\hspace{0pt}0$ such that $\lambda \vec{u}+\mu \vec{v}= \vec{0}$
Say $\lambda \neq 0$ without loss of generality, then $\vec{u}=\left( -\frac{\mu}{\lambda} \right)\vec{v}$, also given $\vec{u}\neq 0$
## Extending Linearly Independent Sets
Suppose $\vec{u}_{1},\dots,\vec{u}_{r}\in V$ are linearly independent, and suppose $\vec{u}\in V$, [[span|$\vec{u} \not\in \text{span}< \vec{u}_{1},\dots,\vec{u}_{r} >$]], then $\{\vec{u}, \vec{u}_{1},\dots,\vec{u}_{r} \}$ is also linearly indipendent
This can be used to find [[Basis|bases]], but may not terminate, so is potentially not as useful as [[Span#Lemma 2|this method]]  
### Proof
Suppose $\vec{u},\vec{u}_{1},\dots,\vec{u}_{r}$ are not linearly independent, then there exists not all $\lambda,\lambda_{i}\in\mathbb{R},1\leq i\leq r$ such that:
$$
\lambda \vec{u}+\lambda_{1}\vec{u}_{1}+\dots+\lambda_{r}\vec{u}_{r}=\vec{0}
$$
Then there are two possibilities
$\lambda=0$ which implies:
$$
\lambda_{1}\vec{u}_{1}+\dots+\lambda_{r}\vec{u}_{r}=\vec{0}
$$
So $\lambda_{1}=\lambda_{2}=\dots=\lambda _{r}=0$ by linear independence of $\vec{u}_{1},\dots,\vec{u}_{r}$ which is a contradiction
Or $\lambda \neq 0$ which implies:
$$
\vec{u}=\left( -\frac{\lambda_{1}}{\lambda} \right)\vec{u}_{1}+\dots+\left( -\frac{\lambda_{r}}{\lambda} \right)\vec{u}_{r}\in \text{span}< \vec{u}_{1},\dots,\vec{u}_{r} > 
$$
Which is also a contradiction
## Example
Consider vectors:
$$
\vec{u}_{1}=\begin{pmatrix}
1\\5\\-2
\end{pmatrix},\vec{u}_{2}=\begin{pmatrix}
1\\1\\2
\end{pmatrix},\vec{u}_{3}=\begin{pmatrix}
1\\-2\\5
\end{pmatrix}\in \mathbb{R}^{3}
$$
Are these linearly indipendent?
We want to solve:
$$
\lambda_{1}\vec{u}_{1}+\lambda_{2}\vec{u}_{2}+\lambda_{3}\vec{u}_{3}=\vec{0}\iff A\vec{\lambda}=\begin{pmatrix}
\vec{u}_{1}&\vec{u}_{2}&\vec{u}_{3}
\end{pmatrix}\begin{pmatrix}
\lambda_{1}\\\lambda_{2}\\\lambda_{3}
\end{pmatrix}=\vec{0}
$$
![[Linear Independence 2024-11-19 11.25.53.excalidraw]]
Since there is a row of zeros, there will be infinitely many solutions, and, in partiular, there must then be a non-zero solution, we can pick one e.g. $\lambda_{3}=4,\lambda_{2}=-7,\lambda_{1}=3$, so
$$
3\vec{u}_{1}-7\vec{u}_{2}+4\vec{u}_{3}=\vec{0}
$$
So they are not linearly independent
___
$$
\vec{v}_{1}=\begin{pmatrix}
1\\3\\1\\2
\end{pmatrix},\vec{v}_{2}=\begin{pmatrix}
2\\-1\\-5\\3
\end{pmatrix},\vec{v}_{3}=\begin{pmatrix}
1\\0\\-2\\-1
\end{pmatrix}\in \mathbb{R}^{4}
$$
Are these linearly independent?
Same process:
![[Linear Independence 2024-11-19 11.34.55.excalidraw]]
There are no free variables, so unique solution to $\lambda_{1}\vec{v}_{1}+\lambda_{2}\vec{v}_{2}+\lambda_{3}\vec{v}_{3}=\vec{0}$ hence $\vec{v}_{1},\vec{v}_{2},\vec{v}_{3}$ are linearly independent

#Mathematics #LinAlg #Definition