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
Say $\lambda \neq 0$ without loss of generality, then $\vec{u}=\left( -\frac{\mu}{\lambda} \right)\vec{v}$, also given $\vec{u}\neq 0$,