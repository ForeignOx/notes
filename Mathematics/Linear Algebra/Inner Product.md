## Real Inner Products
An inner product on a [[Real Vectorspaces|real vectorspace]] $V$ is a [[Linear Maps|map]] $(\cdot,\cdot):V\times V\mapsto \mathbb{R}$, which assigns each pair of vectors $\underline{u},\underline{v}\in V$ a [[Real Numbers|real number]] $(\underline{u},\underline{v})$, satisfying the following for all $\underline{u},\underline{v},\underline{w}\in V$, $\lambda \in\mathbb{R}$:
- $(\underline{u},\underline{v})=(\underline{v},\underline{u})$ symmetry
- $(\underline{u}+\underline{v},\underline{w})=(\underline{u},\underline{w})+(\underline{v},\underline{w})$
- $(\lambda \underline{u},\underline{v})=\lambda(\underline{u},\underline{v})$ these last two mean that it is [[Linear|linear]] in first order, with symmetry as well, linear in second order; a symmetric [[Bilinear Form|bilinear form]]
- $(\underline{v},\underline{v})\geq 0$ with $(\underline{v},\underline{v})=0\iff \underline{v}=\underline{0}$ (positivity)
Essentially, a bilinear form which is symmetric and positie defines an inner product $(\underline{u},\underline{v})=B(\underline{u},\underline{v})$
## Encoding with Matrices
We can always encode an inner product via a [[Matrices|matrix]], since you can encode a bilinear product