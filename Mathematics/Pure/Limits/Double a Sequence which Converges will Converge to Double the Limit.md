If $a_{n}$ is a [[Sequences|sequence]] which [[Convergence|converges]] to $l$ and $b_{n}$ is the sequence defined by $b_{n}=2a_{n}$, then $b_{n}$ converges to $2l$
## Proof
Given $a_{n}$ converges to $l$ and $b_{n}=2a_{n}$
If $\epsilon>0$ then $\exists N_{\epsilon}:n\geq N_{\epsilon}\implies \left| a_{n}-l \right|<\epsilon$
Also since $\frac{\epsilon}{2}>0$, then $\exists N_{a}:n\geq N_{a}\implies \left| a_{n} -l \right|<\frac{\epsilon}{2}$ so
$$
-\frac{\epsilon}{2}<a_{n}-l<\frac{\epsilon}{2}
$$
$$
\implies -\epsilon<2a_{n}-2l<\epsilon 
$$
$$
\implies \left| 2a_{n}-2l \right|<\epsilon 
$$
$$
\implies \left| b_{n}-2l \right|<\epsilon
$$
So $b_{n}$ converges to $2l$

#Mathematics #Limits #Theorem 