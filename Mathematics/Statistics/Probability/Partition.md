The [[sets|sets]] $E_{1},E_{2},\dots,E_{k}\in\mathfrak{F}$ form a finite partition of the [[Sample Spaces|sample space]] $\Omega$ if it satisfies the following properties:
- $\mathbb{P}(E_{i})>0$ for all $1\leq i\leq k$
- $E_{i}$ and $E_{j}$ are pairwise disoint, i.e. $\forall i\neq j,E_{i}\cap E_{j}=\emptyset$
- $\Omega=\bigcup_{i=1}^k E_{i}$
An easy upshot of this is that $\sum_{i=1}^k\mathbb{P}(E_{i})=1$ this is true since
$$
\Omega=\bigcup_{i=1}^kE_{i}
$$
$E_{i}$ are pairwise [[Mutual Exclusivity|mutually exclusive]], so we can take the probability of both sides to get
$$
1=\mathbb{P}\left( \bigcup_{i=1}^k E_{i}\right)=\sum_{i=1}^k(\mathbb{P}(E_{i}))
$$

