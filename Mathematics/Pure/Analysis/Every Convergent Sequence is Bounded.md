We can see from graphs that this appears to be true
![[Every Convergent Sequence is Bounded 2024-07-07 19.40.23.excalidraw]]

## Proof
If $a_{n}$ is a [[Convergence|convergent]] [[Sequences|sequence]] with limit $l$, then:
$$
\forall\epsilon>0\exists N_{\epsilon}:n\geq N_{\epsilon}\implies \left| a_{n}-l \right|<\epsilon
$$
So consider $\epsilon>0$, $N_{\epsilon}$ exists and if $n\geq N_{\epsilon}$ then
$$
\left| a_{n}-l \right|<\epsilon 
$$
$$
\implies -\epsilon<a_{n}-l<\epsilon 
$$
$$
\implies l-\epsilon<a_{n}<l+\epsilon 
$$
$$
\implies \left| a_{n} \right|<max(\left| l-\epsilon \right|,\left| l+\epsilon \right|)
$$
So $a_{n}$ is [[Boundedness|bounded]]
If $n<N_{\epsilon}$, then $a_{n}$ forms a finite set, so $\left| a_{n} \right|\leq |a_{i}|$ for some $i<N_{\epsilon}$ and $i \in\mathbb{N}$, so it is bounded
So if $M=max(\left| l-\epsilon \right|,\left| l+\epsilon \right|,\left| a_{i} \right|)$
then $\left| a_{n} \right|\leq M$ so $a_{n}$ is bounded
## Proposition: Every bounded sequence is convergent
This is not true, as we can consider $a_{n}=(-1)^{n}$
$$
\left| a_{n} \right|=1
$$
$$
\implies \left| a_{n} \right|<2
$$
So $a_{n}$ is bounded, but $a_{n}$ is not convergent

#Mathematics #Limits #Theorem 