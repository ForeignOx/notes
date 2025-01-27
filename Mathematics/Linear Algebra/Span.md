The span, or linear span of some [[Vectors|vectors]] in a [[Real Vectorspaces|vectorspace]] $V$, $\underline{u_{1}},\underline{u_{2}},\dots,\underline{u_{k}}\in V$ is the [[Subsets|subset]]:
$$
\text{span}(\underline{u}_{1},\underline{u}_{2},\dots,\underline{u}_{k}):=\{ \lambda_{1}\underline{u}_{1}+\lambda_{2}\underline{u}_{2}+\dots+\lambda_{k}\underline{u}_{k}\mid\lambda_{1},\lambda_{2},\dots,\lambda_{k}\in \mathbb{R} \}
$$
i.e. the [[Sets|set]] of all [[Linear Combinations|linear combinations]] of $\underline{u_{1}},\underline{u_{2}},\dots,\underline{u_{k}}$
Other ways of writing this include:
$$
\text{span}(\{ \underline{u}_{1},\underline{u}_{2},\dots,\underline{u}_{k} \}),<\underline{u}_{1},\underline{u}_{2},\dots,\underline{u}_{k}>,<\{ \underline{u}_{1},\underline{u}_{2},\dots,\underline{u}_{k} \}>
$$
We say that $U$ is spanned by $\underline{u}_{1},\underline{u}_{2},\dots,\underline{u}_{k}$
___
Suppose
$$
\underline{u}_{i}=\begin{pmatrix}
u_{1i}\\u_{2i}\\\vdots\\u_{ni}
\end{pmatrix}
$$
Form a [[Matrices|matrix]]
$$
A=\begin{pmatrix}
\underline{u}_{1}&\underline{u}_{2}&\dots&\underline{u}_{k}
\end{pmatrix}\in M_{n\times k}(\mathbb{R})
$$
Then we have:
$$
\lambda_{1}\underline{u}_{1}+\lambda_{2}\underline{u}_{2}+\dots+\lambda_{k}\underline{u}_{k}=\begin{pmatrix}
\lambda_{1}u_{11}&\lambda_{2}u_{12} & \dots &\lambda_{k}u_{1k}\\\lambda_{1}u_{21}&\lambda_{2}u_{22} & \dots &\lambda_{k}u_{2k}\\\vdots&\vdots&&\vdots\\\lambda_{1}u_{n1}&\lambda_{2}u_{n2} & \dots &\lambda_{k}u_{nk}
\end{pmatrix}
$$
$$
=\begin{pmatrix}
u_{11}&u_{12}&\dots&u_{1k}\\u_{21}&u_{22}&\dots&u_{2k}\\\vdots&\vdots&&\vdots\\u_{n1}&u_{n 2}&\dots&u_{nk}
\end{pmatrix}\begin{pmatrix}
\lambda_{1}\\\lambda_{2}\\\vdots\\\lambda_{k}
\end{pmatrix}=A\underline{\lambda}
$$
So this means:
$$
\text{span}<\underline{u}_{1},\underline{u}_{2},\dots,\underline{u}_{k}> = \{ A\underline{\lambda}\mid\underline{\lambda}\in \mathbb{R}^{k} \}=\{ \underline{b}\in \mathbb{R}^{n}\mid A\underline{\lambda}=\underline{b}\text{ has a solution} \}
$$
## Lemma
Suppose $\underline{u}_{1},\underline{u}_{2},\dots,\underline{u}_{k}\in V$ and suppose $\underline{u}_{1}\in \text{span}<\underline{u}_{2},\dots,\underline{u}_{k}>$, then
$$
U:=\text{span}<\underline{u}_{1},\underline{u}_{2},\dots,\underline{u}_{k}>=\text{span}<\underline{u}_{2},\dots,\underline{u}_{k}> :=V
$$
### Proof
First note certainly $V\subseteq U$, we must show $U\subseteq V$ since $\underline{u}_{1}\in V$, we have:
$$
\underline{u}_{1}=\mu_{2}\underline{u}_{2}+\dots+\mu_{k}\underline{u}_{k}
$$
For some $\mu_{i}\in\mathbb{R}$, then:
$$
\lambda_{1} \underline{u}_{1}+\lambda_{2}\underline{u}_{2}+\dots+\lambda_{k}\underline{u}_{k}=\lambda_{1}(\mu_{2}\underline{u}_{2}+\dots+\mu_{k}\underline{u}_{k})+\lambda_{2}\underline{u}_{2}+\dots+\lambda_{k}\underline{u}_{k}
$$
$$
= (\lambda_{1}\mu_{2}+\lambda_{2})\underline{u}_{2}+\dots+(\lambda_{1}\mu_{k}+\lambda_{k})\underline{u}_{k}\in V
$$
## Lemma 2
Suppose that $\underline{u}_{1},\dots,\underline{u}_{r}$ is not [[Linear Independence|linearly independent]], then there exists some $1\leq i\leq r$ such that $\underline{u}_{i}\in\text{span}< \underline{u}_{1},\dots,\underline{u}_{i-1},\underline{u}_{i+1},\dots,\underline{u}_{r} >$, so in particular, we have
$$
\text{span}< \underline{u}_{1},\dots,\underline{u}_{r} > =\text{span}< \underline{u}_{1},\dots,\underline{u}_{i-1},\underline{u}_{i+1},\dots,\underline{u}_{r} >
$$
So if you have a finite spanning set for $V$, you can keep removing elements from it, (staying spanning), until you arrive at a linearly independent spanning set; a [[Basis|Basis]] 
### Proof
There exists $\lambda_{j}\in\mathbb{R},1\leq j\leq r$ not all $\hspace{0pt}0$ such that $\lambda_{1}\underline{u}_{1}+\dots+\lambda_{r}\underline{u}_{r}= \underline{0}$, there must in fact be one that is non-zero, so we can suppose that $\lambda_{i}\neq 0$, then:
$$
\underline{u}_{i}=\left( -\frac{\lambda_{1}}{\lambda_{i}} \right)\underline{u}_{1}+\dots+\left( -\frac{\lambda_{i-1}}{\lambda_{i}} \right)\underline{u}_{i-1}+\left( -\frac{\lambda_{i+1}}{\lambda_{i}} \right)\underline{u}_{i+1}+\dots+\left( -\frac{\lambda_{r}}{\lambda_{i}} \right)\underline{u}_{r}
$$
$$
 \in \text{span}< \underline{u}_{1},\dots,\underline{u}_{i-1},\underline{u}_{i+1},\dots,\underline{u}_{r} >
$$
The second part of the statement now follows from the lemma above


#Mathematics #LinAlg #Definition #Theorem