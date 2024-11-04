A random variable $X$ on [[Sample Spaces|$\Omega$]] is a mapping from $\Omega$ to some set of possible values
$$
X:\Omega\to \mathbb{Y}\text{ (some arbitrary sace)}
$$
$$
X(\Omega)=\{ X(\omega)|\omega \in \Omega \}
$$
$$
X(\omega)\in \mathbb{Y}
$$

For us, we will be concerned with $X(\Omega)\subset \mathbb{R}$ or $\mathbb{R}^n$
We now define [[Probabilities|probability]] function $\mathbb{P}_{X}(B)$, where $B\in\mathbb{Y}$:
$$
\mathbb{P}_{X}(B):X(\Omega)\to[0,1]
$$
$$
\mathbb{P}_{X}(B):=\mathbb{P}((X \in B))=\mathbb{P}(X ^{-1}(B))=\mathbb{P}(\{ \omega\mid X(\omega) \in B \})
$$
Where $X ^{-1}$ is the [[Image and Pre-Image|pre-image]] of $X$, this is also known as the distribution/cumulative density/distribution function of $X$
## Examples
Tossing a fair coin thrice and let $X$ denote the number of heads:

| $\omega$    | HHH | HHT | HTT | HTH | THT | THH | TTH | TTT |
| ----------- | --- | --- | --- | --- | --- | --- | --- | --- |
| $X(\omega)$ | 3   | 2   | 1   | 2   | 1   | 2   | 1   | 0   |
Let $A_{1}=\{ X=2 \},A_{2}=\{ X \in[0,1.5] \},A_{3}=\{ 2.5\leq X\leq 4.5 \}$,
$$
A_{1}=\{ X=2 \}=\{ \omega:X(\omega)=2 \}=X ^{-1}(\{ 2 \})=\{ HHT,HTH,THH \}\subseteq\Omega
$$
$$
\mathbb{P}(A_{i})=\frac{|A_{i}|}{|\Omega|}=\frac{3}{2^{3}}=\frac{3}{8}
$$
$$
A_{2}=\{ \omega\mid0\leq X(\omega)\leq 1.5 \}=X ^{-1}([0,1.5])=\{ \omega\mid X(\omega)=0\text{, or }X(\omega)=1 \}
$$
$$
= \{ TTT,HTT,THT,TTH \}
$$
$$
\mathbb{P}(A_{2})=\frac{|A_{2}|}{|\Omega|}=\frac{4}{2^{3}}=\frac{1}{2}
$$
___
Tossing $\hspace{0pt}2$ fair dice and let $X$ be the random variable denoting the sum of the scores. For this example,
$$
\Omega=\{ (1,1),(1,2),\dots,(1,6),(2,1),\dots \}=\{ (i,j)\mid1\leq i\leq 6,1\leq j\leq 6 \}
$$
$$
|\Omega|=6^{2}
$$
$$
 X:\Omega\to \mathbb{R}
$$
$$
 \omega \mapsto X(\omega)
$$
$$
(i,j)\mapsto X(i,j)=i+j
$$
## Theorem
Let $X:\Omega\to \mathbb{R}$ be a random variable, then $\mathbb{P}_{X}$ is a probability on $\mathbb{R}$
### Proof
We need to show $\mathbb{P}_{X}$ satisfies the axioms of probability:
$$
\mathbb{P}_{X}(\text{whole space})=\mathbb{P}_{X}(\mathbb{R})=1
$$
$$
\mathbb{P}_{X}(\mathbb{R})=\mathbb{P}(X ^{-1}(\mathbb{R}))=\mathbb{P}(\Omega)=1
$$
As $X ^{-1}(\mathbb{R})=\{ \omega \mid X(\omega)\in\mathbb{R} \}=\Omega$ 