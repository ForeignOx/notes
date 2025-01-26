Suppose $V$ and $W$ are finite dimensional [[Real Vectorspaces|vectorspaces]], and [[Linear Maps|$T:V\to W$]] is linear, then the [[Kernel|nullity]] and [[Image|rank]] are related to the [[Dimension|dimension]] of $V$ like so:
$$
\text{rk}(T)+\text{null}(T)=\dim(V)
$$
## Proof
Let $\{ \vec{u}_{1},\dots,\vec{u}_{s} \}$ be a [[Basis|basis]] for $\text{ker}(T)$, and $\{ \vec{w}_{1},\dots,\vec{w}_{t} \}$ be a sbasis for $\text{im}(T)$, and suppose $\{ \vec{v}_{1},\dots,\vec{v}_{t} \}\subseteq V$ with $T(\vec{v}_{i})=\vec{w}_{i}$ for all $i$, then we are claiming $\{ \vec{u}_{1},\dots,\vec{u}_{s},\vec{v}_{1},\dots,\vec{v}_{t} \}$ is a basis for $V$. If the claim is true, we have $\text{rk}(T)+\text{null}(T)=t+s=\dim(V)$
To prove the claim we need to first check it is [[Span|spanning]]:
Suppose $\vec{v}\in V$, then $\exists\lambda_{i}$ such that 
$$
\text{im}(T)\ni T(\vec{v})=\lambda_{1}\vec{w}_{1}+\dots+\lambda_{t}\vec{w}_{t}=T(\lambda_{1}\vec{v}_{1}+\dots+\lambda_{t}\vec{v}_{t})
$$
So we see
$$
T(\vec{v}-\lambda_{1}\vec{v}_{1}-\dots-\lambda_{t}\vec{v}_{t})=\vec{0}
$$
So $\vec{v}-\lambda_{1}\vec{v}_{1}-\dots-\lambda_{t}\vec{v}_{t}$ is in the kernel of $T$, so $\exists \mu_{j}$ with
$$
\vec{v}-\lambda_{1}\vec{v}_{1}-\dots-\lambda_t\vec{v}_{t}=\mu_{1}\vec{u}_{1}+\dots+\mu_{s}\vec{u}_{s}
$$
So
$$
\vec{v}=\lambda_{1}\vec{v}_{1}+\dots+\lambda_{t}\vec{v}_{t}+\mu_{1}\vec{u}_{1}+..+\mu_{s}\vec{u}_{s}
$$
So we have spanning, next we need [[Linear Independence|linear independence]]
Suppose
$$
\lambda_{1}\vec{v}_{1}+\dots+\lambda_{t}\vec{v}_{t}+\mu_{1}\vec{u}_{1}+\dots+\mu_{s}\vec{u}_{s}=\vec{0}
$$
By applying $T$:
$$
\lambda_{1}\vec{w}_{1}+\dots+\lambda_{t}\vec{w}_{t}+\vec{0}+\dots+\vec{0}=T(\vec{0})=\vec{0}
$$
So we must have $\lambda_{1}=\dots=\lambda_{t}=0$, since $\vec{w}_{i}$s formed a basis, so the original equation becomes:
$$
\mu_{1}\vec{u}_{1}+\dots+\mu_{s}\vec{u}_{s}=\vec{0}
$$
So since the $\vec{u}_{i}$'s also formed a basis, $\mu_{1}=\dots=\mu_{s}=0$, hence linearly independent 
$W^{5}$

#Mathematics #LinAlg #Theorem 