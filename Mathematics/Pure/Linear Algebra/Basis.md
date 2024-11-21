A basis for a [[Real Vectorspaces|Vectorspace]] $V$ is a finite [[sets|set]] of [[Vectors|vectors]]:
$$
\{ \vec{v}_{1},\vec{v}_{2},\dots,\vec{v}_{n} \}\subseteq V
$$
Such that:
- $\{ \vec{v}_{1},\vec{v}_{2},\dots,\vec{v}_{n} \}$ is [[Linear Independence|linearly independent]]
- $\{ \vec{v}_{1},\vec{v}_{2},\dots,\vec{v}_{n} \}$ [[Span|spans]] $V$
## Examples
For [[Vectorspace Rn|$\mathbb{R}^{n}$]] $\{\vec{e}_{1},\vec{e}_{2},\dots,\vec{e}_{n} \}$ (the standard basis), is the standard basis for $\mathbb{R}^{n}$
FOr $\mathbb{R}[x]_{n}$,:
$$
\{ 1,x,x^{2},\dots,x^{n} \}\subseteq \mathbb{R}[x]_{n}
$$
Is a basis for $\mathbb{R}[x]_{n}$; if $t\in\mathbb{R}[x]_{n}$, then 
$$
a_{0}+a_{1}x+\dots+a_{n}x^{n}\in \text{span}< 1,x,\dots x^{n} > 
$$
So 
$$
\text{span}< \{ 1,x,x^{2},\dots,x^{n} \} > =\mathbb{R}[x]_{n}
$$
Also if $a_{0}+a_{1}x+\dots+a_{n}x^{n}=0$, then $a_{0}=a_{1}=\dots=a_{n}=0$
Note, for example, $\mathbb{R}[x]$ doesn't have a vbasis, since it doesn't have a finite spanning the set
Are the polynomials $1-x,x-x^{2},1-x^{2}$ a basis for $\mathbb{R}[x]_{2}$? The answer is no, since:
$$
1-x+(x-x^{2})-(1-x^{2})=0
$$
So these elements are not linearly independent
If we write $E^{ij}\in M_{m\times n}(\mathbb{R})$ for the matrix that has $(i,j)$rh entry $\hspace{0pt}1$, and all other entries $\hspace{0pt}0$, then
$$
\{ E^{ij}\mid1\leq i\leq m,1\leq j\leq n \}\subseteq M_{m\times n}(\mathbb{R})
$$
Why? If it is spanning,
$$
A=\left( a_{ij}=\sum_{1\leq i \leq m,1\leq j\leq n} \right)a_{ij}E^ij 
$$