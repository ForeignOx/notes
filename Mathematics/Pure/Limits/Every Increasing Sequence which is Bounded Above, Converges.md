## Proof
If $a_{n}$ is an [[Sequences|increasing sequence]] which is [[Boundedness|bounded above]], then$a_{n+1}\geq a_{n}\forall n\in\mathbb{N}$ and $\exists U\in\mathbb{R}:a_{n} \leq U,\forall n\in\mathbb{N}$ so there must be a supremum $M\in\mathbb{R}$ 
Let $\epsilon>0$
Consider $M-\epsilon<M$, so $M-\epsilon$ cannot be an upper bound because $M$ is the supremum so there must exist some $i\in\mathbb{N}:a_{i}>M-\epsilon$ 
And $a_{i+1}\geq a_{i}$ and $a_{n}\geq a_{i}$ if $n>i$, so take $N_{\epsilon}=i$
If
$$
n\geq N_{\epsilon}
$$
$$
\implies i
$$
$$
\implies a_{n}\geq a_{i}>M-\epsilon 
$$
$$
\implies -\epsilon<a_{n}-M
$$
Also, $\forall n,a_{n}\leq M$ so $a_{n}<M+\epsilon$

$$
\implies\epsilon>a_{n}-M
$$
Sooo
$$
-\epsilon<a_{n}-M<\epsilon 
$$
$$
\implies \left| a_{n}-M \right|<\epsilon
$$
So $a_{n}$ [[Convergence|converges]] to $M$

#Mathematics #Limits #Theorem 