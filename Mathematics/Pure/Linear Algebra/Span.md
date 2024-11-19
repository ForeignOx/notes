The span, or linear span of some [[Vectors|vectors]] in a [[Real Vectorspaces|vectorspace]] $V$, $\vec{u_{1}},\vec{u_{2}},\dots,\vec{u_{k}}\in V$ is the [[Subsets|subset]]:
$$
\text{span}(\vec{u_{1}},\vec{u_{2}},\dots,\vec{u_{k}}):=\{ \lambda_{1}\vec{u_{1}}+\lambda_{2}\vec{u_{2}}+\dots+\lambda_{k}\vec{u_{k}}\mid\lambda_{1},\lambda_{2},\dots,\lambda_{k}\in \mathbb{R} \}
$$
i.e. the [[SETS|set]] of all [[Linear Combinations|linear combinations]] of $\vec{u_{1}},\vec{u_{2}},\dots,\vec{u_{k}}$
Other ways of writing this include:
$$
\text{span}(\{ \vec{u_{1}},\vec{u_{2}},\dots,\vec{u_{k}} \}),<\vec{u_{1}},\vec{u_{2}},\dots,\vec{u_{k}}>,<\{ \vec{u_{1}},\vec{u_{2}},\dots,\vec{u_{k}} \}>
$$
We say that $U$ is spanned by $\vec{u_{1}},\vec{u_{2}},\dots,\vec{u_{k}}$
___
Suppose
$$
\vec{u}_{i}=\begin{pmatrix}
u_{1i}\\u_{2i}\\\vdots\\u_{ni}
\end{pmatrix}
$$
Form a [[Matrices|matrix]]
$$
A=\begin{pmatrix}
\vec{u}_{1}&\vec{u}_{2}&\dots&\vec{u}_{k}
\end{pmatrix}\in M_{n\times k}(\mathbb{R})
$$
Then we have:
$$
\lambda_{1}\vec{u}_{1}+\lambda_{2}\vec{u}_{2}+\dots+\lambda_{k}\vec{u}_{k}=\begin{pmatrix}
\lambda_{1}u_{11}&\lambda_{2}u_{12} & \dots &\lambda_{k}u_{1k}\\\lambda_{1}u_{21}&\lambda_{2}u_{22} & \dots &\lambda_{k}u_{2k}\\\vdots&\vdots&&\vdots\\\lambda_{1}u_{n1}&\lambda_{2}u_{n2} & \dots &\lambda_{k}u_{nk}
\end{pmatrix}
$$
$$
=\begin{pmatrix}
u_{11}&u_{12}&\dots&u_{1k}\\u_{21}&u_{22}&\dots&u_{2k}\\\vdots&\vdots&&\vdots\\u_{n1}&u_{n 2}&\dots&u_{nk}
\end{pmatrix}\begin{pmatrix}
\lambda_{1}\\\lambda_{2}\\\vdots\\\lambda_{k}
\end{pmatrix}=A\vec{\lambda}
$$
So this means:
$$
\text{span}<\vec{u}_{1},\vec{u}_{2},\dots,\vec{u}_{k}> = \{ A\vec{\lambda}\mid\vec{\lambda}\in \mathbb{R}^{k} \}=\{ \vec{b}\in \mathbb{R}^{n}\mid A\vec{\lambda}=\vec{b}\text{ has a solution} \}
$$
## Lemma
Suppose $\vec{u}_{1},\vec{u}_{2},\dots,\vec{u}_{k}\in\mathbb{R}^{n}$ and suppose $\vec{u}_{1}\in \text{span}<\vec{u}_{2},\dots,\vec{u}_{k}>$, then
$$
U:=\text{span}<\vec{u}_{1},\vec{u}_{2},\dots,\vec{u}_{k}>=\text{span}<\vec{u}_{2},\dots,\vec{u}_{k}> :=V
$$
### Proof
First note certainly $V\subseteq U$, we must show $U\subseteq V$ since $\vec{u}_{1}\in V$, we have:
$$
\vec{u}_{1}=\mu_{2}\vec{u}_{2}+\dots+\mu_{k}\vec{u}_{k}
$$
For some $\mu_{i}\in\mathbb{R}$, then:
$$
\lambda_{1} \vec{u}_{1}+\lambda_{2}\vec{u}_{2}+\dots+\lambda_{k}\vec{u}_{k}=\lambda_{1}(\mu_{2}\vec{u}_{2}+\dots+\mu_{k}\vec{u}_{k})+\lambda_{2}\vec{u}_{2}+\dots+\lambda_{k}\vec{u}_{k}
$$
$$
= (\lambda_{1}\mu_{2}+\lambda_{2})\vec{u}_{2}+\dots+(\lambda_{1}\mu_{k}+\lambda_{k})\vec{u}_{k}\in V
$$


#Mathematics #LinAlg #Definition #Theorem